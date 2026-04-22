<!DOCTYPE html>
<html>
<head>
  <title>Upload File to GitHub</title>
</head>
<body>
  <h2>Upload Data to GitHub</h2>
  <form id="uploadForm">
    <input type="file" id="fileInput" />
    <button type="button" onclick="uploadFile()">Upload</button>
  </form>

  <script>
    async function uploadFile() {
      const fileInput = document.getElementById('fileInput');
      const file = fileInput.files[0];
      if (!file) {
        alert("Please select a file first!");
        return;
      }

      // Convert file to Base64
      const reader = new FileReader();
      reader.onload = async function() {
        const content = reader.result.split(',')[1];

        // Replace with your GitHub details
        const repo = "your-repo-name";
        const owner = "your-username";
        const path = file.name; // file will be uploaded with its name
        const token = "YOUR_GITHUB_PERSONAL_ACCESS_TOKEN";

        const response = await fetch(`https://api.github.com/repos/${owner}/${repo}/contents/${path}`, {
          method: "PUT",
          headers: {
            "Authorization": `token ${token}`,
            "Content-Type": "application/json"
          },
          body: JSON.stringify({
            message: "Upload file via HTML form",
            content: content
          })
        });

        if (response.ok) {
          alert("File uploaded successfully!");
        } else {
          alert("Upload failed: " + response.statusText);
        }
      };
      reader.readAsDataURL(file);
    }
  </script>
</body>
</html>

This form allows you to enter your details to be added to the site. The form generates an email that can be used to make a page, however the process is manual so please be patient it may take up to a fortnight for it to appear.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Signup form</title>
    <style>
        /* body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        } */
        .container {
            width: 100%;
            max-width: 600px;
            /* background-color: #fff; */
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        label {
            margin-bottom: 5px;
            margin-top: 15px;
        }
        input, select, textarea, button {
            margin-bottom: 15px;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
        }
        button[type="button"] {
            background-color: #008CBA;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Contact Form</h1>
        <form
          action="https://formspree.io/f/xjkbkqaj"
          method="POST"
          enctype="multipart/form-data"
        >
          <label>
            Title (academic only):
            <select name="title">
              <option value="Dr">Dr</option>
              <option value="Prof.">Prof</option>
              <option value="">None</option>
              <!-- add more titles as needed -->
            </select>
          </label>
          <label>
            Your email:
            <input type="email" name="email"> </label>
          </label>
          <label>
            Profile Picture (completely optional):
            <input type="file" name="profile_picture">
          </label>
          <label>
            Personal Website:
            <input type="url" name="personal_website">
          </label>
          <label>
            Google Scholar Page:
            <input type="url" name="google_scholar">
          </label>
          <label>
            ORCID:
            <input type="url" name="orcid">
          </label>
          <label>
            Research Interests and short Bio:
            <textarea name="research_bio"></textarea>
          </label>
          <label>
            Collaborators (please use full names, with no titles):
            <div id="collaborators">
              <input type="text" name="collaborators[]">
            </div>
            <button type="button" onclick="addCollaborator()">Add Collaborator</button>
          </label>
          <label>
            Students and Lab Members (please use full names with no titles):
            <div id="students">
              <input type="text" name="students[]">
            </div>
            <button type="button" onclick="addStudent()">Add Student/Lab Member</button>
          </label>
          <label>
            Primary Academic Disciplines (you may select multiple):
            <select name="primary_disciplines[]" multiple>
              <option value="Biology">Biology</option>
              <option value="Chemistry">Chemistry</option>
              <option value="Physics">Physics</option>
              <option value="Psychology">Psychology</option>
              <option value="Mathematics">Mathematics</option>
              <option value="Computer Science">Computer Science</option>
              <option value="Engineering">Engineering</option>
              <option value="Medicine">Medicine</option>
              <option value="Law">Law</option>
              <option value="Business">Business</option>
              <option value="Economics">Economics</option>
              <option value="Political Science">Political Science</option>
              <option value="Sociology">Sociology</option>
              <option value="Anthropology">Anthropology</option>
              <option value="History">History</option>
              <option value="Literature">Literature</option>
              <option value="Philosophy">Philosophy</option>
              <option value="Art">Art</option>
              <option value="Music">Music</option>
              <!-- add more disciplines as needed -->
            </select>
          </label>
          <label>
            Sub-disciplines (please use accepted terminology in your field, tags may be merged for clarity by the admin):
            <div id="subdisciplines">
              <input type="text" name="subdisciplines[]">
              <input type="text" name="subdisciplines[]">
              <input type="text" name="subdisciplines[]">
            </div>
            <button type="button" onclick="addSubdiscipline()">Add Sub-discipline</button>
          </label>
          <label>
            Your message:
            <textarea name="message"></textarea>
          </label>
          <button type="submit">Send</button>
        </form>
    </div>
    <script>
      function addCollaborator() {
        var div = document.createElement('div');
        div.innerHTML = '<input type="text" name="collaborators[]">';
        document.getElementById('collaborators').appendChild(div);
      }

      function addStudent() {
        var div = document.createElement('div');
        div.innerHTML = '<input type="text" name="students[]">';
        document.getElementById('students').appendChild(div);
      }

      function addSubdiscipline() {
        var div = document.createElement('div');
        div.innerHTML = '<input type="text" name="subdisciplines[]">';
        document.getElementById('subdisciplines').appendChild(div);
      }
    </script>
</body>
</html>



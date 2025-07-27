# password-generator
A simple and customizable password generator built with Python that creates strong, secure passwords using letters, numbers, and symbols.
function generatePassword() {
  const length = parseInt(document.getElementById('lengthSlider').value);
  let charset = '';

  if (document.getElementById('uppercase').checked) charset += 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  if (document.getElementById('lowercase').checked) charset += 'abcdefghijklmnopqrstuvwxyz';
  if (document.getElementById('numbers').checked) charset += '0123456789';
  if (document.getElementById('symbols').checked) charset += '!@#$%^&*()_+-=[]{}|;:,.<>?';

  if (!charset) return alert('Please select at least one character type!');

  let password = '';
  for (let i = 0; i < length; i++) {
    password += charset.charAt(Math.floor(Math.random() * charset.length));
  }

  document.getElementById('generatedPassword').value = password;
}

 This snippet highlights:

✅ Custom character set

✅ Random password logic

✅ DOM interaction
cd path/to/your/project-folder
git init
git remote add origin https://github.com/jujjharshini17-arch/password-generator.git
git add .
git commit -m "Initial commit - password generator"
git push -u origin master

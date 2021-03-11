# Vhosts configuration for XAMPP on Windows 10.

Configuration was tested with XAMPP containing PHP 7.2 & 7.3.

### Installation

1. Download repository as ZIP.
2. Copy all files from the ZIP to main XAMPP directory (default: C:/xampp).
3. Open `apache/conf/extra/httpd-vhosts.conf` file and change "C:/Projects" to the path where you would like to store your projects.

> Also remeber to create this directory before starting xampp.

4. Go to `C:\Windows\System32\drivers\etc\hosts` and add the following entries:

```
127.0.0.1       localhost
127.0.0.1       *.localhost
```

> Make sure to open `hosts` file in editor with system admin privileges. For example Notepad++ is a good editor for this purpose.

### Usage

1. Now go to your projects directory (by default: `C:/Projects`) and create the folder with the name of your project.

> Important: Use only basic ASCII characters!
> The name of the folder you create is the name of the subdomain under which your webstite will run.
> Example: If you create `C:/Projects/my-super-website` folder, then your subdomain will be: `my-super-website.localhost`.

2. Inside your project directory create `public` folder. This is the place where all your files will be accessible by the web server (apache from xampp). Here you should create your index.php or index.html file.

### Testing

1. Launch apache from xampp control panel.
2. Open your browser and type your project domain with the following schema: `<project directory>.localhost`.

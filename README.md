# How to update chromedriver on Ubuntu

I always forget how to update it the best way and - I admit - I always need to recheck it on StackOverflow. So time that I store in my own repos for a quick lookup:

```bash
version=$(curl -s "https://chromedriver.storage.googleapis.com/LATEST_RELEASE")
wget -qP /tmp/ "https://chromedriver.storage.googleapis.com/${version}/chromedriver_linux64.zip"
sudo unzip -o /tmp/chromedriver_linux64.zip -d /usr/bin
```

Source: https://stackoverflow.com/a/57306360

---

## Chromedriver Update (npm)

Afterwards you may want to update your chromedriver via npm:

```bash
npm i -g chromedriver --detect_chromedriver_version --chromedriver-force-download
```

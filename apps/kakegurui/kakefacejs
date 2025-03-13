g.clear();

function getFormattedDate() {
  let time = new Date();
  let days = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
  let months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"];
  
  let day = days[time.getDay()];
  let month = months[time.getMonth()];
  let date = time.getDate();
  let year = time.getFullYear();
  
  return `${day} ${month} ${date} ${year}`;
}

function drawClock() {
  let time = new Date();
  let hours = ("0" + time.getHours()).slice(-2);
  let minutes = ("0" + time.getMinutes()).slice(-2);
  let formattedDate = getFormattedDate();

  g.setColor("#000000");
  g.fillRect(0, 0, g.getWidth(), g.getHeight());

  g.setColor("#ff0000");
  g.drawRect(2, 2, g.getWidth() - 2, g.getHeight() - 2);

  g.setFont("Vector", 40);
  g.setFontAlign(0, 0);
  g.drawString(hours + ":" + minutes, g.getWidth()/2, g.getHeight()/2 - 10);

  g.setFont("Vector", 18);
  g.drawString(formattedDate, g.getWidth()/2, g.getHeight()/2 + 30);

  g.flip();
}

setInterval(drawClock, 60000);
drawClock();

Bangle.setLCDPower(1);
Bangle.setLocked(false);

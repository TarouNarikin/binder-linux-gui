FROM ubuntu:latest
RUN apt update && apt install -y xfce4 x11vnc xvfb novnc wget
RUN mkdir ~/.vnc && x11vnc -storepasswd 1234 ~/.vnc/passwd
CMD ["sh", "-c", "Xvfb :1 -screen 0 1024x768x16 & x11vnc -display :1 -rfbauth ~/.vnc/passwd -forever"]

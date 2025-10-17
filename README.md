# make-qr-code
qr code generation via python in a simple way



import qrcode as qr
from pyzbar.pyzbar import decode
from PIL import Image


img = qr.make("www.linkedin.com/in/prashant23012006")
img2 = qr.make("https://github.com/iprashantsinghh")
img.save("prashant.linkedin.png")

img2 = qr.make("https://github.com/iprashantsinghh")

img2.save("prashant.github.png")


a = decode(Image.open("myqr.png"))
print(a[0].data.decode("ascii"))



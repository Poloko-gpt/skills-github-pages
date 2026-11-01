<video id="camara"
       autoplay
       playsinline
       style="width:100%">
</video>

<button onclick="iniciarCamara()">
  Activar cámara
</button>

<script>
async function iniciarCamara() {
  try {
    const stream =
      await navigator.mediaDevices.getUserMedia({
        video: {
          facingMode: "environment"
        },
        audio: false
      });

    document.getElementById("camara").srcObject =
      stream;

  } catch (error) {
    alert(error.name + ": " + error.message);
  }
}
</script>

title: Welcome to my blog!
---

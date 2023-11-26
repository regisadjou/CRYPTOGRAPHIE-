# FONCTION DE CHIFFREMENT ET DE DECHIFFREMENT DE CESAR en JavaScript 

<script>
function crypto(a, d) {
  let b = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z'];
  let c = [];

  for (let i = 0; i <= a.length - 1; i++) {
    for (let j = 0; j <= b.length - 1; j++) {
      if (a[i] === b[j]) {
        let y = (i + d) % 26;
        c[i] = b[y];
      }
    }
  }

  for (let i = 0; i <= a.length - 1; i++) {
    for (let j = 0; j <= b.length - 1; j++) {
      if (a[i] === b[j]) {
        let e = c[j];
        document.write(e);
      }
    }
  }
}

function decrypto(a, d) {
  let b = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z'];
  let c = [];

  for (let i = 0; i <= a.length-1; i++) {
    for (let j = 0; j <= b.length-1; j++) {
      if (a[i] === b[j]) {
       
        let y = (j - d + 26) % 26;
        c[i] = b[y];
        document.write(c[i]);
      }
    }
  }
}
</script>

<script>

crypto(['H','A','B','I','L','L','E','Z',
  'V','O','U','S',
  'C','O','N','V','E','N','A','B','L','E','M','E','N','T'], 3);


//decrypto(['K','D','E','L','O','O','H',
  //'C','Y','R','X',
  //'V','F','R','Q','Y','H','Q','D','E','O','H','P','H','Q','W'], 3);
</script>

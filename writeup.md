# Write-up: Mushroom CTF

## Step 1: Investigation
Extract the zip file and inspect the image metadata.

Command:
`exiftool image_0.png`

Look for the `Comment` field in the output. You will find this hidden string:
`Hitta nyckeln: Q1RGe3N2YW1wYXJfYXJfYmFzdH0=`

## Step 2: Decoding
The string ends with an `=` sign and appears to be random characters, which indicates Base64 encoding. Decode it using your terminal.

Command:
`echo "Q1RGe3N2YW1wYXJfYXJfYmFzdH0=" | base64 -d`

## The Flag
Running the decode command reveals the final flag:
`CTF{svampar_ar_bast}`

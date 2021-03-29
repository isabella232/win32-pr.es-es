---
description: Importar la clave pública de los controladores
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importar la clave pública de los controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906707"
---
# <a name="importing-the-drivers-public-key"></a>Importar la clave pública de los controladores

La clave pública RSA del controlador se encuentra en las etiquetas de módulo y exponente del nodo hoja del certificado. Ambos valores están codificados en Base64 y deben descodificarse. Si usa CryptoAPI de Microsoft, debe importar la clave en un proveedor de servicios criptográficos (CSP), que es el módulo que implementa los algoritmos criptográficos.

Para convertir el módulo y los exponentes de la codificación Base64 a matrices binarias, utilice la función **CryptStringToBinary** , tal como se muestra en el código siguiente. Llame una vez a la función para obtener el tamaño de la matriz de bytes. A continuación, asigne el búfer y vuelva a llamar a la función.


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



La matriz codificada en Base64 está en orden big-endian, mientras que la CryptoAPI espera el número en orden Little-endian, por lo que debe intercambiar el orden de bytes de la matriz que se devuelve desde **CryptStringToBinary**. El módulo es de 256 bytes, pero la matriz de bytes descodificada puede ser inferior a 256 bytes. Si es así, deberá asignar una nueva matriz de 256 bytes, copiar los datos en la nueva matriz y rellenar la parte delantera de la matriz con ceros. El exponente es un valor de DWORD (4 bytes).

Una vez que tenga los valores de módulo y exponente, puede importar la clave en el proveedor de servicios criptográficos (CSP) predeterminado, tal como se muestra en el código siguiente:


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



Ahora puede usar CryptoAPI para cifrar comandos y solicitudes de estado con la clave pública del controlador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




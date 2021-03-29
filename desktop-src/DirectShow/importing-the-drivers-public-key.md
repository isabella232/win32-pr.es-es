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
# <a name="importing-the-drivers-public-key"></a><span data-ttu-id="663fb-103">Importar la clave pública de los controladores</span><span class="sxs-lookup"><span data-stu-id="663fb-103">Importing the Drivers Public Key</span></span>

<span data-ttu-id="663fb-104">La clave pública RSA del controlador se encuentra en las etiquetas de módulo y exponente del nodo hoja del certificado.</span><span class="sxs-lookup"><span data-stu-id="663fb-104">The driver's RSA public key is contained in the Modulus and Exponent tags of the certificate's leaf node.</span></span> <span data-ttu-id="663fb-105">Ambos valores están codificados en Base64 y deben descodificarse.</span><span class="sxs-lookup"><span data-stu-id="663fb-105">Both values are base64-encoded and must be decoded.</span></span> <span data-ttu-id="663fb-106">Si usa CryptoAPI de Microsoft, debe importar la clave en un proveedor de servicios criptográficos (CSP), que es el módulo que implementa los algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="663fb-106">If you are using Microsoft's CryptoAPI, you must import the key into a cryptographic service provider (CSP), which is the module that implements the cryptographic algorithms.</span></span>

<span data-ttu-id="663fb-107">Para convertir el módulo y los exponentes de la codificación Base64 a matrices binarias, utilice la función **CryptStringToBinary** , tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="663fb-107">To convert the modulus and exponents from base64 encoding to binary arrays, use the **CryptStringToBinary** function, as shown in the following code.</span></span> <span data-ttu-id="663fb-108">Llame una vez a la función para obtener el tamaño de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="663fb-108">Call the function once to get the size of the byte array.</span></span> <span data-ttu-id="663fb-109">A continuación, asigne el búfer y vuelva a llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="663fb-109">Then allocate the buffer and call the function again.</span></span>


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



<span data-ttu-id="663fb-110">La matriz codificada en Base64 está en orden big-endian, mientras que la CryptoAPI espera el número en orden Little-endian, por lo que debe intercambiar el orden de bytes de la matriz que se devuelve desde **CryptStringToBinary**.</span><span class="sxs-lookup"><span data-stu-id="663fb-110">The base64-encoded array is in big-endian order, whereas the CryptoAPI expects the number in little-endian order, so you need to swap the byte order of the array that is returned from **CryptStringToBinary**.</span></span> <span data-ttu-id="663fb-111">El módulo es de 256 bytes, pero la matriz de bytes descodificada puede ser inferior a 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="663fb-111">The modulus is 256 bytes, but the decoded byte array might be less than 256 bytes.</span></span> <span data-ttu-id="663fb-112">Si es así, deberá asignar una nueva matriz de 256 bytes, copiar los datos en la nueva matriz y rellenar la parte delantera de la matriz con ceros.</span><span class="sxs-lookup"><span data-stu-id="663fb-112">If so, you will need to allocate a new array that is 256 bytes, copy the data into the new array, and pad the front of the array with zeros.</span></span> <span data-ttu-id="663fb-113">El exponente es un valor de DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="663fb-113">The exponent is a DWORD (4-byte) value.</span></span>

<span data-ttu-id="663fb-114">Una vez que tenga los valores de módulo y exponente, puede importar la clave en el proveedor de servicios criptográficos (CSP) predeterminado, tal como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="663fb-114">After you have the modulus and exponent values, you can import the key into the default cryptographic service provider (CSP), as shown in the following code:</span></span>


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



<span data-ttu-id="663fb-115">Ahora puede usar CryptoAPI para cifrar comandos y solicitudes de estado con la clave pública del controlador.</span><span class="sxs-lookup"><span data-stu-id="663fb-115">Now you can use the CryptoAPI to encrypt commands and status requests with the driver's public key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="663fb-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="663fb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663fb-117">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="663fb-117">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




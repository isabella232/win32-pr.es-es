---
description: Inicio de una sesión copp
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Inicio de una sesión copp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e3d952e7e938eee3eef27663ea075b3a5b23d4e61ef9f9fd0ea9b5395708cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748675"
---
# <a name="initiating-a-copp-session"></a>Inicio de una sesión copp

Para iniciar una sesión del Protocolo de protección de salida certificado (COPP), debe preparar una firma *,* que es una matriz que contiene la concatenación de los números siguientes:

-   Número aleatorio de 128 bits devuelto por el controlador. (Este valor se muestra como *guidRandom* en [Obtención de la cadena de certificados del controlador).](obtaining-the-drivers-certificate-chain.md)
-   Una clave AES simétrica de 128 bits.
-   Número de secuencia inicial de 32 bits para las solicitudes de estado.
-   Número de secuencia inicial de 32 bits para los comandos COPP.

Genere una clave AES simétrica como se muestra a continuación:


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



La **función CryptGenKey** crea la clave simétrica, pero la clave todavía se mantiene en el CSP. Para exportar la clave a una matriz de bytes, use la **función CryptExportKey.** Este es el motivo para usar la marca EXPORTABLE de CRYPT \_ al llamar **a CryptGenKey.** El código siguiente exporta la clave y la copia en el


```
pData
```



.


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



Los datos devueltos en


```
pData
```



tiene el diseño siguiente:


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



Sin embargo, no se define ninguna estructura que coincida con este diseño en los encabezados CryptoAPI. Puede definir uno o realizar alguna aritmética de puntero. Por ejemplo, para comprobar el tamaño de la clave:


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



Para obtener el puntero a la propia clave:


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



A continuación, genere un número aleatorio de 32 bits que se usará como secuencia de inicio para las solicitudes de estado copp. La manera recomendada de crear un número aleatorio es llamar a la **función CryptGenRandom.** No use la **función rand** en la biblioteca en tiempo de ejecución de C, porque no es realmente aleatoria. Genere un segundo número aleatorio de 32 bits que se usará como secuencia de inicio para los comandos COPP.


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



Ahora puede preparar la firma COPP. Se trata de una matriz de 256 bytes, definida como la [**estructura AMCOPPSignature.**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) Inicialice el contenido de la matriz en cero. A continuación, copie los cuatro números en la matriz: el número aleatorio del controlador, la clave AES, el número de secuencia de estado y el número de secuencia de comandos, en ese orden. Por último, intercambie el orden de bytes de toda la matriz.

Según la documentación de **CryptEncrypt**:

<dl> "La longitud de los datos de texto no cifrado que se pueden cifrar con una llamada a **CryptEncrypt** con una clave RSA es la longitud del módulo de clave menos once bytes. Los once bytes son el mínimo elegido para el relleno PKCS \# 1".  
</dl>

En este caso, el módulo es de 256 bytes, por lo que la longitud máxima del mensaje es de 245 bytes (256 – 11). La **estructura AMCOPPSignature** es de 256 bytes, pero los datos significativos de la firma son solo 40 bytes. El código siguiente cifra la firma y proporciona el resultado en


```
CoppSig
```



.


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



Ahora pase la matriz cifrada [**a IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



Si este método se realiza correctamente, está listo para enviar comandos COPP y solicitudes de estado al controlador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




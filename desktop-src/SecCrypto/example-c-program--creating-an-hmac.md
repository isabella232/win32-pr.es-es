---
description: Se usa para comprobar que un mensaje no se ha cambiado durante el tránsito.
ms.assetid: a4bb67fb-8217-4e76-b1bf-461ccd39f58a
title: 'Programa C de ejemplo: Creación de un HMAC'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4f6a91025ed159e580cfcb9780527536a31f4f72ae54d5a821a328d45abec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765893"
---
# <a name="example-c-program-creating-an-hmac"></a>Programa C de ejemplo: Creación de un HMAC

Normalmente, se usa una suma de comprobación de autenticación de mensajes hash (HMAC) para comprobar que un mensaje no se ha cambiado durante el tránsito. Ambas partes del mensaje deben tener una clave secreta compartida. El remitente combina la clave y el mensaje en una cadena, crea una síntesis de la cadena mediante un algoritmo como SHA-1 o MD5 y transmite el mensaje y la síntesis. El receptor combina la clave compartida con el mensaje, aplica el algoritmo adecuado y compara el resumen obtenido con el transmitido por el remitente. Si los resúmenes son exactamente iguales, el mensaje no se alteró.

En este ejemplo se muestran las siguientes tareas y funciones cryptoAPI:

-   Adquirir un identificador para un proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) mediante una [**llamada a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Derivar una clave simétrica de una cadena de bytes mediante una llamada a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash), [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)y [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).
-   Uso de la clave simétrica para crear un objeto hash HMAC mediante una llamada a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) y [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).
-   Hashing a message by calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).
-   Recuperar el hash mediante una [**llamada a CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam).


```C++
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>

int main()
{
//--------------------------------------------------------------------
// Declare variables.
//
// hProv:           Handle to a cryptographic service provider (CSP). 
//                  This example retrieves the default provider for  
//                  the PROV_RSA_FULL provider type.  
// hHash:           Handle to the hash object needed to create a hash.
// hKey:            Handle to a symmetric key. This example creates a 
//                  key for the RC4 algorithm.
// hHmacHash:       Handle to an HMAC hash.
// pbHash:          Pointer to the hash.
// dwDataLen:       Length, in bytes, of the hash.
// Data1:           Password string used to create a symmetric key.
// Data2:           Message string to be hashed.
// HmacInfo:        Instance of an HMAC_INFO structure that contains 
//                  information about the HMAC hash.
// 
HCRYPTPROV  hProv       = NULL;
HCRYPTHASH  hHash       = NULL;
HCRYPTKEY   hKey        = NULL;
HCRYPTHASH  hHmacHash   = NULL;
PBYTE       pbHash      = NULL;
DWORD       dwDataLen   = 0;
BYTE        Data1[]     = {0x70,0x61,0x73,0x73,0x77,0x6F,0x72,0x64};
BYTE        Data2[]     = {0x6D,0x65,0x73,0x73,0x61,0x67,0x65};
HMAC_INFO   HmacInfo;

//--------------------------------------------------------------------
// Zero the HMAC_INFO structure and use the SHA1 algorithm for
// hashing.

ZeroMemory(&HmacInfo, sizeof(HmacInfo));
HmacInfo.HashAlgid = CALG_SHA1;

//--------------------------------------------------------------------
// Acquire a handle to the default RSA cryptographic service provider.

if (!CryptAcquireContext(
    &hProv,                   // handle of the CSP
    NULL,                     // key container name
    NULL,                     // CSP name
    PROV_RSA_FULL,            // provider type
    CRYPT_VERIFYCONTEXT))     // no key access is requested
{
   printf(" Error in AcquireContext 0x%08x \n",
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Derive a symmetric key from a hash object by performing the
// following steps:
//    1. Call CryptCreateHash to retrieve a handle to a hash object.
//    2. Call CryptHashData to add a text string (password) to the 
//       hash object.
//    3. Call CryptDeriveKey to create the symmetric key from the
//       hashed password derived in step 2.
// You will use the key later to create an HMAC hash object. 

if (!CryptCreateHash(
    hProv,                    // handle of the CSP
    CALG_SHA1,                // hash algorithm to use
    0,                        // hash key
    0,                        // reserved
    &hHash))                  // address of hash object handle
{
   printf("Error in CryptCreateHash 0x%08x \n",
          GetLastError());
   goto ErrorExit;
}

if (!CryptHashData(
    hHash,                    // handle of the hash object
    Data1,                    // password to hash
    sizeof(Data1),            // number of bytes of data to add
    0))                       // flags
{
   printf("Error in CryptHashData 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptDeriveKey(
    hProv,                    // handle of the CSP
    CALG_RC4,                 // algorithm ID
    hHash,                    // handle to the hash object
    0,                        // flags
    &hKey))                   // address of the key handle
{
   printf("Error in CryptDeriveKey 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Create an HMAC by performing the following steps:
//    1. Call CryptCreateHash to create a hash object and retrieve 
//       a handle to it.
//    2. Call CryptSetHashParam to set the instance of the HMAC_INFO 
//       structure into the hash object.
//    3. Call CryptHashData to compute a hash of the message.
//    4. Call CryptGetHashParam to retrieve the size, in bytes, of
//       the hash.
//    5. Call malloc to allocate memory for the hash.
//    6. Call CryptGetHashParam again to retrieve the HMAC hash.

if (!CryptCreateHash(
    hProv,                    // handle of the CSP.
    CALG_HMAC,                // HMAC hash algorithm ID
    hKey,                     // key for the hash (see above)
    0,                        // reserved
    &hHmacHash))              // address of the hash handle
{
   printf("Error in CryptCreateHash 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptSetHashParam(
    hHmacHash,                // handle of the HMAC hash object
    HP_HMAC_INFO,             // setting an HMAC_INFO object
    (BYTE*)&HmacInfo,         // the HMAC_INFO object
    0))                       // reserved
{
   printf("Error in CryptSetHashParam 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

if (!CryptHashData(
    hHmacHash,                // handle of the HMAC hash object
    Data2,                    // message to hash
    sizeof(Data2),            // number of bytes of data to add
    0))                       // flags
{
   printf("Error in CryptHashData 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

//--------------------------------------------------------------------
// Call CryptGetHashParam twice. Call it the first time to retrieve
// the size, in bytes, of the hash. Allocate memory. Then call 
// CryptGetHashParam again to retrieve the hash value.

if (!CryptGetHashParam(
    hHmacHash,                // handle of the HMAC hash object
    HP_HASHVAL,               // query on the hash value
    NULL,                     // filled on second call
    &dwDataLen,               // length, in bytes, of the hash
    0))
{
   printf("Error in CryptGetHashParam 0x%08x \n", 
          GetLastError());
   goto ErrorExit;
}

pbHash = (BYTE*)malloc(dwDataLen);
if(NULL == pbHash) 
{
   printf("unable to allocate memory\n");
   goto ErrorExit;
}
    
if (!CryptGetHashParam(
    hHmacHash,                 // handle of the HMAC hash object
    HP_HASHVAL,                // query on the hash value
    pbHash,                    // pointer to the HMAC hash value
    &dwDataLen,                // length, in bytes, of the hash
    0))
{
   printf("Error in CryptGetHashParam 0x%08x \n", GetLastError());
   goto ErrorExit;
}

// Print the hash to the console.

printf("The hash is:  ");
for(DWORD i = 0 ; i < dwDataLen ; i++) 
{
   printf("%2.2x ",pbHash[i]);
}
printf("\n");

// Free resources.
ErrorExit:
    if(hHmacHash)
        CryptDestroyHash(hHmacHash);
    if(hKey)
        CryptDestroyKey(hKey);
    if(hHash)
        CryptDestroyHash(hHash);    
    if(hProv)
        CryptReleaseContext(hProv, 0);
    if(pbHash)
        free(pbHash);
    return 0;
}

```



 

 

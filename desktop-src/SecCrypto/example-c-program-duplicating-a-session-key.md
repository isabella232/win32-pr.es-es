---
description: En el ejemplo siguiente se crea una clave de sesión aleatoria, se duplica la clave, se establecen algunos parámetros adicionales en la clave original y se destruyen las claves originales y duplicadas.
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 'Programa C de ejemplo: duplicación de una clave de sesión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4116a021b358864da27b2eb94d66a0f74f1462232f58441e7af5c2c7b91e114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007793"
---
# <a name="example-c-program-duplicating-a-session-key"></a>Programa C de ejemplo: duplicación de una clave de sesión

En el ejemplo siguiente se crea una clave de sesión [*aleatoria,*](../secgloss/s-gly.md)se duplica la clave, se establecen algunos parámetros adicionales en la clave original y se destruyen las claves originales y duplicadas. En este ejemplo se muestra el uso de [**CryptDuplicateKey y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) funciones relacionadas.

En este ejemplo se muestran las siguientes tareas y funciones cryptoAPI:

-   Acceso a [*un proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) mediante [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Crear una clave de sesión [**mediante CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).
-   Duplicación de la clave creada mediante [**CryptDuplicateKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey)
-   Usar [**CryptSetKeyParam para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) modificar el proceso de generación de claves de dos maneras diferentes.
-   Rellenar un búfer con bytes aleatorios mediante [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).
-   Destruir las claves mediante [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).
-   Publicación del CSP con [**CryptReleaseContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

En este ejemplo se usa la [**función MyHandleError**](myhandleerror.md). El código de esta función se incluye con el ejemplo. El código para esta y otras funciones auxiliares también se muestra en [De uso general Functions](general-purpose-functions.md).


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(    
   &hCryptProv,
   NULL,
   NULL,
   PROV_RSA_FULL,
   0)) 
{    
    printf("CryptAcquireContext succeeded. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 

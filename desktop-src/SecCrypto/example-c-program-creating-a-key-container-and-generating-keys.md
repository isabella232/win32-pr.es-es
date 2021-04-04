---
description: Crea un contenedor de claves con nombre y agrega un par de claves de firma y un par de claves de intercambio al contenedor.
ms.assetid: b9d13024-0e53-4930-9962-a2a0d0cb88de
title: 'Programa C de ejemplo: crear un contenedor de claves y generar claves'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e389df22cb4e745cf1c1a65542a17eeabe9b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277958"
---
# <a name="example-c-program-creating-a-key-container-and-generating-keys"></a>Programa C de ejemplo: crear un contenedor de claves y generar claves

En el ejemplo siguiente se crea un [*contenedor de claves*](../secgloss/k-gly.md) con nombre y se agrega un par de claves de [*firma*](../secgloss/s-gly.md) y un par de [*claves de intercambio*](../secgloss/e-gly.md) al contenedor. Este ejemplo se puede ejecutar sin problemas aunque el contenedor de claves con nombre y las claves criptográficas ya existan.

> [!Note]  
> Una aplicación no debe utilizar el contenedor de claves predeterminado para almacenar las claves privadas. Cuando varias aplicaciones usan el mismo contenedor, una aplicación puede cambiar o destruir las claves que otra aplicación necesita tener disponibles. Se recomienda que las aplicaciones utilicen contenedores de claves que están vinculados a la aplicación. Al hacerlo, se reduce el riesgo de que otras aplicaciones manipulen las claves necesarias para que una aplicación funcione correctamente.

 

En este ejemplo se muestran las siguientes tareas y funciones de CryptoAPI:

1.  Intenta adquirir el contenedor de claves con nombre. Si el contenedor de claves con nombre todavía no existe, se crea.
2.  Si no existe un par de claves de firma en el contenedor de claves, se crea un par de claves de firma en el contenedor de claves.
3.  Si no existe un par de claves de intercambio en el contenedor de claves, se crea un par de claves de intercambio en el contenedor de claves.

Estas operaciones solo deben realizarse una vez para cada usuario en cada equipo. Si el contenedor de claves con nombre y los pares de claves ya se han creado, este ejemplo no realiza ninguna operación.

En este ejemplo se usan las siguientes funciones de CryptoAPI:

-   [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)
-   [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
-   [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)
-   [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

En este ejemplo se usa la función [**MyHandleError**](myhandleerror.md). El código de esta función se incluye con el ejemplo. El código de esta y otras funciones auxiliares también se enumeran en [funciones de de uso general](general-purpose-functions.md).


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void main(void) 
{ 
    // Handle for the cryptographic provider context.
    HCRYPTPROV hCryptProv;        
    
    // The name of the container.
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    //---------------------------------------------------------------
    // Begin processing. Attempt to acquire a context by using the 
    // specified key container.
    if(CryptAcquireContext(
        &hCryptProv,
        pszContainerName,
        NULL,
        PROV_RSA_FULL,
        0))
    {
        _tprintf(
            TEXT("A crypto context with the %s key container ")
            TEXT("has been acquired.\n"), 
            pszContainerName);
    }
    else
    { 
        //-----------------------------------------------------------
        // Some sort of error occurred in acquiring the context. 
        // This is most likely due to the specified container 
        // not existing. Create a new key container.
        if(GetLastError() == NTE_BAD_KEYSET)
        {
            if(CryptAcquireContext(
                &hCryptProv, 
                pszContainerName, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("A new key container has been ")
                    TEXT("created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create a new key ")
                    TEXT("container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("CryptAcquireContext failed.\n"));
        }
    }

    //---------------------------------------------------------------
    // A context with a key container is available.
    // Attempt to get the handle to the signature key. 

    // Public/private key handle.
    HCRYPTKEY hKey;               
    
    if(CryptGetUserKey(
        hCryptProv,
        AT_SIGNATURE,
        &hKey))
    {
        _tprintf(TEXT("A signature key is available.\n"));
    }
    else
    {
        _tprintf(TEXT("No signature key is available.\n"));
        if(GetLastError() == NTE_NO_KEY) 
        {
            //-------------------------------------------------------
            // The error was that there is a container but no key.

            // Create a signature key pair. 
            _tprintf(TEXT("The signature key does not exist.\n"));
            _tprintf(TEXT("Create a signature key pair.\n")); 
            if(CryptGenKey(
                hCryptProv,
                AT_SIGNATURE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Created a signature key pair.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred creating a ")
                    TEXT("signature key.\n")); 
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("getting a signature key.\n"));
        }
    } // End if.

    _tprintf(TEXT("A signature key pair existed, or one was ")
        TEXT("created.\n\n"));

    // Destroy the signature key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    } 

    // Next, check the exchange key. 
    if(CryptGetUserKey(
        hCryptProv,
        AT_KEYEXCHANGE,
        &hKey)) 
    {
        _tprintf(TEXT("An exchange key exists.\n"));
    }
    else
    {
        _tprintf(TEXT("No exchange key is available.\n"));

        // Check to determine whether an exchange key 
        // needs to be created.
        if(GetLastError() == NTE_NO_KEY) 
        { 
            // Create a key exchange key pair.
            _tprintf(TEXT("The exchange key does not exist.\n"));
            _tprintf(TEXT("Attempting to create an exchange key ")
                TEXT("pair.\n"));
            if(CryptGenKey(
                hCryptProv,
                AT_KEYEXCHANGE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Exchange key pair created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred attempting to ")
                    TEXT("create an exchange key.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("occurred.\n"));
        }
    }

    // Destroy the exchange key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    }

    // Release the CSP.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv, 0)))
        {
            MyHandleError(TEXT("Error during CryptReleaseContext."));
        }
    } 
    
    _tprintf(TEXT("Everything is okay. A signature key "));
    _tprintf(TEXT("pair and an exchange key exist in "));
    _tprintf(TEXT("the %s key container.\n"), pszContainerName);  
} // End main.
```



 

 

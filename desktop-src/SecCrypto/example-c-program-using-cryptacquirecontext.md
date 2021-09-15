---
description: Muestra varias maneras diferentes de usar CryptAcquireContext y las funciones CryptoAPI relacionadas para trabajar con un proveedor de servicios criptográficos (CSP) y un contenedor de claves.
ms.assetid: e8d2503c-a38f-44f6-a653-ae9c7bf903bd
title: 'Programa de C de ejemplo: uso de CryptAcquireContext'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074d1967d8a32001e620b089280c034887b90cd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473466"
---
# <a name="example-c-program-using-cryptacquirecontext"></a>Programa de C de ejemplo: uso de CryptAcquireContext

En el ejemplo siguiente se muestran varias maneras diferentes de usar [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) y las funciones cryptoAPI relacionadas para trabajar con un proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y un contenedor de [*claves*](../secgloss/k-gly.md).

En este ejemplo se muestran las siguientes tareas y funciones cryptoAPI:

-   Use la [**función CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para adquirir un identificador para el CSP predeterminado y el contenedor de claves predeterminado. Si no existe ningún contenedor de claves predeterminado, use **la función CryptAcquireContext** para crear el contenedor de claves predeterminado.
-   Use la [**función CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) para recuperar información sobre un CSP y un contenedor de claves.
-   Aumente el [*número de referencias*](../secgloss/r-gly.md) en el proveedor mediante la función [**CryptContextAddRef.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref)
-   Libere un CSP mediante la [**función CryptReleaseContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)
-   Cree un contenedor de claves con nombre mediante la [**función CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   Adquiera un identificador para un CSP mediante el contenedor de claves recién creado.
-   Elimine un contenedor de claves mediante la [**función CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)

En este ejemplo se usa la [**función MyHandleError**](myhandleerror.md). El código de esta función se incluye con el ejemplo. El código para esta y otras funciones auxiliares también se muestra en [De uso general Functions](general-purpose-functions.md).


```C++
//-------------------------------------------------------------------
//  Copyright (C) Microsoft.  All rights reserved.
//  Example code using CryptAcquireContext.
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
    //---------------------------------------------------------------
    // Declare and initialize variables.
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Get a handle to the default PROV_RSA_FULL provider.
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        NULL, 
        PROV_RSA_FULL, 
        0)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
    }
    else
    {
        if (GetLastError() == NTE_BAD_KEYSET)
        {
            // No default container was found. Attempt to create it.
            if(CryptAcquireContext(
                &hCryptProv, 
                NULL, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("CryptAcquireContext succeeded.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create the default ")
                    TEXT("key container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("A general error running ")
                TEXT("CryptAcquireContext."));
        }
    }

    CHAR pszName[1000];
    DWORD cbName;

    //---------------------------------------------------------------
    // Read the name of the CSP.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_NAME, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Provider name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading CSP name.\n"));
    }

    //---------------------------------------------------------------
    // Read the name of the key container.
    cbName = 1000;
    if(CryptGetProvParam(
        hCryptProv, 
        PP_CONTAINER, 
        (BYTE*)pszName, 
        &cbName, 
        0))
    {
        _tprintf(TEXT("CryptGetProvParam succeeded.\n"));
        printf("Key Container name: %s\n", pszName);
    }
    else
    {
        MyHandleError(TEXT("Error reading key container name.\n"));
    }
    //---------------------------------------------------------------
    // Perform cryptographic operations.
    //...

    //---------------------------------------------------------------
    //  Add to the reference count on the provider. When the 
    //  reference count on a provider is greater than one,  
    //  CryptReleaseContext reduces the reference count but does not 
    //  free the provider.

    if(CryptContextAddRef(
        hCryptProv, 
        NULL, 
        0)) 
    {
        _tprintf(TEXT("CryptcontextAddRef succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptContextAddRef!\n"));
    }

    //---------------------------------------------------------------
    //  The reference count on hCryptProv is now greater than one. 
    //  The first call to CryptReleaseContext will not release the 
    //  provider handle. 

    //---------------------------------------------------------------
    //  Release the context once.
    if (CryptReleaseContext(hCryptProv, 0))
    {
        _tprintf(TEXT("The first call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #1!\n"));
    }

    //---------------------------------------------------------------
    // Release the provider handle again.
    if (CryptReleaseContext(hCryptProv, 0)) 
    {
        _tprintf(TEXT("The second call to CryptReleaseContext ")
            TEXT("succeeded.\n"));
    }
    else
    {
        MyHandleError(TEXT("Error during ")
            TEXT("CryptReleaseContext #2!\n"));
    }

    //---------------------------------------------------------------
    // Get a handle to a PROV_RSA_FULL provider and
    // create a key container named "My Sample Key Container".
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    hCryptProv = NULL;
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName,
        NULL, 
        PROV_RSA_FULL, 
        CRYPT_NEWKEYSET)) 
    {
        _tprintf(TEXT("CryptAcquireContext succeeded. \n"));
        _tprintf(TEXT("New key set created. \n")); 

        //-----------------------------------------------------------
        // Release the provider handle and the key container.
        if(hCryptProv)
        {
            if(CryptReleaseContext(hCryptProv, 0)) 
            {
                hCryptProv = NULL;
                _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
            }
            else
            {
                MyHandleError(TEXT("Error during ")
                    TEXT("CryptReleaseContext!\n"));
            }
        }
    }
    else
    {
        if(GetLastError() == NTE_EXISTS)
        {
            _tprintf(TEXT("The named key container could not be ")
                TEXT("created because it already exists.\n"));
            
            // Just continue the program. The named container 
            // will be reopened below.
        }
        else
        {
            MyHandleError(TEXT("Error during CryptAcquireContext ")
                TEXT("for a new key container."));
        }
    }

    //---------------------------------------------------------------
    // Get a handle to the provider by using the new key container. 
    // Note: This key container will be empty until keys
    // are explicitly created by using the CryptGenKey function.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        0)) 
    {
        _tprintf(TEXT("Acquired the key set just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }

    //---------------------------------------------------------------
    // Perform cryptographic operations.

    //---------------------------------------------------------------
    // Release the provider handle.
    if(CryptReleaseContext(
        hCryptProv, 
        0)) 
    {
        _tprintf(TEXT("CryptReleaseContext succeeded. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptReleaseContext!\n"));
    }

    //---------------------------------------------------------------
    // Delete the new key container.
    if(CryptAcquireContext(
        &hCryptProv, 
        pszContainerName, 
        NULL, 
        PROV_RSA_FULL,
        CRYPT_DELETEKEYSET)) 
    {
        _tprintf(TEXT("Deleted the key container just created. \n"));
    }
    else
    {
        MyHandleError(TEXT("Error during CryptAcquireContext!\n"));
    }
} // End of main.
```



 

 

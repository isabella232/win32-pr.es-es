---
description: El proveedor base solo utilizó claves simétricas de 40 bits.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nueva funcionalidad de longitud de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278798"
---
# <a name="new-key-length-functionality"></a>Nueva funcionalidad de longitud de clave

El proveedor base solo utilizó [*claves simétricas*](../secgloss/s-gly.md)de 40 bits. La adición de claves más largas en el proveedor mejorado y el hecho de que las claves importadas pueden ser de longitud arbitraria requiere un método para consultar la longitud de una clave específica. Para encontrar la longitud real de una clave en bits, un usuario puede llamar a [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con el \_ valor del parámetro KEYLEN de KP. La longitud de la clave se devuelve en el **valor DWORD** al que apunta el parámetro *pbData* .

> [!Note]  
> Para protegerse contra los ataques de [*Cryptanalysis*](../secgloss/c-gly.md) de paso a través, las aplicaciones deben comprobar si hay [*longitudes de clave*](../secgloss/k-gly.md) insuficientes y notificar al usuario cuando se encuentre una.

 

En el ejemplo siguiente se muestra cómo consultar la longitud de una clave.


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 

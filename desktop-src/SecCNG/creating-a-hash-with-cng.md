---
description: Los valores hash son más útiles para comprobar la integridad de los datos cuando se usan con un algoritmo de firma asimétrica.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Crear un hash con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666219"
---
# <a name="creating-a-hash-with-cng"></a>Crear un hash con CNG

Un [*hash*](/windows/desktop/SecGloss/h-gly) es una operación unidireccional que se realiza en un bloque de datos para crear un valor hash único que representa el contenido de los datos. Independientemente de Cuándo se realice el hash, el mismo [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se realiza en los mismos datos siempre generará el mismo valor hash. Si se cambia alguno de los datos, el valor hash cambiará correctamente.

Los valores hash no son útiles para el cifrado de datos porque no están diseñados para reproducirlos en el valor hash. Los valores hash son más útiles para comprobar la integridad de los datos cuando se usan con un algoritmo de firma asimétrica. Por ejemplo, si ha aplicado un algoritmo hash a un mensaje de texto, ha firmado el hash e incluido el valor hash firmado con el mensaje original, el destinatario podría comprobar el hash firmado, crear el valor hash para el mensaje recibido y, a continuación, comparar este valor hash con el valor hash firmado incluido en el mensaje original. Si los dos valores hash son idénticos, el destinatario puede estar seguro de que el mensaje original no se ha modificado.

El tamaño del valor hash es fijo para un algoritmo hash determinado. Esto significa que, independientemente de si el bloque de datos es grande o pequeño, el valor hash siempre tendrá el mismo tamaño. Por ejemplo, el algoritmo hash SHA256 tiene un tamaño de valor hash de 256 bits.

-   [Crear un objeto hash](#creating-a-hashing-object)
-   [Crear un objeto hash reutilizable](#creating-a-reusable-hashing-object)
-   [Duplicar un objeto hash](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Crear un objeto hash

Para crear un hash mediante CNG, realice los pasos siguientes:

1.  Abra un proveedor de algoritmos que admita el algoritmo deseado. Los algoritmos hash típicos incluyen MD2, MD4, MD5, SHA-1 y SHA256. Llame a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) y especifique el identificador de algoritmo adecuado en el parámetro *pszAlgId* . La función devuelve un identificador al proveedor.
2.  Realice los pasos siguientes para crear el objeto hash:

    1.  Obtenga el tamaño del objeto llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar la propiedad **de \_ \_ longitud del objeto BCRYPT** .
    2.  Asigna memoria para contener el objeto hash.
    3.  Cree el objeto llamando a la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .

3.  Aplicar un algoritmo hash a los datos. Esto implica llamar a la función [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) una o varias veces. Cada llamada anexa los datos especificados al hash.
4.  Realice los pasos siguientes para obtener el valor hash:

    1.  Recupere el tamaño del valor llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obtener la propiedad de **\_ \_ longitud de hash BCRYPT** .
    2.  Asigne memoria para contener el valor.
    3.  Recupere el valor hash mediante una llamada a la función [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) . Después de llamar a esta función, el objeto hash ya no es válido.

5.  Para completar este procedimiento, debe realizar los siguientes pasos de limpieza:

    1.  Cierre el objeto hash pasando el identificador hash a la función [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libere la memoria que asignó para el objeto hash.
    3.  Si no va a crear más objetos hash, cierre el proveedor de algoritmos pasando el identificador de proveedor a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .

        Si va a crear más objetos hash, se recomienda volver a usar el proveedor de algoritmos en lugar de crear y destruir el mismo tipo de proveedor de algoritmos varias veces.

    4.  Cuando haya terminado de usar la memoria del valor hash, libere.

En el ejemplo siguiente se muestra cómo crear un valor hash mediante CNG.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

}

```



## <a name="creating-a-reusable-hashing-object"></a>Crear un objeto hash reutilizable

A partir de Windows 8 y Windows Server 2012, puede crear un objeto hash reutilizable para los escenarios que requieren que se calculen varios hash o HMAC en una sucesión rápida. Para ello, especifique el **marcador BCRYPT \_ \_ reutilizable \_ hash** al llamar a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) . Todos los proveedores de algoritmos hash de Microsoft admiten esta marca. Un objeto hash creado con esta marca se puede volver a usar inmediatamente después de llamar a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) como si se hubiera creado recientemente llamando a [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Realice los pasos siguientes para crear un objeto hash reutilizable:

1.  Abra un proveedor de algoritmos que admita el algoritmo hash deseado. Llame a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) y especifique el identificador de algoritmo adecuado en el parámetro *pszAlgId* y el **\_ \_ \_ marcador BCRYPT reutilizable hash** en el parámetro *dwFlags* . La función devuelve un identificador al proveedor.
2.  Realice los pasos siguientes para crear el objeto hash:

    1.  Obtenga el tamaño del objeto llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar la propiedad **de \_ \_ longitud del objeto BCRYPT** .
    2.  Asigna memoria para contener el objeto hash.
    3.  Cree el objeto llamando a la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Especifique **el \_ \_ \_ indicador reutilizable hash BCRYPT** en el parámetro *dwFlags* .

3.  Aplicar un algoritmo hash a los datos mediante una llamada a la función [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .
4.  Realice los pasos siguientes para obtener el valor hash:

    1.  Obtenga el tamaño del valor hash llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obtener la propiedad **de \_ \_ longitud de hash BCRYPT** .
    2.  Asigne memoria para contener el valor.
    3.  Obtenga el valor hash llamando a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Para volver a usar el objeto hash con datos nuevos, vaya al paso 3.
6.  Para completar este procedimiento, debe realizar los siguientes pasos de limpieza:

    1.  Cierre el objeto hash pasando el identificador hash a la función [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libere la memoria que asignó para el objeto hash.
    3.  Si no va a crear más objetos hash, cierre el proveedor de algoritmos pasando el identificador de proveedor a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .
    4.  Cuando haya terminado de usar la memoria del valor hash, libere.

## <a name="duplicating-a-hash-object"></a>Duplicar un objeto hash

En algunas circunstancias, puede ser útil aplicar un algoritmo hash a cierta cantidad de datos comunes y, a continuación, crear dos objetos hash independientes a partir de los datos comunes. No es necesario crear dos objetos hash independientes y aplicar un algoritmo hash a los datos comunes para lograrlo. Puede crear un único objeto hash y agregar todos los datos comunes al objeto hash. A continuación, puede usar la función [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) para crear un duplicado del objeto hash original. El objeto hash duplicado contiene toda la información de estado y los datos con hash como el original, pero es un objeto hash completamente independiente. Ahora puede Agregar los datos únicos a cada uno de los objetos hash y obtener el valor hash tal como se muestra en el ejemplo. Esta técnica es útil cuando se aplica un algoritmo hash a una cantidad posiblemente grande de datos comunes. Solo tiene que agregar los datos comunes al hash original una vez y, después, puede duplicar el objeto hash para obtener un objeto hash único.

 

 

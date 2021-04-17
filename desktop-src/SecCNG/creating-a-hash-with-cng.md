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
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="384fe-103">Crear un hash con CNG</span><span class="sxs-lookup"><span data-stu-id="384fe-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="384fe-104">Un [*hash*](/windows/desktop/SecGloss/h-gly) es una operación unidireccional que se realiza en un bloque de datos para crear un valor hash único que representa el contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="384fe-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="384fe-105">Independientemente de Cuándo se realice el hash, el mismo [*algoritmo hash*](/windows/desktop/SecGloss/h-gly) que se realiza en los mismos datos siempre generará el mismo valor hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="384fe-106">Si se cambia alguno de los datos, el valor hash cambiará correctamente.</span><span class="sxs-lookup"><span data-stu-id="384fe-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="384fe-107">Los valores hash no son útiles para el cifrado de datos porque no están diseñados para reproducirlos en el valor hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="384fe-108">Los valores hash son más útiles para comprobar la integridad de los datos cuando se usan con un algoritmo de firma asimétrica.</span><span class="sxs-lookup"><span data-stu-id="384fe-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="384fe-109">Por ejemplo, si ha aplicado un algoritmo hash a un mensaje de texto, ha firmado el hash e incluido el valor hash firmado con el mensaje original, el destinatario podría comprobar el hash firmado, crear el valor hash para el mensaje recibido y, a continuación, comparar este valor hash con el valor hash firmado incluido en el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="384fe-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="384fe-110">Si los dos valores hash son idénticos, el destinatario puede estar seguro de que el mensaje original no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="384fe-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="384fe-111">El tamaño del valor hash es fijo para un algoritmo hash determinado.</span><span class="sxs-lookup"><span data-stu-id="384fe-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="384fe-112">Esto significa que, independientemente de si el bloque de datos es grande o pequeño, el valor hash siempre tendrá el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="384fe-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="384fe-113">Por ejemplo, el algoritmo hash SHA256 tiene un tamaño de valor hash de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="384fe-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="384fe-114">Crear un objeto hash</span><span class="sxs-lookup"><span data-stu-id="384fe-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="384fe-115">Crear un objeto hash reutilizable</span><span class="sxs-lookup"><span data-stu-id="384fe-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="384fe-116">Duplicar un objeto hash</span><span class="sxs-lookup"><span data-stu-id="384fe-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="384fe-117">Crear un objeto hash</span><span class="sxs-lookup"><span data-stu-id="384fe-117">Creating a Hashing Object</span></span>

<span data-ttu-id="384fe-118">Para crear un hash mediante CNG, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="384fe-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="384fe-119">Abra un proveedor de algoritmos que admita el algoritmo deseado.</span><span class="sxs-lookup"><span data-stu-id="384fe-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="384fe-120">Los algoritmos hash típicos incluyen MD2, MD4, MD5, SHA-1 y SHA256.</span><span class="sxs-lookup"><span data-stu-id="384fe-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="384fe-121">Llame a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) y especifique el identificador de algoritmo adecuado en el parámetro *pszAlgId* .</span><span class="sxs-lookup"><span data-stu-id="384fe-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="384fe-122">La función devuelve un identificador al proveedor.</span><span class="sxs-lookup"><span data-stu-id="384fe-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="384fe-123">Realice los pasos siguientes para crear el objeto hash:</span><span class="sxs-lookup"><span data-stu-id="384fe-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="384fe-124">Obtenga el tamaño del objeto llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar la propiedad **de \_ \_ longitud del objeto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="384fe-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="384fe-125">Asigna memoria para contener el objeto hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="384fe-126">Cree el objeto llamando a la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="384fe-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="384fe-127">Aplicar un algoritmo hash a los datos.</span><span class="sxs-lookup"><span data-stu-id="384fe-127">Hash the data.</span></span> <span data-ttu-id="384fe-128">Esto implica llamar a la función [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) una o varias veces.</span><span class="sxs-lookup"><span data-stu-id="384fe-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="384fe-129">Cada llamada anexa los datos especificados al hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="384fe-130">Realice los pasos siguientes para obtener el valor hash:</span><span class="sxs-lookup"><span data-stu-id="384fe-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="384fe-131">Recupere el tamaño del valor llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obtener la propiedad de **\_ \_ longitud de hash BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="384fe-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="384fe-132">Asigne memoria para contener el valor.</span><span class="sxs-lookup"><span data-stu-id="384fe-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="384fe-133">Recupere el valor hash mediante una llamada a la función [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) .</span><span class="sxs-lookup"><span data-stu-id="384fe-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="384fe-134">Después de llamar a esta función, el objeto hash ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="384fe-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="384fe-135">Para completar este procedimiento, debe realizar los siguientes pasos de limpieza:</span><span class="sxs-lookup"><span data-stu-id="384fe-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="384fe-136">Cierre el objeto hash pasando el identificador hash a la función [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="384fe-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="384fe-137">Libere la memoria que asignó para el objeto hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="384fe-138">Si no va a crear más objetos hash, cierre el proveedor de algoritmos pasando el identificador de proveedor a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="384fe-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="384fe-139">Si va a crear más objetos hash, se recomienda volver a usar el proveedor de algoritmos en lugar de crear y destruir el mismo tipo de proveedor de algoritmos varias veces.</span><span class="sxs-lookup"><span data-stu-id="384fe-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="384fe-140">Cuando haya terminado de usar la memoria del valor hash, libere.</span><span class="sxs-lookup"><span data-stu-id="384fe-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="384fe-141">En el ejemplo siguiente se muestra cómo crear un valor hash mediante CNG.</span><span class="sxs-lookup"><span data-stu-id="384fe-141">The following example shows how to create a hash value by using CNG.</span></span>


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



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="384fe-142">Crear un objeto hash reutilizable</span><span class="sxs-lookup"><span data-stu-id="384fe-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="384fe-143">A partir de Windows 8 y Windows Server 2012, puede crear un objeto hash reutilizable para los escenarios que requieren que se calculen varios hash o HMAC en una sucesión rápida.</span><span class="sxs-lookup"><span data-stu-id="384fe-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="384fe-144">Para ello, especifique el **marcador BCRYPT \_ \_ reutilizable \_ hash** al llamar a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="384fe-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="384fe-145">Todos los proveedores de algoritmos hash de Microsoft admiten esta marca.</span><span class="sxs-lookup"><span data-stu-id="384fe-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="384fe-146">Un objeto hash creado con esta marca se puede volver a usar inmediatamente después de llamar a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) como si se hubiera creado recientemente llamando a [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="384fe-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="384fe-147">Realice los pasos siguientes para crear un objeto hash reutilizable:</span><span class="sxs-lookup"><span data-stu-id="384fe-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="384fe-148">Abra un proveedor de algoritmos que admita el algoritmo hash deseado.</span><span class="sxs-lookup"><span data-stu-id="384fe-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="384fe-149">Llame a la función [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) y especifique el identificador de algoritmo adecuado en el parámetro *pszAlgId* y el **\_ \_ \_ marcador BCRYPT reutilizable hash** en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="384fe-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="384fe-150">La función devuelve un identificador al proveedor.</span><span class="sxs-lookup"><span data-stu-id="384fe-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="384fe-151">Realice los pasos siguientes para crear el objeto hash:</span><span class="sxs-lookup"><span data-stu-id="384fe-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="384fe-152">Obtenga el tamaño del objeto llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para recuperar la propiedad **de \_ \_ longitud del objeto BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="384fe-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="384fe-153">Asigna memoria para contener el objeto hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="384fe-154">Cree el objeto llamando a la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="384fe-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="384fe-155">Especifique **el \_ \_ \_ indicador reutilizable hash BCRYPT** en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="384fe-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="384fe-156">Aplicar un algoritmo hash a los datos mediante una llamada a la función [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="384fe-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="384fe-157">Realice los pasos siguientes para obtener el valor hash:</span><span class="sxs-lookup"><span data-stu-id="384fe-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="384fe-158">Obtenga el tamaño del valor hash llamando a la función [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) para obtener la propiedad **de \_ \_ longitud de hash BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="384fe-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="384fe-159">Asigne memoria para contener el valor.</span><span class="sxs-lookup"><span data-stu-id="384fe-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="384fe-160">Obtenga el valor hash llamando a [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span><span class="sxs-lookup"><span data-stu-id="384fe-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="384fe-161">Para volver a usar el objeto hash con datos nuevos, vaya al paso 3.</span><span class="sxs-lookup"><span data-stu-id="384fe-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="384fe-162">Para completar este procedimiento, debe realizar los siguientes pasos de limpieza:</span><span class="sxs-lookup"><span data-stu-id="384fe-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="384fe-163">Cierre el objeto hash pasando el identificador hash a la función [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="384fe-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="384fe-164">Libere la memoria que asignó para el objeto hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="384fe-165">Si no va a crear más objetos hash, cierre el proveedor de algoritmos pasando el identificador de proveedor a la función [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="384fe-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="384fe-166">Cuando haya terminado de usar la memoria del valor hash, libere.</span><span class="sxs-lookup"><span data-stu-id="384fe-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="384fe-167">Duplicar un objeto hash</span><span class="sxs-lookup"><span data-stu-id="384fe-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="384fe-168">En algunas circunstancias, puede ser útil aplicar un algoritmo hash a cierta cantidad de datos comunes y, a continuación, crear dos objetos hash independientes a partir de los datos comunes.</span><span class="sxs-lookup"><span data-stu-id="384fe-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="384fe-169">No es necesario crear dos objetos hash independientes y aplicar un algoritmo hash a los datos comunes para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="384fe-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="384fe-170">Puede crear un único objeto hash y agregar todos los datos comunes al objeto hash.</span><span class="sxs-lookup"><span data-stu-id="384fe-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="384fe-171">A continuación, puede usar la función [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) para crear un duplicado del objeto hash original.</span><span class="sxs-lookup"><span data-stu-id="384fe-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="384fe-172">El objeto hash duplicado contiene toda la información de estado y los datos con hash como el original, pero es un objeto hash completamente independiente.</span><span class="sxs-lookup"><span data-stu-id="384fe-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="384fe-173">Ahora puede Agregar los datos únicos a cada uno de los objetos hash y obtener el valor hash tal como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="384fe-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="384fe-174">Esta técnica es útil cuando se aplica un algoritmo hash a una cantidad posiblemente grande de datos comunes.</span><span class="sxs-lookup"><span data-stu-id="384fe-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="384fe-175">Solo tiene que agregar los datos comunes al hash original una vez y, después, puede duplicar el objeto hash para obtener un objeto hash único.</span><span class="sxs-lookup"><span data-stu-id="384fe-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 

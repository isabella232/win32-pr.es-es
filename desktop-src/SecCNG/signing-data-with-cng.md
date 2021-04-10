---
description: La firma de datos no protege los datos. Solo se comprueba la integridad de los datos.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Firmar datos con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156137"
---
# <a name="signing-data-with-cng"></a><span data-ttu-id="4b288-104">Firmar datos con CNG</span><span class="sxs-lookup"><span data-stu-id="4b288-104">Signing Data with CNG</span></span>

<span data-ttu-id="4b288-105">La firma de datos no protege los datos.</span><span class="sxs-lookup"><span data-stu-id="4b288-105">Data signing does not protect the data.</span></span> <span data-ttu-id="4b288-106">Solo se comprueba la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="4b288-106">It only to verifies the integrity of the data.</span></span> <span data-ttu-id="4b288-107">El remitente aplica un algoritmo hash a los datos y firma (cifra) el hash mediante una clave privada.</span><span class="sxs-lookup"><span data-stu-id="4b288-107">The sender hashes that data and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="4b288-108">El destinatario previsto realiza la comprobación creando un hash de los datos recibidos, descifrando la firma para obtener el hash original y comparando los dos valores hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-108">The intended recipient performs verification by creating a hash of the data received, decrypting the signature to obtain the original hash, and comparing the two hashes.</span></span>

<span data-ttu-id="4b288-109">Cuando los datos están firmados, el remitente crea un valor [*hash*](/windows/desktop/SecGloss/h-gly) y firma (cifra) el hash mediante una clave privada.</span><span class="sxs-lookup"><span data-stu-id="4b288-109">When data is signed, the sender creates a [*hash*](/windows/desktop/SecGloss/h-gly) value and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="4b288-110">Esta firma se adjunta a los datos y se envían en un mensaje a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="4b288-110">This signature is then attached to the data and sent in a message to a recipient.</span></span> <span data-ttu-id="4b288-111">El algoritmo hash que se usó para crear la firma debe conocerse de antemano por el destinatario o identificarse en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b288-111">The hashing algorithm that was used to create the signature must be known in advance by the recipient or identified in the message.</span></span> <span data-ttu-id="4b288-112">La forma de hacer esto es el protocolo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4b288-112">How this is done is up to the message protocol.</span></span>

<span data-ttu-id="4b288-113">Para comprobar la firma, el destinatario extrae los datos y la firma del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b288-113">To verify the signature, the recipient extracts the data and the signature from the message.</span></span> <span data-ttu-id="4b288-114">A continuación, el destinatario crea otro valor hash a partir de los datos, descifra el hash firmado mediante la clave pública del remitente y compara los dos valores hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-114">The recipient then creates another hash value from the data, decrypts the signed hash by using the sender's public key, and compares the two hash values.</span></span> <span data-ttu-id="4b288-115">Si los valores son idénticos, se ha comprobado la firma y se supone que los datos no están alterados.</span><span class="sxs-lookup"><span data-stu-id="4b288-115">If the values are identical, the signature has been verified and the data is assumed to be unaltered.</span></span>

<span data-ttu-id="4b288-116">**Para crear una firma mediante CNG**</span><span class="sxs-lookup"><span data-stu-id="4b288-116">**To create a signature by using CNG**</span></span>

1.  <span data-ttu-id="4b288-117">Cree un valor hash para los datos mediante las funciones hash de CNG.</span><span class="sxs-lookup"><span data-stu-id="4b288-117">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="4b288-118">Para obtener más información sobre cómo crear un hash, vea [crear un hash con CNG](creating-a-hash-with-cng.md).</span><span class="sxs-lookup"><span data-stu-id="4b288-118">For more information about creating a hash, see [Creating a Hash With CNG](creating-a-hash-with-cng.md).</span></span>
2.  <span data-ttu-id="4b288-119">Cree una clave asimétrica para firmar el hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-119">Create an asymmetric key to sign the hash.</span></span> <span data-ttu-id="4b288-120">Puede crear una clave persistente con las funciones de [almacenamiento de claves CNG](cng-key-storage-functions.md) o una clave efímera con las [funciones primitivas criptográficas de CNG](cng-cryptographic-primitive-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4b288-120">You can either create a persistent key with the [CNG Key Storage Functions](cng-key-storage-functions.md) or an ephemeral key with the [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>
3.  <span data-ttu-id="4b288-121">Use las funciones [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) o [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) para firmar (cifrar) el valor hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-121">Use either the [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) or the [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) function to sign (encrypt) the hash value.</span></span> <span data-ttu-id="4b288-122">Esta función firma el valor hash mediante la clave asimétrica.</span><span class="sxs-lookup"><span data-stu-id="4b288-122">This function signs the hash value by using the asymmetric key.</span></span>
4.  <span data-ttu-id="4b288-123">Combine los datos y la firma en un mensaje que se puede enviar al destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="4b288-123">Combine the data and signature into a message which can be sent sent to the intended recipient.</span></span>

<span data-ttu-id="4b288-124">**Para comprobar una firma mediante CNG**</span><span class="sxs-lookup"><span data-stu-id="4b288-124">**To verify a signature by using CNG**</span></span>

1.  <span data-ttu-id="4b288-125">Extraiga los datos y la firma del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b288-125">Extract the data and signature from the message.</span></span>
2.  <span data-ttu-id="4b288-126">Cree un valor hash para los datos mediante las funciones hash de CNG.</span><span class="sxs-lookup"><span data-stu-id="4b288-126">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="4b288-127">El algoritmo hash utilizado debe ser el mismo que se usó para firmar el hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-127">The hashing algorithm used must be the same algorithm that was used to sign he hash.</span></span>
3.  <span data-ttu-id="4b288-128">Obtenga la parte pública del par de claves asimétricas que se usó para firmar el hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-128">Obtain the public portion of the asymmetric key pair that was used to sign the hash.</span></span> <span data-ttu-id="4b288-129">La forma de obtener esta clave depende de cómo se haya creado y guardado la clave.</span><span class="sxs-lookup"><span data-stu-id="4b288-129">How you obtain this key depends on how the key was created and persisted.</span></span> <span data-ttu-id="4b288-130">Si la clave se creó o cargó con las [funciones de almacenamiento de claves CNG](cng-key-storage-functions.md), usará la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) para cargar la clave persistente.</span><span class="sxs-lookup"><span data-stu-id="4b288-130">If the key was created or loaded with the [CNG Key Storage Functions](cng-key-storage-functions.md), you will use the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function to load the persisted key.</span></span> <span data-ttu-id="4b288-131">Si la clave es una clave efímera, tendría que haberse guardado en un BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="4b288-131">If the key is an ephemeral key, then it would have to have been saved to a key BLOB.</span></span> <span data-ttu-id="4b288-132">Debe pasar este BLOB de clave a la función [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="4b288-132">You need to pass this key BLOB to either the [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) or the [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) function.</span></span>
4.  <span data-ttu-id="4b288-133">Pase el nuevo valor hash, la firma y el identificador de clave a la función [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) o [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) .</span><span class="sxs-lookup"><span data-stu-id="4b288-133">Pass the new hash value, the signature, and the key handle to either the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) or the [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) function.</span></span> <span data-ttu-id="4b288-134">Estas funciones realizan la comprobación mediante la clave pública para descifrar la firma y comparar el hash descifrado con el hash calculado en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="4b288-134">These functions perform verification by using the public key to decrypt the signature and comparing the decrypted hash to the hash computed in step 2.</span></span> <span data-ttu-id="4b288-135">La función **BCryptVerifySignature** devolverá un **estado \_ correcto** si la firma coincide con el hash o el **estado \_ \_ signatura no válida** si la firma no coincide con el hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-135">The **BCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **STATUS\_INVALID\_SIGNATURE** if the signature does not match the hash.</span></span> <span data-ttu-id="4b288-136">La función **NCryptVerifySignature** devolverá un **estado \_ correcto** si la firma coincide con el hash o con la **\_ \_ firma incorrecta de NTE** si la firma no coincide con el hash.</span><span class="sxs-lookup"><span data-stu-id="4b288-136">The **NCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **NTE\_BAD\_SIGNATURE** if the signature does not match the hash.</span></span>

## <a name="signing-and-verifying-data-example"></a><span data-ttu-id="4b288-137">Ejemplo de firma y comprobación de datos</span><span class="sxs-lookup"><span data-stu-id="4b288-137">Signing and Verifying Data Example</span></span>

<span data-ttu-id="4b288-138">En el ejemplo siguiente se muestra cómo usar las API primitivas criptográficas para firmar datos con una clave persistente y comprobar la firma con una clave efímera.</span><span class="sxs-lookup"><span data-stu-id="4b288-138">The following example shows how to use the cryptographic primitive APIs to sign data with a persisted key and verify the signature with an ephemeral key.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for ECDSA 256 signing using CNG
    
    Example for use of BCrypt/NCrypt API
    
    Persisted key for signing and ephemeral key for verification

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>
#include <ncrypt.h>


#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const  BYTE rgbMsg[] =
{
    0x04, 0x87, 0xec, 0x66, 0xa8, 0xbf, 0x17, 0xa6,
    0xe3, 0x62, 0x6f, 0x1a, 0x55, 0xe2, 0xaf, 0x5e,
    0xbc, 0x54, 0xa4, 0xdc, 0x68, 0x19, 0x3e, 0x94,
};

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{
    NCRYPT_PROV_HANDLE      hProv           = NULL;
    NCRYPT_KEY_HANDLE       hKey            = NULL;
    BCRYPT_KEY_HANDLE       hTmpKey         = NULL;
    SECURITY_STATUS         secStatus       = ERROR_SUCCESS;
    BCRYPT_ALG_HANDLE       hHashAlg        = NULL,
                            hSignAlg        = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbBlob          = 0,
                            cbSignature     = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL,
                            pbBlob          = NULL,
                            pbSignature     = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hHashAlg,
                                                BCRYPT_SHA1_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hSignAlg,
                                                BCRYPT_ECDSA_P256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
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
                                        hHashAlg, 
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
                                        hHashAlg, 
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

    //open handle to KSP
    if(FAILED(secStatus = NCryptOpenStorageProvider(
                                                &hProv, 
                                                MS_KEY_STORAGE_PROVIDER, 
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptOpenStorageProvider\n", secStatus);
        goto Cleanup;
    }

    //create a persisted key
    if(FAILED(secStatus = NCryptCreatePersistedKey(
                                                hProv,
                                                &hKey,
                                                NCRYPT_ECDSA_P256_ALGORITHM,
                                                L"my ecc key",
                                                0,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptCreatePersistedKey\n", secStatus);
        goto Cleanup;
    }

    //create key on disk
    if(FAILED(secStatus = NCryptFinalizeKey(hKey, 0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptFinalizeKey\n", secStatus);
        goto Cleanup;
    }

    //sign the hash
    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    NULL,
                                    0,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }


    //allocate the signature buffer
    pbSignature = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbSignature);
    if(NULL == pbSignature)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    pbSignature,
                                    cbSignature,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        pbBlob,
                                        cbBlob,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptImportKeyPair(
                                            hSignAlg,
                                            NULL,
                                            BCRYPT_ECCPUBLIC_BLOB,
                                            &hTmpKey,
                                            pbBlob,
                                            cbBlob,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptImportKeyPair\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptVerifySignature(
                                            hTmpKey,
                                            NULL,
                                            pbHash,
                                            cbHash,
                                            pbSignature,
                                            cbSignature,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptVerifySignature\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hHashAlg)
    {
        BCryptCloseAlgorithmProvider(hHashAlg,0);
    }

    if(hSignAlg)
    {
        BCryptCloseAlgorithmProvider(hSignAlg,0);
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

    if(pbSignature)
    {
        HeapFree(GetProcessHeap(), 0, pbSignature);
    }

    if(pbBlob)
    {
        HeapFree(GetProcessHeap(), 0, pbBlob);
    }

    if (hTmpKey)    
    {
        BCryptDestroyKey(hTmpKey);
    }

    if (hKey)    
    {
        NCryptDeleteKey(hKey, 0);
    }

    if (hProv)    
    {
        NCryptFreeObject(hProv);
    }    
}


```



 

 

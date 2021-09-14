---
description: La firma de datos no protege los datos. Solo comprueba la integridad de los datos.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Firma de datos con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073645"
---
# <a name="signing-data-with-cng"></a>Firma de datos con CNG

La firma de datos no protege los datos. Solo comprueba la integridad de los datos. El remitente aplica un algoritmo hash a los datos y firma (cifra) el hash mediante una clave privada. El destinatario previsto realiza la comprobación creando un hash de los datos recibidos, descifrando la firma para obtener el hash original y comparando los dos hashes.

Cuando se firman los datos, el remitente crea un [*valor hash*](/windows/desktop/SecGloss/h-gly) y firma (cifra) el hash mediante una clave privada. A continuación, esta firma se adjunta a los datos y se envía en un mensaje a un destinatario. El destinatario debe conocer de antemano el algoritmo hash que se usó para crear la firma o identificarlo en el mensaje. La forma en que se hace esto es hasta el protocolo de mensajes.

Para comprobar la firma, el destinatario extrae los datos y la firma del mensaje. A continuación, el destinatario crea otro valor hash a partir de los datos, descifra el hash firmado mediante la clave pública del remitente y compara los dos valores hash. Si los valores son idénticos, se ha comprobado la firma y se supone que los datos no están modificados.

**Para crear una firma mediante CNG**

1.  Cree un valor hash para los datos mediante las funciones hash de CNG. Para obtener más información sobre cómo crear un hash, vea [Creating a Hash With CNG](creating-a-hash-with-cng.md).
2.  Cree una clave asimétrica para firmar el hash. Puede crear una clave persistente con la clave [CNG Storage Functions](cng-key-storage-functions.md) o una clave efímera con las funciones primitivas criptográficas [de CNG](cng-cryptographic-primitive-functions.md).
3.  Use [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) o la función [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) para firmar (cifrar) el valor hash. Esta función firma el valor hash mediante la clave asimétrica.
4.  Combine los datos y la firma en un mensaje que se puede enviar al destinatario previsto.

**Para comprobar una firma mediante CNG**

1.  Extraiga los datos y la firma del mensaje.
2.  Cree un valor hash para los datos mediante las funciones hash de CNG. El algoritmo hash utilizado debe ser el mismo algoritmo que se usó para firmar el hash.
3.  Obtenga la parte pública del par de claves asimétricas que se usó para firmar el hash. La forma de obtener esta clave depende de cómo se creó y persistió la clave. Si la clave se creó o cargó con la clave [CNG Storage Functions](cng-key-storage-functions.md), usará la función [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) para cargar la clave persistente. Si la clave es una clave efímera, tendría que guardarse en un blob de clave. Debe pasar este blob de clave a la [**función BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) o [**NCryptImportKey.**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey)
4.  Pase el nuevo valor hash, la firma y el identificador de clave a [**la función NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) o [**BCryptVerifySignature.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) Estas funciones realizan la comprobación mediante la clave pública para descifrar la firma y comparar el hash descifrado con el hash calculado en el paso 2. La **función BCryptVerifySignature** devolverá **STATUS \_ SUCCESS** si la firma coincide con el hash o **STATUS INVALID \_ \_ SIGNATURE** si la firma no coincide con el hash. La **función NCryptVerifySignature** devolverá **STATUS \_ SUCCESS** si la firma coincide con el hash o **NTE BAD \_ \_ SIGNATURE** si la firma no coincide con el hash.

## <a name="signing-and-verifying-data-example"></a>Ejemplo de firma y comprobación de datos

En el ejemplo siguiente se muestra cómo usar las API primitivas criptográficas para firmar datos con una clave persistente y comprobar la firma con una clave efímera.


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



 

 

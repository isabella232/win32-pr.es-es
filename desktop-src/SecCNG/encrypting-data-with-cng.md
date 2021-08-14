---
description: CNG permite cifrar datos mediante un número mínimo de llamadas de función y permite realizar toda la administración de memoria.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Cifrado de datos con CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b264518c2a0ccfe0f626c869ba3062c0429941234ca0c286f9e7801961485b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907743"
---
# <a name="encrypting-data-with-cng"></a>Cifrado de datos con CNG

El uso principal de cualquier API de criptografía es cifrar y descifrar datos. CNG permite cifrar datos mediante un número mínimo de llamadas de función y permite realizar toda la administración de memoria. Aunque muchos de los detalles de implementación del protocolo se quedan en el usuario, CNG proporciona las primitivas que realizan las tareas reales de cifrado y descifrado de datos.

-   [Cifrar datos](#encrypting-data-with-cng)
-   [Ejemplo de cifrado de datos](#encrypting-data-example)
-   [Descifrar datos](#decrypting-data)

## <a name="encrypting-data"></a>Cifrar datos

Para cifrar los datos, realice los pasos siguientes:

1.  Abra un proveedor de algoritmos que admita el cifrado, como **BCRYPT \_ DES \_ ALGORITHM**.
2.  Cree una clave con la que cifrar los datos. Se puede crear una clave mediante cualquiera de las siguientes funciones:
    -   [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) o [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) para proveedores asimétricos.
    -   [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) o [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) para proveedores simétricos.

    > [!Note]  
    > El cifrado y descifrado de datos con una clave asimétrica consumen muchos cálculos en comparación con el cifrado de claves simétricas. Si necesita cifrar datos con una clave asimétrica, debe cifrar los datos con una clave simétrica, cifrar la clave simétrica con una clave asimétrica e incluir la clave simétrica cifrada con el mensaje. A continuación, el destinatario puede descifrar la clave simétrica y usar la clave simétrica para descifrar los datos.

     

3.  Obtenga el tamaño de los datos cifrados. Esto se basa en el algoritmo de cifrado, el esquema de relleno (si existe) y el tamaño de los datos que se cifrarán. Puede obtener el tamaño de los datos cifrados mediante la [**función BCryptEncrypt,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) pasando **NULL** para el *parámetro pbOutput.* Todos los demás parámetros deben ser los mismos que cuando los datos se cifran realmente, excepto el *parámetro pbInput,* que no se usa en este caso.
4.  Puede cifrar los datos en su lugar con el mismo búfer o cifrar los datos en un búfer independiente.

    Si desea cifrar los datos en su lugar, pase el puntero de búfer de texto no cifrado para los parámetros *pbInput* y *pbOutput* en la [**función BCryptEncrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) Es posible que el tamaño de los datos cifrados sea mayor que el tamaño de los datos sin cifrar, por lo que el búfer de texto no cifrado debe ser lo suficientemente grande como para contener los datos cifrados, no solo el texto no cifrado. Puede usar el tamaño obtenido en el paso 3 para asignar el búfer de texto no cifrado.

    Si desea cifrar los datos en un búfer independiente, asigne un búfer de memoria para los datos cifrados mediante el tamaño obtenido en el paso 3.

5.  Llame a [**la función BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) para cifrar los datos. Esta función escribirá los datos cifrados en la ubicación proporcionada en el *parámetro pbOutput.*
6.  Conserve los datos cifrados según sea necesario.
7.  Repita los pasos 5 y 6 hasta que se hayan cifrado todos los datos.

## <a name="encrypting-data-example"></a>Ejemplo de cifrado de datos

En el ejemplo siguiente se muestra cómo cifrar datos con CNG mediante el algoritmo de cifrado simétrico estándar de cifrado avanzado.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a>Descifrar datos

Para descifrar los datos, realice los pasos siguientes:

1.  Abra un proveedor de algoritmos que admita el cifrado, como **BCRYPT \_ DES \_ ALGORITHM**.
2.  Obtenga la clave con la que se cifraron los datos y use esa clave para obtener un identificador para la clave.
3.  Obtenga el tamaño de los datos descifrados. Esto se basa en el algoritmo de cifrado, el esquema de relleno (si existe) y el tamaño de los datos que se descifrarán. Puede obtener el tamaño de los datos cifrados mediante la [**función BCryptDecrypt,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) pasando **NULL** para el *parámetro pbOutput.* Los parámetros que especifican el esquema de relleno y el [*vector*](/windows/desktop/SecGloss/i-gly) de inicialización (IV) deben ser los mismos que cuando se cifraron los datos, excepto para el *parámetro pbInput,* que no se usa en este caso.
4.  Asigne un búfer de memoria para los datos descifrados.
5.  Puede descifrar los datos en su lugar mediante el mismo búfer o descifrar los datos en un búfer independiente.

    Si desea descifrar los datos en su lugar, pase el puntero de búfer de texto cifrado para los parámetros *pbInput* y *pbOutput* en la [**función BCryptDecrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)

    Si desea descifrar los datos en un búfer independiente, asigne un búfer de memoria para los datos descifrados mediante el tamaño obtenido en el paso 3.

6.  Llame a [**la función BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) para descifrar los datos. Los parámetros que especifican el esquema de relleno y el IV deben ser los mismos que cuando se cifraron los datos. Esta función escribirá los datos descifrados en la ubicación proporcionada en el *parámetro pbOutput.*
7.  Conserve los datos descifrados según sea necesario.
8.  Repita los pasos 5 y 6 hasta que se descifren todos los datos.

 

 

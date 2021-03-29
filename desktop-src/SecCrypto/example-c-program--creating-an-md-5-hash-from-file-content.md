---
description: 'Programa C de ejemplo: crear un hash MD5 a partir del contenido del archivo'
ms.assetid: 3186e292-87fd-425b-b9cf-92a294a57b69
title: 'Programa C de ejemplo: crear un hash MD5 a partir del contenido del archivo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea252a0afe41574e7636e163e20e024719c4617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002917"
---
# <a name="example-c-program-creating-an-md5-hash-from-file-content"></a><span data-ttu-id="c5dd6-103">Programa C de ejemplo: crear un hash MD5 a partir del contenido del archivo</span><span class="sxs-lookup"><span data-stu-id="c5dd6-103">Example C Program: Creating an MD5 Hash from File Content</span></span>

<span data-ttu-id="c5dd6-104">En el ejemplo siguiente se muestra cómo usar CryptoAPI para calcular el hash [*MD5*](../secgloss/m-gly.md) del contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c5dd6-104">The following example demonstrates using CryptoAPI to compute the [*MD5*](../secgloss/m-gly.md) hash of the contents of a file.</span></span> <span data-ttu-id="c5dd6-105">Este ejemplo realiza el cálculo en el contenido de un archivo especificado en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c5dd6-105">This example performs the computation on the contents of a file specified at run time.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

#define BUFSIZE 1024
#define MD5LEN  16

DWORD main()
{
    DWORD dwStatus = 0;
    BOOL bResult = FALSE;
    HCRYPTPROV hProv = 0;
    HCRYPTHASH hHash = 0;
    HANDLE hFile = NULL;
    BYTE rgbFile[BUFSIZE];
    DWORD cbRead = 0;
    BYTE rgbHash[MD5LEN];
    DWORD cbHash = 0;
    CHAR rgbDigits[] = "0123456789abcdef";
    LPCWSTR filename=L"filename.txt";
    // Logic to check usage goes here.

    hFile = CreateFile(filename,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        FILE_FLAG_SEQUENTIAL_SCAN,
        NULL);

    if (INVALID_HANDLE_VALUE == hFile)
    {
        dwStatus = GetLastError();
        printf("Error opening file %s\nError: %d\n", filename, 
            dwStatus); 
        return dwStatus;
    }

    // Get handle to the crypto provider
    if (!CryptAcquireContext(&hProv,
        NULL,
        NULL,
        PROV_RSA_FULL,
        CRYPT_VERIFYCONTEXT))
    {
        dwStatus = GetLastError();
        printf("CryptAcquireContext failed: %d\n", dwStatus); 
        CloseHandle(hFile);
        return dwStatus;
    }

    if (!CryptCreateHash(hProv, CALG_MD5, 0, 0, &hHash))
    {
        dwStatus = GetLastError();
        printf("CryptAcquireContext failed: %d\n", dwStatus); 
        CloseHandle(hFile);
        CryptReleaseContext(hProv, 0);
        return dwStatus;
    }

    while (bResult = ReadFile(hFile, rgbFile, BUFSIZE, 
        &cbRead, NULL))
    {
        if (0 == cbRead)
        {
            break;
        }

        if (!CryptHashData(hHash, rgbFile, cbRead, 0))
        {
            dwStatus = GetLastError();
            printf("CryptHashData failed: %d\n", dwStatus); 
            CryptReleaseContext(hProv, 0);
            CryptDestroyHash(hHash);
            CloseHandle(hFile);
            return dwStatus;
        }
    }

    if (!bResult)
    {
        dwStatus = GetLastError();
        printf("ReadFile failed: %d\n", dwStatus); 
        CryptReleaseContext(hProv, 0);
        CryptDestroyHash(hHash);
        CloseHandle(hFile);
        return dwStatus;
    }

    cbHash = MD5LEN;
    if (CryptGetHashParam(hHash, HP_HASHVAL, rgbHash, &cbHash, 0))
    {
        printf("MD5 hash of file %s is: ", filename);
        for (DWORD i = 0; i < cbHash; i++)
        {
            printf("%c%c", rgbDigits[rgbHash[i] >> 4],
                rgbDigits[rgbHash[i] & 0xf]);
        }
        printf("\n");
    }
    else
    {
        dwStatus = GetLastError();
        printf("CryptGetHashParam failed: %d\n", dwStatus); 
    }

    CryptDestroyHash(hHash);
    CryptReleaseContext(hProv, 0);
    CloseHandle(hFile);

    return dwStatus; 
}   
```



 

 

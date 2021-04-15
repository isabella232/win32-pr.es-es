---
description: En el ejemplo siguiente se muestra el descifrado de un archivo.
ms.assetid: be355b08-95c1-4ad3-bb05-6f646d5db5cd
title: 'Programa C de ejemplo: descifrado de un archivo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e65b7e33ba58a80fe87cc51a25912c66bf3589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648599"
---
# <a name="example-c-program-decrypting-a-file"></a><span data-ttu-id="5d33b-103">Programa C de ejemplo: descifrado de un archivo</span><span class="sxs-lookup"><span data-stu-id="5d33b-103">Example C Program: Decrypting a File</span></span>

<span data-ttu-id="5d33b-104">En el ejemplo siguiente se muestra el descifrado de un archivo.</span><span class="sxs-lookup"><span data-stu-id="5d33b-104">The following example shows the decryption of a file.</span></span> <span data-ttu-id="5d33b-105">En el ejemplo se pide al usuario el nombre de un archivo cifrado y el nombre de un archivo donde se escribirán los datos descifrados.</span><span class="sxs-lookup"><span data-stu-id="5d33b-105">The example asks the user for the name of an encrypted file and the name of a file where the decrypted data will be written.</span></span> <span data-ttu-id="5d33b-106">El archivo con los datos cifrados debe existir.</span><span class="sxs-lookup"><span data-stu-id="5d33b-106">The file with the encrypted data must exist.</span></span> <span data-ttu-id="5d33b-107">En el ejemplo se crea o se sobrescribe el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="5d33b-107">The example creates or overwrites the output file.</span></span>

<span data-ttu-id="5d33b-108">En el ejemplo también se solicita una cadena que se usa como contraseña.</span><span class="sxs-lookup"><span data-stu-id="5d33b-108">The example also requests a string that is used as a password.</span></span> <span data-ttu-id="5d33b-109">Si se usó una contraseña para crear la clave de sesión de cifrado, se debe especificar la misma contraseña para crear la clave de sesión de descifrado.</span><span class="sxs-lookup"><span data-stu-id="5d33b-109">If a password was used to create the encryption session key, that same password must be entered to create the decryption session key.</span></span> <span data-ttu-id="5d33b-110">Para obtener más información, vea [el ejemplo C programa: cifrar un archivo](example-c-program-encrypting-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="5d33b-110">For more information, see [Example C Program: Encrypting a File](example-c-program-encrypting-a-file.md).</span></span>

<span data-ttu-id="5d33b-111">Debido al cambio en las restricciones de control de exportación, el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la [*longitud de clave*](../secgloss/k-gly.md) predeterminada pueden cambiar entre las versiones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5d33b-111">Due to changing export control restrictions, the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and default [*key length*](../secgloss/k-gly.md) may change between operating system releases.</span></span> <span data-ttu-id="5d33b-112">Es importante que tanto el cifrado como el descifrado usen el mismo CSP y que la longitud de la clave se establezca explícitamente para garantizar la interoperabilidad en distintas plataformas de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5d33b-112">It is important that both the encryption and decryption use the same CSP and that the key length be explicitly set to ensure interoperability on different operating system platforms.</span></span>

<span data-ttu-id="5d33b-113">En este ejemplo se usa la función [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="5d33b-113">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="5d33b-114">El código de esta función se incluye con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d33b-114">The code for this function is included with the sample.</span></span> <span data-ttu-id="5d33b-115">El código de esta y otras funciones auxiliares también se enumeran en [funciones de de uso general](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5d33b-115">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
// Decrypting_a_File.cpp : Defines the entry point for the console 
// application.
//

#include <tchar.h>
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>
#include <conio.h>

// Link with the Advapi32.lib file.
#pragma comment (lib, "advapi32")

#define KEYLENGTH  0x00800000
#define ENCRYPT_ALGORITHM CALG_RC4 
#define ENCRYPT_BLOCK_SIZE 8 

bool MyDecryptFile(
    LPTSTR szSource, 
    LPTSTR szDestination, 
    LPTSTR szPassword);

void MyHandleError(
    LPTSTR psz, 
    int nErrorNumber);

int _tmain(int argc, _TCHAR* argv[])
{
    if(argc < 3)
    {
        _tprintf(TEXT("Usage: <example.exe> <source file> ")
            TEXT("<destination file> | <password>\n"));
        _tprintf(TEXT("<password> is optional.\n"));
        _tprintf(TEXT("Press any key to exit."));
        _gettch();
        return 1;
    }

    LPTSTR pszSource = argv[1]; 
    LPTSTR pszDestination = argv[2]; 
    LPTSTR pszPassword = NULL;

    if(argc >= 4)
    {
        pszPassword = argv[3];
    }

    //---------------------------------------------------------------
    // Call EncryptFile to do the actual encryption.
    if(MyDecryptFile(pszSource, pszDestination, pszPassword))
    {
        _tprintf(
            TEXT("Encryption of the file %s was successful. \n"), 
            pszSource);
        _tprintf(
            TEXT("The encrypted data is in file %s.\n"), 
            pszDestination);
    }
    else
    {
        MyHandleError(
            TEXT("Error encrypting file!\n"), 
            GetLastError()); 
    }

    return 0;
}

//-------------------------------------------------------------------
// Code for the function MyDecryptFile called by main.
//-------------------------------------------------------------------
// Parameters passed are:
//  pszSource, the name of the input file, an encrypted file.
//  pszDestination, the name of the output, a plaintext file to be 
//   created.
//  pszPassword, either NULL if a password is not to be used or the 
//   string that is the password.
bool MyDecryptFile(
    LPTSTR pszSourceFile, 
    LPTSTR pszDestinationFile, 
    LPTSTR pszPassword)
{ 
    //---------------------------------------------------------------
    // Declare and initialize local variables.
    bool fReturn = false;
    HANDLE hSourceFile = INVALID_HANDLE_VALUE;
    HANDLE hDestinationFile = INVALID_HANDLE_VALUE; 
    HCRYPTKEY hKey = NULL; 
    HCRYPTHASH hHash = NULL; 

    HCRYPTPROV hCryptProv = NULL; 

    DWORD dwCount;
    PBYTE pbBuffer = NULL; 
    DWORD dwBlockLen; 
    DWORD dwBufferLen; 

    //---------------------------------------------------------------
    // Open the source file. 
    hSourceFile = CreateFile(
        pszSourceFile, 
        FILE_READ_DATA,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        FILE_ATTRIBUTE_NORMAL,
        NULL);
    if(INVALID_HANDLE_VALUE != hSourceFile)
    {
        _tprintf(
            TEXT("The source encrypted file, %s, is open. \n"), 
            pszSourceFile);
    }
    else
    { 
        MyHandleError(
            TEXT("Error opening source plaintext file!\n"), 
            GetLastError());
        goto Exit_MyDecryptFile;
    } 

    //---------------------------------------------------------------
    // Open the destination file. 
    hDestinationFile = CreateFile(
        pszDestinationFile, 
        FILE_WRITE_DATA,
        FILE_SHARE_READ,
        NULL,
        OPEN_ALWAYS,
        FILE_ATTRIBUTE_NORMAL,
        NULL);
    if(INVALID_HANDLE_VALUE != hDestinationFile)
    {
         _tprintf(
             TEXT("The destination file, %s, is open. \n"), 
             pszDestinationFile);
    }
    else
    {
        MyHandleError(
            TEXT("Error opening destination file!\n"), 
            GetLastError()); 
        goto Exit_MyDecryptFile;
    }

    //---------------------------------------------------------------
    // Get the handle to the default provider. 
    if(CryptAcquireContext(
        &hCryptProv, 
        NULL, 
        MS_ENHANCED_PROV, 
        PROV_RSA_FULL, 
        0))
    {
        _tprintf(
            TEXT("A cryptographic provider has been acquired. \n"));
    }
    else
    {
        MyHandleError(
            TEXT("Error during CryptAcquireContext!\n"), 
            GetLastError());
        goto Exit_MyDecryptFile;
    }

    //---------------------------------------------------------------
    // Create the session key.
    if(!pszPassword || !pszPassword[0]) 
    { 
        //-----------------------------------------------------------
        // Decrypt the file with the saved session key. 

        DWORD dwKeyBlobLen;
        PBYTE pbKeyBlob = NULL;

        // Read the key BLOB length from the source file. 
        if(!ReadFile(
            hSourceFile, 
            &dwKeyBlobLen, 
            sizeof(DWORD), 
            &dwCount, 
            NULL))
        {
            MyHandleError(
                TEXT("Error reading key BLOB length!\n"), 
                GetLastError());
            goto Exit_MyDecryptFile;
        }

        // Allocate a buffer for the key BLOB.
        if(!(pbKeyBlob = (PBYTE)malloc(dwKeyBlobLen)))
        {
            MyHandleError(
                TEXT("Memory allocation error.\n"), 
                E_OUTOFMEMORY); 
        }

        //-----------------------------------------------------------
        // Read the key BLOB from the source file. 
        if(!ReadFile(
            hSourceFile, 
            pbKeyBlob, 
            dwKeyBlobLen, 
            &dwCount, 
            NULL))
        {
            MyHandleError(
                TEXT("Error reading key BLOB length!\n"), 
                GetLastError());
            goto Exit_MyDecryptFile;
        }

        //-----------------------------------------------------------
        // Import the key BLOB into the CSP. 
        if(!CryptImportKey(
              hCryptProv, 
              pbKeyBlob, 
              dwKeyBlobLen, 
              0, 
              0, 
              &hKey))
        {
            MyHandleError(
                TEXT("Error during CryptImportKey!/n"), 
                GetLastError()); 
            goto Exit_MyDecryptFile;
        }

        if(pbKeyBlob)
        {
            free(pbKeyBlob);
        }
    }
    else
    {
        //-----------------------------------------------------------
        // Decrypt the file with a session key derived from a 
        // password. 

        //-----------------------------------------------------------
        // Create a hash object. 
        if(!CryptCreateHash(
               hCryptProv, 
               CALG_MD5, 
               0, 
               0, 
               &hHash))
        {
            MyHandleError(
                TEXT("Error during CryptCreateHash!\n"), 
                GetLastError());
            goto Exit_MyDecryptFile;
        }
        
        //-----------------------------------------------------------
        // Hash in the password data. 
        if(!CryptHashData(
               hHash, 
               (BYTE *)pszPassword, 
               lstrlen(pszPassword), 
               0)) 
        {
            MyHandleError(
                TEXT("Error during CryptHashData!\n"), 
                GetLastError()); 
            goto Exit_MyDecryptFile;
        }
    
        //-----------------------------------------------------------
        // Derive a session key from the hash object. 
        if(!CryptDeriveKey(
              hCryptProv, 
              ENCRYPT_ALGORITHM, 
              hHash, 
              KEYLENGTH, 
              &hKey))
        { 
            MyHandleError(
                TEXT("Error during CryptDeriveKey!\n"), 
                GetLastError()) ; 
            goto Exit_MyDecryptFile;
        }
    }

    //---------------------------------------------------------------
    // The decryption key is now available, either having been 
    // imported from a BLOB read in from the source file or having 
    // been created by using the password. This point in the program 
    // is not reached if the decryption key is not available.
     
    //---------------------------------------------------------------
    // Determine the number of bytes to decrypt at a time. 
    // This must be a multiple of ENCRYPT_BLOCK_SIZE. 

    dwBlockLen = 1000 - 1000 % ENCRYPT_BLOCK_SIZE; 
    dwBufferLen = dwBlockLen; 

    //---------------------------------------------------------------
    // Allocate memory for the file read buffer. 
    if(!(pbBuffer = (PBYTE)malloc(dwBufferLen)))
    {
       MyHandleError(TEXT("Out of memory!\n"), E_OUTOFMEMORY); 
       goto Exit_MyDecryptFile;
    }
    
    //---------------------------------------------------------------
    // Decrypt the source file, and write to the destination file. 
    bool fEOF = false;
    do
    {
        //-----------------------------------------------------------
        // Read up to dwBlockLen bytes from the source file. 
        if(!ReadFile(
            hSourceFile, 
            pbBuffer, 
            dwBlockLen, 
            &dwCount, 
            NULL))
        {
            MyHandleError(
                TEXT("Error reading from source file!\n"), 
                GetLastError());
            goto Exit_MyDecryptFile;
        }

        if(dwCount < dwBlockLen)
        {
            fEOF = TRUE;
        }

        //-----------------------------------------------------------
        // Decrypt the block of data. 
        if(!CryptDecrypt(
              hKey, 
              0, 
              fEOF, 
              0, 
              pbBuffer, 
              &dwCount))
        {
            MyHandleError(
                TEXT("Error during CryptDecrypt!\n"), 
                GetLastError()); 
            goto Exit_MyDecryptFile;
        }

        //-----------------------------------------------------------
        // Write the decrypted data to the destination file. 
        if(!WriteFile(
            hDestinationFile, 
            pbBuffer, 
            dwCount,
            &dwCount,
            NULL))
        { 
            MyHandleError(
                TEXT("Error writing ciphertext.\n"), 
                GetLastError());
            goto Exit_MyDecryptFile;
        }

        //-----------------------------------------------------------
        // End the do loop when the last block of the source file 
        // has been read, encrypted, and written to the destination 
        // file.
    }while(!fEOF);

    fReturn = true;

Exit_MyDecryptFile:

    //---------------------------------------------------------------
    // Free the file read buffer.
    if(pbBuffer)
    {
        free(pbBuffer);
    }

    //---------------------------------------------------------------
    // Close files.
    if(hSourceFile)
    {
        CloseHandle(hSourceFile);
    }

    if(hDestinationFile)
    {
        CloseHandle(hDestinationFile);
    }

    //-----------------------------------------------------------
    // Release the hash object. 
    if(hHash) 
    {
        if(!(CryptDestroyHash(hHash)))
        {
            MyHandleError(
                TEXT("Error during CryptDestroyHash.\n"), 
                GetLastError()); 
        }

        hHash = NULL;
    }

    //---------------------------------------------------------------
    // Release the session key. 
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(
                TEXT("Error during CryptDestroyKey!\n"), 
                GetLastError());
        }
    } 

    //---------------------------------------------------------------
    // Release the provider handle. 
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv, 0)))
        {
            MyHandleError(
                TEXT("Error during CryptReleaseContext!\n"), 
                GetLastError());
        }
    } 

    return fReturn;
}


//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the  
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(LPTSTR psz, int nErrorNumber)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), nErrorNumber);
}

```



 

 

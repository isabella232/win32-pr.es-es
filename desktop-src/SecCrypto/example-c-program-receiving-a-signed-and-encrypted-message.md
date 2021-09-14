---
description: 'El ejemplo siguiente funciona junto con el programa en El programa de ejemplo C: Envío y recepción de un mensaje firmado y cifrado. Lee el mensaje firmado y cifrado y, a continuación, descifra y comprueba el mensaje.'
ms.assetid: 65ca30ba-a184-46ef-808c-e2fedcc86079
title: 'Programa C de ejemplo: recepción de un mensaje firmado y cifrado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1d97b50eb401568ebf1732f347f800eed0c26f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171074"
---
# <a name="example-c-program-receiving-a-signed-and-encrypted-message"></a>Programa C de ejemplo: recepción de un mensaje firmado y cifrado

El ejemplo siguiente funciona junto con el programa en El programa [de ejemplo C: Enviar y recibir un mensaje firmado y cifrado](example-c-program-sending-and-receiving-a-signed-and-encrypted-message.md). Lee el mensaje firmado y cifrado y, a continuación, descifra y comprueba el mensaje.

Para descifrar y comprobar el mensaje, la [*clave privada*](../secgloss/p-gly.md) del receptor previsto del mensaje debe estar disponible. El certificado del firmante se incluye en el blob del [*mensaje*](../secgloss/b-gly.md) leído desde el archivo.

En este ejemplo se muestran las tareas siguientes:

-   Abrir y cerrar almacenes de certificados del sistema.
-   Lectura de [**un BLOB DE NOMBRE DE \_ \_ CERTIFICADO**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) desde un archivo.
-   Inicializar las estructuras de datos necesarias para descifrar y comprobar un mensaje.
-   Llamar a una función CryptoAPI para encontrar el tamaño necesario de un búfer, asignar el búfer del tamaño necesario y llamar de nuevo a la función CryptoAPI para rellenar el búfer. Para obtener más información, [vea Recuperar datos de longitud desconocida.](retrieving-data-of-unknown-length.md)

En este ejemplo se usan las siguientes funciones de CryptoAPI:

-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature)
-   [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

En este ejemplo [**se usa MyHandleError**](myhandleerror.md) para salir correctamente del programa en caso de error. El código **MyHandleError se** incluye con el ejemplo y también se puede encontrar junto con otras funciones auxiliares en [De uso general Functions](general-purpose-functions.md).


```C++
//-------------------------------------------------------------------
// Example C Program: 
// Reads a signed and encrypted message, then decrypts and verifies 
// the message.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

BYTE* DecryptAndVerify(DWORD cbBlob, BYTE *pbBlob)
{
    //---------------------------------------------------------------
    //  Declare and initialize local variables.

    HCERTSTORE hCertStore;
    CRYPT_DECRYPT_MESSAGE_PARA DecryptPara;
    CRYPT_VERIFY_MESSAGE_PARA VerifyPara;
    DWORD dwSignerIndex = 0;
    BYTE *pbDecrypted;
    DWORD cbDecrypted;

    //---------------------------------------------------------------
    //   Open the certificate store.

    if ( !(hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    //   Initialize the needed data structures.

    DecryptPara.cbSize = sizeof(CRYPT_DECRYPT_MESSAGE_PARA);
    DecryptPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    DecryptPara.cCertStore = 1;
    DecryptPara.rghCertStore = &hCertStore;

    VerifyPara.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyPara.hCryptProv = 0;
    VerifyPara.pfnGetSignerCertificate = NULL;
    VerifyPara.pvGetArg = NULL;
    pbDecrypted = NULL;
    cbDecrypted = 0;

    //---------------------------------------------------------------
    //     Call CryptDecryptAndVerifyMessageSignature a first time
    //     to determine the needed size of the buffer to hold the 
    //     decrypted message. 
    //     Note: The sixth parameter is NULL in this call to 
    //     get the required size of the bytes string to contain the 
    //     decrypted message.

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbBlob,
        cbBlob,
        NULL,           
        &cbDecrypted,
        NULL,
        NULL)))
    {
        MyHandleError(TEXT("Failed getting size."));
    }

    //---------------------------------------------------------------
    //    Allocate memory for the buffer to hold the decrypted
    //    message.

    if(!(pbDecrypted = (BYTE *)malloc(cbDecrypted)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbBlob,
        cbBlob,
        pbDecrypted,
        &cbDecrypted,
        NULL,
        NULL)))
    {
        pbDecrypted = NULL;
    }

    //---------------------------------------------------------------
    //  Close the certificate store.

    CertCloseStore(hCertStore, 0);

    //---------------------------------------------------------------
    //    Return the decrypted string or NULL.

    return pbDecrypted;

} // End of DecryptandVerify.

BYTE* ReadBlob(DWORD *pcbBlob)
{
    FILE *hInputFile;
    BYTE *pbBlob;

    // Open the input file and read in the signed and encrypted BLOB.
    // This file would be created by a program such as the example 
    // program "Example C Program: Sending and Receiving a Signed and 
    // Encrypted Message" in the Platform Software Development Kit (SDK).
    // Change the path name for this file if it is not in the same
    // directory as the executable.

    if( !(hInputFile= _tfopen(TEXT("sandvout.txt"), TEXT("rb"))))
    {
        MyHandleError(TEXT("Input file was not opened.\n"));
    }

    fread(
        pcbBlob,
        sizeof(DWORD),
        1,
        hInputFile);

    if(ferror(hInputFile))
    {
        MyHandleError(TEXT("The size of the BLOB was not read.\n"));
    }

    if(!(pbBlob = (BYTE *) malloc(*pcbBlob)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    fread(
        pbBlob,
        *pcbBlob,
        1,
        hInputFile);

    if(ferror(hInputFile))
    {
        MyHandleError(TEXT("The bytes of the BLOB were not read.\n"));
    }

    fclose(hInputFile);

    return pbBlob;
}  // End of ReadBlob.

//-------------------------------------------------------------------
//   Main calls ReadBlob to read in the signed and encrypted message.
//   It then calls DecryptAndVerify which, if successful, decrypts
//   and verifies the message. 
//   The function main prints the returned, decrypted message
//   if the verification and decryption are successful.

//   Note: The file with the signed and encrypted file must be
//   available, and the user running this program must have access to
//   the private key of the intended message receiver.

//   Also note that this program does not use CryptAcquireContext.
   
void main()
{
    BYTE *pReturnMessage;
    BYTE *pbBlob;
    DWORD cbBlob;

    if((pbBlob = ReadBlob(&cbBlob)) == NULL)
    {
        MyHandleError(TEXT("Read BLOB did not return the BLOB. "));
    }

    if(pReturnMessage = DecryptAndVerify(cbBlob, pbBlob))
    {
        _tprintf(TEXT
                ("    The returned, verified message is ->\n%s\n"), 
            pReturnMessage);
        _tprintf(TEXT("    The program executed without error.\n"));
    }
    else
    {
        _tprintf(TEXT("Verification failed.\n"));
    }

} // End of main.


```



 

 

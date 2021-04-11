---
description: En el ejemplo siguiente se muestra cómo crear una clave criptográfica de sesión a partir del hash de una contraseña, así como el uso de la función CryptDeriveKey y las funciones relacionadas.
ms.assetid: f4748725-2a47-487c-b18c-7b27112d1090
title: 'Programa C de ejemplo: derivar una clave de sesión de una contraseña'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46884fa40a3a5682ca21229048004314bf03609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278806"
---
# <a name="example-c-program-deriving-a-session-key-from-a-password"></a>Programa C de ejemplo: derivar una clave de sesión de una contraseña

En el ejemplo siguiente se muestra cómo crear una [*clave criptográfica de sesión*](../secgloss/s-gly.md) a partir del [*hash*](../secgloss/h-gly.md) de una contraseña, así como el uso de la función [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) y las funciones relacionadas.

En este ejemplo se muestran las siguientes tareas y funciones de CryptoAPI:

-   Llamar a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para adquirir un identificador para el CSP predeterminado y el [*contenedor de claves*](../secgloss/k-gly.md)predeterminado.
-   Usar [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) para crear un objeto hash vacío.
-   Aplicar un algoritmo hash al texto de una contraseña mediante [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).
-   Derivar una clave de sesión de la contraseña con hash mediante [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).
-   Destruir el hash y la contraseña.
-   Uso de [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) para liberar el CSP.

En este ejemplo se usa la función [**MyHandleError**](myhandleerror.md). El código de esta función se incluye con el ejemplo.

El código de esta y otras funciones auxiliares también se enumeran en [funciones de de uso general](general-purpose-functions.md).


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void GetConsoleInput(char*, UINT);
#define PASSWORD_LENGTH 512

void main()
{
    //----------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.

    HCRYPTPROV hCryptProv;
    HCRYPTKEY hKey;
    HCRYPTHASH hHash;
    CHAR szPassword[PASSWORD_LENGTH] = "";
    DWORD dwLength;

    //----------------------------------------------------------------
    // Get the password from the user.

    fprintf(stderr,"Enter a password to be used to create a key:");

    // Get a password while printing only asterisks to the screen.
    GetConsoleInput(szPassword, PASSWORD_LENGTH);
    printf("The password has been stored.\n");
    dwLength = (DWORD) strlen(szPassword);

    //----------------------------------------------------------------
    // Acquire a cryptographic provider context handle.

    if(CryptAcquireContext(
       &hCryptProv,
       NULL,
       NULL,
       PROV_RSA_FULL,
       0))
    {
        printf("A context has been acquired. \n");
    }
    else
    {
         MyHandleError("Error during CryptAcquireContext!");
    }
    //----------------------------------------------------------------
    // Create an empty hash object.

    if(CryptCreateHash(
       hCryptProv,
       CALG_MD5,
       0,
       0,
       &hHash))
    {
        printf("An empty hash object has been created. \n");
    }
    else
    {
        MyHandleError("Error during CryptCreateHash!");
    }
    //----------------------------------------------------------------
    // Hash the password string.

    if(CryptHashData(
       hHash,
       (BYTE *)szPassword,
       dwLength,
       0))
    {
         printf("The password has been hashed. \n");
    }
    else
    {
         MyHandleError("Error during CryptHashData!");
    }
    //----------------------------------------------------------------
    // Create a session key based on the hash of the password.

    if(CryptDeriveKey(
       hCryptProv,
       CALG_RC2,
       hHash,
       CRYPT_EXPORTABLE,
       &hKey))
    {
        printf("The key has been derived. \n");
    }
    else
    {
        MyHandleError("Error during CryptDeriveKey!");
    }
    //----------------------------------------------------------------
    // Use hKey as appropriate to encrypt or decrypt a message.

    //----------------------------------------------------------------
    // Clean up.

    // Destroy the hash object.

    if(hHash)
    {
       if(!(CryptDestroyHash(hHash)))
           MyHandleError("Error during CryptDestroyHash");
    }

    // Destroy the session key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
            MyHandleError("Error during CryptDestroyKey");
    }

    // Release the provider handle.
    if(hCryptProv)
    {
       if(!(CryptReleaseContext(hCryptProv, 0)))
           MyHandleError("Error during CryptReleaseContext");
    }
    printf("The program to derive a key completed without error. \n");
} // end main

//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}

//--------------------------------------------------------------------
// The GetConsoleInput function gets an array of characters from the
// keyboard, while printing only asterisks to the screen.

void GetConsoleInput(char* strInput,
                    UINT  intMaxChars)
{
    char ch;
    char minChar = ' ';
    minChar++;

    ch = (char)_getch();
    while (ch != '\r')
    {
        if (ch == '\b' && strlen(strInput) > 0)
        {
            strInput[strlen(strInput)-1]   = '\0';
            printf("\b \b");
        }
        else if ((ch >= minChar) && (strlen(strInput) < intMaxChars))
        {
            strInput[strlen(strInput)+1] = '\0';
            strInput[strlen(strInput)]   = ch;
            _putch('*');
        }
        ch = (char)_getch();
    }
    _putch('\n');
}

```



 

 

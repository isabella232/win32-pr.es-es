---
description: Enumera los certificados de un almacén de certificados, muestra el asunto y el usuario de cada certificado y convierte el nombre de sujeto de cada certificado en su forma codificada de notación de sintaxis abstracta uno (ASN. 1) y, a continuación, vuelve a su forma descodificada.
ms.assetid: 8b4771da-0996-40fb-98ce-73efe8e3534f
title: 'Programa C de ejemplo: convertir nombres de certificados en ASN. 1 y atrás'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14114d4ba956acabf26ff28368403c699497b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911598"
---
# <a name="example-c-program-converting-names-from-certificates-to-asn1-and-back"></a><span data-ttu-id="30aa9-103">Programa C de ejemplo: convertir nombres de certificados en ASN. 1 y atrás</span><span class="sxs-lookup"><span data-stu-id="30aa9-103">Example C Program: Converting Names from Certificates to ASN.1 and Back</span></span>

<span data-ttu-id="30aa9-104">En el ejemplo siguiente se enumeran los certificados de un [*almacén de certificados*](../secgloss/c-gly.md), se muestra el asunto y el usuario de cada certificado y se convierte el nombre del sujeto de cada certificado en su forma codificada de [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1) y, a continuación, se vuelve a crear en su forma descodificada.</span><span class="sxs-lookup"><span data-stu-id="30aa9-104">The following example enumerates the certificates in a [*certificate store*](../secgloss/c-gly.md), displays the subject and user of each certificate, and converts the subject name from each certificate into its [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) encoded form, and then back in to its decoded form.</span></span>

<span data-ttu-id="30aa9-105">En este ejemplo se muestran las siguientes tareas y funciones de [*CryptoAPI*](../secgloss/c-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="30aa9-105">This example shows the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="30aa9-106">Apertura de un almacén del sistema mediante [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span><span class="sxs-lookup"><span data-stu-id="30aa9-106">Opening a system store using [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span></span>
-   <span data-ttu-id="30aa9-107">Uso de [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore) para obtener el primer certificado del almacén abierto.</span><span class="sxs-lookup"><span data-stu-id="30aa9-107">Using [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore) to get the first certificate from the open store.</span></span>
-   <span data-ttu-id="30aa9-108">Usar [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) para obtener el nombre de sujeto y el nombre de usuario del certificado.</span><span class="sxs-lookup"><span data-stu-id="30aa9-108">Using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) to get the subject name and the user name from the certificate.</span></span>
-   <span data-ttu-id="30aa9-109">Usar [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) para convertir el nombre de sujeto del certificado en su forma de codificación ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="30aa9-109">Using [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) to convert the subject name from the certificate into its ASN.1 encoded form.</span></span>
-   <span data-ttu-id="30aa9-110">Usar [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea) para convertir una cadena codificada ASN. 1 en su forma descodificada.</span><span class="sxs-lookup"><span data-stu-id="30aa9-110">Using [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea) to convert an ASN.1 encoded string into its decoded form.</span></span>
-   <span data-ttu-id="30aa9-111">Cierre de un almacén de certificados con [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) con la marca de marca de comprobación del **\_ \_ almacén de \_ \_ cierre** de certificado.</span><span class="sxs-lookup"><span data-stu-id="30aa9-111">Closing a certificate store using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) with the **CERT\_CLOSE\_STORE\_CHECK\_FLAG** flag.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")



//-------------------------------------------------------------------
// Example C Program: 
// Converting a name from a certificate to an ASN.1 encoded string
// and back.

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MY_STRING_TYPE (CERT_OID_NAME_STR)

//-------------------------------------------------------------------
// Declare auxiliary functions

void MyHandleError(LPTSTR);
void Local_wait();

void main(void)
{
    HCERTSTORE hCertStore;
    PCCERT_CONTEXT pCertContext;

    //---------------------------------------------------------------
    // Begin Processing by opening a certificate store.

    if(!(hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        MY_ENCODING_TYPE,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"MY")))
    {
        MyHandleError(TEXT("The MY system store did not open."));
    }

    //---------------------------------------------------------------
    //       Loop through the certificates in the store. 
    //       For each certificate,
    //             get and print the name of the 
    //                  certificate subject and issuer.
    //             convert the subject name from the certificate
    //                  to an ASN.1 encoded string and print the
    //                  octets from that string.
    //             convert the encoded string back into its form 
    //                  in the certificate.

    pCertContext = NULL;
    while(pCertContext = CertEnumCertificatesInStore(
        hCertStore,
        pCertContext))
    {
        LPTSTR pszString;
        LPTSTR pszName;
        DWORD cbSize;
        CERT_BLOB blobEncodedName;

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of subject of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            0,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(
            pCertContext,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszName,
            cbSize))

        {
            _tprintf(TEXT("\nSubject -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //        Get and display 
        //        the name of Issuer of the certificate.

        if(!(cbSize = CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            NULL,   
            0)))
        {
            MyHandleError(TEXT("CertGetName 1 failed."));
        }

        if(!(pszName = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        if(CertGetNameString(   
            pCertContext,   
            CERT_NAME_SIMPLE_DISPLAY_TYPE,   
            CERT_NAME_ISSUER_FLAG,
            NULL,   
            pszName,   
            cbSize))
        {
            _tprintf(TEXT("Issuer  -> %s.\n"), pszName);

            //-------------------------------------------------------
            //       Free the memory allocated for the string.
            free(pszName);
        }
        else
        {
            MyHandleError(TEXT("CertGetName failed."));
        }

        //-----------------------------------------------------------
        //       Convert the subject name to an ASN.1 encoded
        //       string and print the octets in that string.

        //       First : Get the number of bytes that must 
        //       be allocated for the string.

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            NULL,
            0);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes needed for a string to hold the
        //  converted name, including the null terminator. 
        //  If it returns one, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //        Allocated the needed buffer. Note that this
        //        memory must be freed inside the loop or the 
        //        application will leak memory.

        if(!(pszString = (LPTSTR)malloc(cbSize * sizeof(TCHAR))))
        {
            MyHandleError(TEXT("Memory allocation failed."));
        }

        //-----------------------------------------------------------
        //       Call the function again to get the string. 

        cbSize = CertNameToStr(
            pCertContext->dwCertEncodingType,
            &(pCertContext->pCertInfo->Subject),
            MY_STRING_TYPE,
            pszString,
            cbSize);

        //-----------------------------------------------------------
        //  The function CertNameToStr returns the number
        //  of bytes in the string, including the null terminator.
        //  If it returns 1, the name is an empty string.

        if (1 == cbSize)
        {
            MyHandleError(TEXT("Subject name is an empty string."));
        }

        //-----------------------------------------------------------
        //    Get the length needed to convert the string back 
        //    back into the name as it was in the certificate.

        if(!(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            NULL,        // NULL to get the number of bytes 
                            // needed for the buffer.          
            &cbSize,     // Pointer to a DWORD to hold the 
                            // number of bytes needed for the 
                            // buffer
            NULL )))     // Optional address of a pointer to
                            // old the location for an error in the 
                            // input string.
        {
            MyHandleError(
                TEXT("Could not get the length of the BLOB."));
        }

        if (!(blobEncodedName.pbData = (LPBYTE)malloc(cbSize)))
        {
            MyHandleError(
                TEXT("Memory Allocation for the BLOB failed."));
        }
        blobEncodedName.cbData = cbSize;

        if(CertStrToName(
            MY_ENCODING_TYPE,
            pszString, 
            MY_STRING_TYPE,
            NULL,
            blobEncodedName.pbData,
            &blobEncodedName.cbData,
            NULL))
        {
            _tprintf(TEXT("CertStrToName created the BLOB.\n"));
        }
        else
        {
            MyHandleError(TEXT("Could not create the BLOB."));
        }

        //-----------------------------------------------------------
        //       Free the memory.

        free(blobEncodedName.pbData);
        free(pszString);

        //-----------------------------------------------------------
        //       Pause before information on the next certificate
        //       is displayed.

        Local_wait();

    } // End of while loop
     
    _tprintf(
        TEXT("\nThere are no more certificates in the store. \n"));

    //---------------------------------------------------------------
    //   Close the MY store.

    if(CertCloseStore(
        hCertStore,
        CERT_CLOSE_STORE_CHECK_FLAG))
    {
        _tprintf(TEXT("The store is closed. ")
            TEXT("All certificates are released.\n"));
    }
    else
    {
        _tprintf(TEXT("The store was closed, ")
            TEXT("but certificates still in use.\n"));
    }

    _tprintf(TEXT("This demonstration program ran to completion ")
        TEXT("without error.\n"));

    Local_wait();

} // End of main

//-------------------------------------------------------------------
//    This example uses the function MyHandleError, a simple error
//    handling function, to print an error message to the standard  
//    error (stderr) file and exit the program. 
//    For most applications, replace this function with one 
//    that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr,
        TEXT("An error occurred in running the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

void Local_wait()
{
//-------------------------------------------------------------------
//  This function prints a prompt string 
//  and wait for the user to hit enter.
//  It provides a pause with its length controlled by the user.

     _tprintf(TEXT("Hit Enter to continue : "));
     getchar();
}
```



 

 

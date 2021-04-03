---
description: En el ejemplo siguiente se muestra cómo serializar un contexto de certificado y sus propiedades en un formulario que se puede almacenar en un archivo, enviar con un mensaje de correo electrónico o transmitir de otro modo a otro usuario.
ms.assetid: cda7fa68-debe-40e6-8c4a-536dacccc2d1
title: 'Programa C de ejemplo: serialización de certificados'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efee0269a587e659605d375472f6e0ba16673d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082994"
---
# <a name="example-c-program-serializing-certificates"></a>Programa C de ejemplo: serialización de certificados

En el ejemplo siguiente se muestra cómo serializar un [*contexto de certificado*](../secgloss/c-gly.md) y sus propiedades en un formulario que se puede almacenar en un archivo, enviar con un mensaje de correo electrónico o transmitir de otro modo a otro usuario. En el ejemplo también se muestra cómo se puede volver a cambiar el certificado serializado a un certificado y se agrega a un almacén de certificados. El mismo proceso también funciona con las [*CRL*](../secgloss/c-gly.md) y las [*CTL*](../secgloss/c-gly.md) mediante [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) y [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement).

En este ejemplo se muestran las siguientes tareas y funciones de CryptoAPI:

-   Apertura de un almacén de certificados del sistema mediante [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Apertura de un almacén de certificados con [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
-   Recuperar un certificado de un almacén mediante [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).
-   Obtener el nombre del sujeto del certificado mediante [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   Crear un formulario serializado de un [*contexto de certificado*](../secgloss/c-gly.md) y sus propiedades mediante [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement).
-   Crear un nuevo certificado a partir de una cadena serializada y agregarlo a un almacén de certificados mediante [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore).
-   El uso de [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore) para crear un nuevo certificado a partir de la parte codificada de un certificado existente.
-   Usar [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) para cerrar un almacén de certificados.


```C++
//------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example that uses CertSerializeCertificateStoreElement to
// serialize the data from a certificate, 
// and CertAddSerializedElementToStore to add that data as a new
// certificate to a store.
// CertAddEncodeCertificateToStore is also demonstrated.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE         hSystemStore;
HCERTSTORE         hFileStore;
PCCERT_CONTEXT     pCertContext = NULL;
char               pszNameString[256]; 
BYTE*              pbElement;
DWORD              cbElement;

//-------------------------------------------------------------------
// Open a system certificate store.

if(hSystemStore = CertOpenSystemStore(
    0,
    "CA"))
{
  printf("The CA system store is open. Continue.\n");
}
else
{
  MyHandleError("The first system store did not open.");
}
//-------------------------------------------------------------------
// Open a second store.
// In order to work, a file-based certificate store named 
// teststor.sto must be available in the working directory.

if(hFileStore = CertOpenStore(
   CERT_STORE_PROV_FILENAME,
   MY_ENCODING_TYPE,
   NULL,
   0,
   L"testStor.sto" ))
{
     printf("The file store is open. Continue.\n");
}
else
{
     MyHandleError("The file store did not open.");
}
//-------------------------------------------------------------------
// Retrieve the first certificate from the Root store.
// CertFindCertificateInStore could be used here to find
// a certificate with a specific property.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("A certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate available. "
         "The store may be empty.");
}
//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
// Find out how much memory to allocate for the serialized element.

if(CertSerializeCertificateStoreElement(
    pCertContext,      // The existing certificate.
    0,                 // Accept default for dwFlags, 
    NULL,              // NULL for the first function call.
    &cbElement))       // Address where the length of the 
                       // serialized element will be placed.
{
     printf("The length of the serialized string is %d.\n",
         cbElement);
}
else
{
     MyHandleError("Finding the length of the serialized "
         "element failed.");
}
//-------------------------------------------------------------------
// Allocate memory for the serialized element.

if(pbElement = (BYTE*)malloc(cbElement))
{
     printf("Memory has been allocated. Continue.\n");
}
else
{
     MyHandleError("The allocation of memory failed.");
}
//-------------------------------------------------------------------
// Create the serialized element from a certificate context.

if(CertSerializeCertificateStoreElement(
    pCertContext,        // The certificate context source for the 
                         // serialized element.
    0,                   // dwFlags. Accept the default.
    pbElement,           // A pointer to where the new element will
                         // be stored.
    &cbElement))         // The length of the serialized element,
{
     printf("The encoded element has been serialized. \n");
}
else
{
     MyHandleError("The element could not be serialized.");
}
//-------------------------------------------------------------------
//  pbElement could be written to a file or be sent by email
//  to another user. 
//  The following process uses the serialized 
//  pbElement and its length, cbElement, to 
//  add a new certificate to a store.

if(CertAddSerializedElementToStore(
    hFileStore,          // Store where certificate is to be added.
    pbElement,           // The serialized element for another
                         // certificate. 
    cbElement,           // The length of pbElement.  
    CERT_STORE_ADD_REPLACE_EXISTING,
                         // Flag to indicate what to do if a matching
                         // certificate is already in the store.
    0,                   // dwFlags. Accept the default.
    CERT_STORE_CERTIFICATE_CONTEXT_FLAG, 
    NULL,
    NULL
    ))
{
     printf("The new certificate is added to the second store.\n");
}
else
{
     MyHandleError("The new element was not added to a store.");
}
//-------------------------------------------------------------------
//  Next, another certificate will be retrieved from the system store
//  and its encoded part, pCertContext->pbCertEncoded, will be
//  used to create a new certificate to be added to the file store.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("Another certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate is available. "
         "The store may be empty.");
}

//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
//  Create a new certificate from the encoded portion of pCertContext
//  and add it to the file-based store.

if(CertAddEncodedCertificateToStore(
     hFileStore,
     MY_ENCODING_TYPE,
     pCertContext->pbCertEncoded,
     pCertContext->cbCertEncoded,
     CERT_STORE_ADD_USE_EXISTING,
     NULL))
{
     printf("Another certificate is added to the file store.\n");
}
else
{
     MyHandleError("The new certificate was not added to the "
         "file store.");
}
//-------------------------------------------------------------------
// Free memory.

free(pbElement);
CertCloseStore(hSystemStore,0);
CertCloseStore(hFileStore,0); 
printf("The program ran without error to the end.\n");

} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 

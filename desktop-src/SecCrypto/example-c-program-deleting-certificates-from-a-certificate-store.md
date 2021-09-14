---
description: En el ejemplo siguiente se enumeran los certificados de un almacén de certificados del sistema, en el que se muestra el nombre del firmantes de cada certificado y se permite al usuario elegir eliminar los certificados del almacén.
ms.assetid: 52a0287b-7d2a-483e-8bbc-43621c4b7103
title: 'Programa C de ejemplo: Eliminación de certificados de un almacén de certificados'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29f55d27bf2a85d82e4ab96e51fe5368c9de935
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171133"
---
# <a name="example-c-program-deleting-certificates-from-a-certificate-store"></a>Programa C de ejemplo: Eliminación de certificados de un almacén de certificados

En el ejemplo siguiente se enumeran los certificados de un almacén de certificados del [*sistema,*](../secgloss/c-gly.md)que muestran el nombre del firmantes de cada certificado y permite al usuario elegir eliminar los certificados del almacén. En el ejemplo se obtiene el nombre del almacén de certificados del usuario y, por tanto, se puede usar para mantener el contenido de cualquier almacén de certificados del sistema.

En este ejemplo se muestran las siguientes tareas y [*funciones cryptoAPI:*](../secgloss/c-gly.md)

-   Abrir un almacén de certificados del sistema [**mediante CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Enumerar los certificados de un almacén de certificados [**mediante CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).
-   Obtener el nombre del sujeto de un certificado mediante [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   Comparar el nombre del firmante del certificado con el nombre del emisor del certificado mediante [**CertCompareCertificateName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename).
-   Comprobación para determinar si la clave pública del certificado actual coincide con la clave pública de un certificado anterior mediante [**CertComparePublicKeyInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo).
-   Duplicar un puntero a un [*contexto de certificado*](../secgloss/c-gly.md) mediante [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext).
-   Comparar los [**miembros \_ de CERT INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) de cada certificado mediante [**CertCompareCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate).
-   Eliminar un certificado de un almacén mediante [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore).
-   Cierre de un almacén de certificados [**mediante CertCloseStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

En este ejemplo se obtiene el nombre de un almacén de certificados del sistema del usuario, se abre ese almacén y se pasa por los certificados de ese almacén. Para cada certificado, se muestra el nombre del sujeto del certificado y se ofrece al usuario una opción para eliminar ese certificado.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HANDLE          hStoreHandle;
PCCERT_CONTEXT  pCertContext=NULL;   
PCCERT_CONTEXT  pDupCertContext; 
PCERT_PUBLIC_KEY_INFO pOldPubKey = NULL;
PCERT_PUBLIC_KEY_INFO pNewPubKey; 
char pszStoreName[256];
char pszNameString[256];
char fResponse ='n';  
char x;

//-------------------------------------------------------------------
// Get the name of the certificate store to open. 
printf("This program maintains the contents of a certificate\n");
printf("store by allowing you to delete any excess certificates\n");
printf("from a store. \n\n");
printf("Please enter the name of the system store to maintain:");
fgets(pszStoreName, 255, stdin);
if (pszStoreName[strlen(pszStoreName) - 1] =='\n')
   pszStoreName[strlen(pszStoreName) - 1] = '\0';
printf("Certificates will be deleted from "
       "the %s store.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hStoreHandle = CertOpenSystemStore(
     NULL,     
     pszStoreName))
{
     printf("The %s store has been opened. \n", pszStoreName);
}
else
{
     MyHandleError("The store was not opened.");
}
//-------------------------------------------------------------------
// Find the certificates in the system store. 

while(pCertContext= CertEnumCertificatesInStore(
    hStoreHandle,
    pCertContext)) // on the first call to the function,
                   //  this parameter is NULL
                   // on all subsequent
                   //  calls, it is the last pointer returned by 
                   //  the function
{
//-------------------------------------------------------------------
// Get and display the name of the subject of the certificate.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
   printf("\nCertificate for %s \n",pszNameString);
}
else
{
   MyHandleError("CertGetName failed.");
}
//-------------------------------------------------------------------
// Check to determine whether the issuer 
// and the subject are the same.

if(CertCompareCertificateName(
   MY_ENCODING_TYPE,
   &(pCertContext->pCertInfo->Issuer),
   &(pCertContext->pCertInfo->Subject)))
{
     printf("The certificate subject and issuer are the same.\n");
}
else
{
     printf("The certificate subject and issuer "
         "are not the same.\n");
}
//--------------------------------------------------------------------
// Determine whether this certificate's public key matches 
// the public key of the last certificate.

pNewPubKey = &(pCertContext->pCertInfo->SubjectPublicKeyInfo);
if(pOldPubKey)
   if(CertComparePublicKeyInfo(
       MY_ENCODING_TYPE,
       pOldPubKey,
       pNewPubKey))
   {
       printf("The public keys are the same.\n");
   }
   else
   {
       printf("This certificate has a different public key.\n");
   }
//-------------------------------------------------------------------
// Reset the old key.

pOldPubKey = pNewPubKey;

//-------------------------------------------------------------------
// Determine whether this certificate is to be deleted. 

printf("Would you like to delete this certificate? (y/n) ");
fResponse = getchar();
if(fResponse == 'y')
{
   //----------------------------------------------------------------
   // Create a duplicate pointer to the certificate to be 
   // deleted. In this way, the original pointer is not freed 
   // when the certificate is deleted from the store 
   // and the enumeration of the certificates in the store can
   // continue. If the original pointer is used, after the 
   // certificate is deleted, the enumeration loop stops.

   if(pDupCertContext = CertDuplicateCertificateContext(
      pCertContext))
   {
       printf("A duplicate pointer was created. Continue. \n");
   }
   else
   {
        MyHandleError("Duplication of the certificate "
            "pointer failed.");
   }

//-------------------------------------------------------------------
// Compare the pCertInfo members of the two certificates 
// to determine whether they are identical.

if(CertCompareCertificate(
      X509_ASN_ENCODING,
      pDupCertContext->pCertInfo, 
      pCertContext->pCertInfo))
{
     printf("The two certificates are identical. \n");
}
else
{
     printf("The two certificates are not identical. \n");
}
//-------------------------------------------------------------------
// Delete the certificate.
   if(CertDeleteCertificateFromStore(
     pDupCertContext))   
   {
       printf("The certificate has been deleted. Continue. \n");
   }
   else
   {
      printf("The deletion of the certificate failed.\n");
   }
} // end if

//-------------------------------------------------------------------
// Clear the input buffer.

x = getchar();

} // end while

//-------------------------------------------------------------------
// Clean up.

CertCloseStore(
   hStoreHandle,
   0);
printf("The program ran to completion successfully. \n");
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 

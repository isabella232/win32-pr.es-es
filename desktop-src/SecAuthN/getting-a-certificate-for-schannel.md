---
description: En el ejemplo siguiente se muestran los pasos para obtener una estructura de contexto de certificado \_ que contenga un certificado; debe seleccionar un certificado y un almacén de certificados adecuados para la aplicación.
ms.assetid: 31d7a8bd-729f-4db7-8e22-25d14296c0c4
title: Obtener un certificado para Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf7f311ac31fe2ff033d4b57f7d04bd1f42424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652557"
---
# <a name="getting-a-certificate-for-schannel"></a>Obtener un certificado para Schannel

En el ejemplo siguiente se muestran los pasos para obtener una estructura de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado que contenga un certificado; debe seleccionar un certificado y un almacén de certificados adecuados para la aplicación.

En este ejemplo se muestra la apertura de un [*almacén de certificados*](/windows/desktop/SecGloss/c-gly) y la ubicación de un certificado que se pasará a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , por medio de la estructura de [**\_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) .


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "crypt32.lib")

#define MACHINE_NAME "example server"

PCCERT_CONTEXT getServerCertificate ()
{
  HCERTSTORE hMyCertStore = NULL;
  PCCERT_CONTEXT aCertContext = NULL;
  
  //-------------------------------------------------------
  // Open the My store, also called the personal store.
  // This call to CertOpenStore opens the Local_Machine My 
  // store as opposed to the Current_User's My store.

    hMyCertStore = CertOpenStore(CERT_STORE_PROV_SYSTEM,
                                 X509_ASN_ENCODING,
                                 0,
                                 CERT_SYSTEM_STORE_LOCAL_MACHINE,
                                 L"MY");

  if (hMyCertStore == NULL) 
  {
    printf("Error opening MY store for server.\n");
    goto cleanup;
  }
  //-------------------------------------------------------
  // Search for a certificate with some specified
  // string in it. This example attempts to find
  // a certificate with the string "example server" in
  // its subject string. Substitute an appropriate string
  // to find a certificate for a specific user.

  aCertContext = CertFindCertificateInStore(hMyCertStore, 
                  X509_ASN_ENCODING, 
                  0,
                  CERT_FIND_SUBJECT_STR_A,
                  MACHINE_NAME, // use appropriate subject name
                  NULL
  );
  
  if (aCertContext == NULL)
  {
    printf("Error retrieving server certificate.");
    goto cleanup;
  }
cleanup:
  if(hMyCertStore)
  {
      CertCloseStore(hMyCertStore,0);
  }
  return aCertContext;
}
```



 

 

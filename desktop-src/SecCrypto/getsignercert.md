---
description: La función GetSignerCert pasa por (enumera) los certificados de un almacén de certificados hasta que se encuentra un certificado con una clave de firma.
ms.assetid: a3279492-a154-418d-ab25-45ec458ad483
title: GetSignerCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beff3e220fc8f0c95992c4a14a3dc8b5f5d19fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003123"
---
# <a name="getsignercert"></a><span data-ttu-id="a63b2-103">GetSignerCert</span><span class="sxs-lookup"><span data-stu-id="a63b2-103">GetSignerCert</span></span>

<span data-ttu-id="a63b2-104">La función **GetSignerCert** pasa por (enumera) los certificados de un [*almacén de certificados*](../secgloss/c-gly.md) hasta que se encuentra un certificado con una clave de firma.</span><span class="sxs-lookup"><span data-stu-id="a63b2-104">The **GetSignerCert** function goes through (enumerates) the certificates in a [*certificate store*](../secgloss/c-gly.md) until a certificate with a signature key is found.</span></span> <span data-ttu-id="a63b2-105">Si se encuentra un certificado, se devuelve un puntero al certificado.</span><span class="sxs-lookup"><span data-stu-id="a63b2-105">If a certificate is found, a pointer to the certificate is returned.</span></span> <span data-ttu-id="a63b2-106">Este código muestra:</span><span class="sxs-lookup"><span data-stu-id="a63b2-106">This code demonstrates:</span></span>

-   <span data-ttu-id="a63b2-107">Buscar un certificado con una propiedad de certificado.</span><span class="sxs-lookup"><span data-stu-id="a63b2-107">Finding a certificate with a certificate property.</span></span>
-   <span data-ttu-id="a63b2-108">Comprobando la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a63b2-108">Checking that property.</span></span>
-   <span data-ttu-id="a63b2-109">Devolver un puntero al [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) donde se encontró el atributo.</span><span class="sxs-lookup"><span data-stu-id="a63b2-109">Returning a pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) where the attribute was found.</span></span>

<span data-ttu-id="a63b2-110">Este código usa un controlador de errores denominado **MyHandleError**.</span><span class="sxs-lookup"><span data-stu-id="a63b2-110">This code uses an error handler called **MyHandleError**.</span></span> <span data-ttu-id="a63b2-111">Para ver la implementación de este controlador de errores, vea el tema [**MyHandleError**](myhandleerror.md) .</span><span class="sxs-lookup"><span data-stu-id="a63b2-111">To view the implementation for this error handler, see the [**MyHandleError**](myhandleerror.md) topic.</span></span>


```C++
#include <windows.h>

PCCERT_CONTEXT GetSignerCert(
        HCERTSTORE hCertStore)
//--------------------------------------------------------------------
//   Parameter passed in:
//      hCertStore, the handle of the store to be searched.
{
//--------------------------------------------------------------------
//   Declare and initialize local variables.

PCCERT_CONTEXT       pCertContext = NULL;
BOOL                 fMore = TRUE;
DWORD                dwSize = NULL;
CRYPT_KEY_PROV_INFO* pKeyInfo = NULL;
DWORD                PropId = CERT_KEY_PROV_INFO_PROP_ID;

//--------------------------------------------------------------------
//  Find certificates in the store until the end of the store
//  is reached or a certificate with an AT_SIGNATURE key is found.

while(fMore && 
  (pCertContext= CertFindCertificateInStore(
     hCertStore,           // Handle of the store to be searched.
     0,                    // Encoding type. Not used for this search.
     0,                    // dwFindFlags. Special find criteria.
                           // Not used in this search.
     CERT_FIND_PROPERTY,   // Find type that determines the kind of 
                           // search to do. In this case, search for 
                           // certificates that have a specific 
                           // extended property.
     &PropId,              // pvFindPara. Gives the specific 
                           // value searched for, here the identifier 
                           // of an extended property.
     pCertContext)))       // pCertContext is NULL for the 
                           // first call to the function. 
                           // If the function is called
                           // in a loop, after the first call
                           // pCertContext is the certificate
                           // returned by the previous call.
{
//-------------------------------------------------------------
// For simplicity, this code only searches 
// for the first occurrence of an AT_SIGNATURE key. 
// In many situations, a search would also look for a 
// specific subject name as well as the key type.

//-------------------------------------------------------------
// Call CertGetCertificateContextProperty once to get the
// returned structure size.

   if(!(CertGetCertificateContextProperty(
                 pCertContext,
                 CERT_KEY_PROV_INFO_PROP_ID,
                 NULL,
                 &dwSize)))
   {
      MyHandleError("Error Getting Key Property");
   }

//--------------------------------------------------------------
// Allocate memory for the returned structure.
    
   if(pKeyInfo)
        free(pKeyInfo);
   if(!(pKeyInfo = (CRYPT_KEY_PROV_INFO*)malloc(dwSize)))
   {
       MyHandleError("Error Allocating Memory for pKeyInfo");
   }
 
   //--------------------------------------------------------------
   // Get the key information structure.

   if(!(CertGetCertificateContextProperty(
       pCertContext,
       CERT_KEY_PROV_INFO_PROP_ID,
       pKeyInfo,
       &dwSize)))
   {
       MyHandleError("The second call to the function failed.");
   }
   
   //-------------------------------------------     
   // Check the dwKeySpec member for a signature key.
   if(pKeyInfo->dwKeySpec == AT_SIGNATURE)
   {
        fMore  = FALSE;
    }
}  // End of while loop

if(pKeyInfo)
   free(pKeyInfo);
return (pCertContext);
}  // End of GetSignerCert
```



 

 

---
description: En el ejemplo siguiente se muestra cómo un cliente típico obtendría credenciales Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Obtención de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360782"
---
# <a name="getting-schannel-credentials"></a><span data-ttu-id="3a625-103">Obtención de credenciales de Schannel</span><span class="sxs-lookup"><span data-stu-id="3a625-103">Getting Schannel Credentials</span></span>

<span data-ttu-id="3a625-104">En el ejemplo siguiente se muestra cómo un cliente típico obtendría credenciales Schannel.</span><span class="sxs-lookup"><span data-stu-id="3a625-104">The following example demonstrates how a typical client would obtain Schannel credentials.</span></span> <span data-ttu-id="3a625-105">El ejemplo sigue la práctica recomendada de usar los valores predeterminados del sistema para los cifrados y los niveles de cifrado.</span><span class="sxs-lookup"><span data-stu-id="3a625-105">The example follows the recommended practice of using the system defaults for ciphers and cipher strengths.</span></span> <span data-ttu-id="3a625-106">Esto permite que el paquete Schannel use los algoritmos más seguros posibles para proteger el canal.</span><span class="sxs-lookup"><span data-stu-id="3a625-106">This allows the Schannel package to use the strongest possible algorithms to secure the channel.</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



<span data-ttu-id="3a625-107">La principal diferencia entre la solicitud de cliente y el lado servidor para las credenciales es que el servidor debe proporcionar un certificado mediante una estructura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="3a625-107">The primary difference between the client-side and server-side request for credentials is that the server must provide a certificate using a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure as follows:</span></span>


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



<span data-ttu-id="3a625-108">La función de ejemplo *getServerCertificate* es una función de marcador de posición para esta actividad específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a625-108">The example function *getServerCertificate* is a placeholder function for this application-specific activity.</span></span> <span data-ttu-id="3a625-109">Para ver un ejemplo de implementación de la función *getServerCertificate* , consulte [obtención de un certificado](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="3a625-109">For an example implementation of the *getServerCertificate* function, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

> [!Note]  
> <span data-ttu-id="3a625-110">Al solicitar las credenciales que va a usar el servidor, cambie el tercer parámetro (*fCredentialUse*) de la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) de SECPKG \_ CRED \_ Outbound to SECPKG \_ CRED \_ Inbound.</span><span class="sxs-lookup"><span data-stu-id="3a625-110">When requesting credentials to be used by the server, change the third (*fCredentialUse*) parameter of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function from SECPKG\_CRED\_OUTBOUND to SECPKG\_CRED\_INBOUND.</span></span>

 

 

 

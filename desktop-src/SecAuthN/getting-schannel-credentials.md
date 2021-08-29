---
description: En el ejemplo siguiente se muestra cómo un cliente típico obtendría las credenciales de Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Obtención de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e088e0e0e0cb2edbc6a6551669cf4d8c5b8b3d2eb8cad38699e83001e5350
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623185"
---
# <a name="getting-schannel-credentials"></a>Obtención de credenciales de Schannel

En el ejemplo siguiente se muestra cómo un cliente típico obtendría las credenciales de Schannel. En el ejemplo se sigue la práctica recomendada de usar los valores predeterminados del sistema para los cifrados y los puntos fuertes del cifrado. Esto permite que el paquete Schannel use los algoritmos más seguros posibles para proteger el canal.


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



La diferencia principal entre la solicitud de credenciales del lado cliente y la del lado servidor es que el servidor debe proporcionar un certificado mediante una [**estructura CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de la siguiente manera:


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



La función de *ejemplo getServerCertificate* es una función de marcador de posición para esta actividad específica de la aplicación. Para obtener un ejemplo de implementación de *la función getServerCertificate,* vea [Obtención de un certificado.](getting-a-certificate-for-schannel.md)

> [!Note]  
> Al solicitar las credenciales que usará el servidor, cambie el tercer parámetro *(fCredentialUse)* de la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) de SECPKG CRED OUTBOUND a \_ \_ SECPKG \_ CRED \_ INBOUND.

 

 

 

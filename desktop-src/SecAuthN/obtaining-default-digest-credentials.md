---
description: Tanto los clientes como los servidores deben obtener credenciales para poder establecer un contexto de seguridad para el intercambio de mensajes.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtención de credenciales implícitas predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786593"
---
# <a name="obtaining-default-digest-credentials"></a>Obtención de credenciales implícitas predeterminadas

Tanto los clientes como los servidores deben [*obtener credenciales para*](../secgloss/c-gly.md) poder establecer un contexto de seguridad [*para*](../secgloss/s-gly.md) el intercambio de mensajes. El comportamiento predeterminado de la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) es proporcionar credenciales para la entidad de seguridad asociada a la sesión de inicio de [*sesión actual.*](../secgloss/s-gly.md)

En el ejemplo siguiente se muestra una llamada del lado servidor para obtener las credenciales predeterminadas.


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



La llamada del lado cliente para las credenciales predeterminadas es idéntica, salvo que el tercer parámetro debe especificar SECPKG CRED OUTBOUND para indicar que el cliente usará el identificador de credenciales devuelto \_ \_ por la función.

Para obtener un ejemplo en el que se muestra cómo obtener credenciales para una entidad de seguridad que no sea el usuario que ha iniciado sesión, vea [Obtención de credenciales alternativas.](obtaining-alternate-digest-credentials.md)

 

 

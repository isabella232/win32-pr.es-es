---
description: Tanto los clientes como los servidores deben obtener las credenciales para poder establecer un contexto de seguridad para el intercambio de mensajes.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtención de credenciales de Resumen predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276691"
---
# <a name="obtaining-default-digest-credentials"></a>Obtención de credenciales de Resumen predeterminadas

Tanto los clientes como los servidores deben obtener [*las credenciales*](../secgloss/c-gly.md) para poder establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes. El comportamiento predeterminado de la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) es proporcionar credenciales para la entidad de seguridad asociada a la [*sesión*](../secgloss/s-gly.md)de inicio de sesión actual.

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



La llamada del lado cliente para las credenciales predeterminadas es idéntica, salvo que el tercer parámetro debe especificar SECPKG \_ CRED \_ Outbound para indicar que el cliente usará el identificador de credenciales devuelto por la función.

Para obtener un ejemplo que muestra cómo obtener las credenciales de una entidad de seguridad que no sea el usuario que ha iniciado sesión, consulte [obtención de credenciales alternativas](obtaining-alternate-digest-credentials.md).

 

 

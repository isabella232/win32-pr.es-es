---
description: El proceso de autenticación de Schannel requiere las credenciales; tanto el cliente como el servidor deben obtener credenciales válidas para establecer un contexto de seguridad para el intercambio de mensajes. Para obtener un ejemplo que muestra este procedimiento, vea Obtención de credenciales.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtención de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173394"
---
# <a name="obtaining-schannel-credentials"></a>Obtención de credenciales de Schannel

El proceso de autenticación de Schannel requiere las credenciales; tanto el cliente como el servidor deben obtener credenciales válidas para establecer un contexto [*de seguridad para*](../secgloss/s-gly.md) el intercambio de mensajes. Para obtener un ejemplo que muestra este procedimiento, vea [Obtención de credenciales.](getting-a-certificate-for-schannel.md)

La aplicación obtiene las credenciales mediante una llamada a [**la función AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) que devuelve un identificador a las credenciales solicitadas. Dado que los identificadores de credenciales se usan para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor. Esto significa que las aplicaciones que admiten conexiones de cliente y servidor deben obtener un mínimo de dos identificadores de credenciales.

En Windows XP, una estructura [**\_ CRED de SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica lo siguiente:

-   Un protocolo de seguridad
-   Cifrados permitidos
-   Niveles mínimos y máximos de cifrado
-   Un [*certificado X.509*](../secgloss/x-gly.md) usado para la autenticación: necesario para el servidor, opcional para el cliente a menos que el servidor solicite la autenticación de cliente.

Pase la [**estructura \_ CRED de SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (a través del *parámetro pAuthData)* a la [**función AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Esta función devuelve el identificador de credenciales necesario para establecer un [*contexto de seguridad*](../secgloss/s-gly.md).

Para obtener información detallada sobre cómo establecer los cifrados usados con Schannel, vea [Especificar cifrados de Schannel y puntos fuertes de cifrado.](specifying-schannel-ciphers-and-cipher-strengths.md)

Para obtener información sobre los certificados, vea [Funciones de almacén de certificados y certificados](../seccrypto/cryptography-functions.md).

Para obtener un ejemplo en el que se muestra cómo abrir un almacén [*de*](../secgloss/c-gly.md) certificados y buscar un certificado para usarlo para la autenticación de Schannel, consulte [Obtención de un certificado.](getting-a-certificate-for-schannel.md)

 

 

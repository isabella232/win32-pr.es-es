---
description: El proceso de autenticación de Schannel requiere credenciales. tanto el cliente como el servidor deben obtener credenciales válidas para establecer un contexto de seguridad para el intercambio de mensajes. Para obtener un ejemplo en el que se muestra este procedimiento, vea obtener credenciales.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtención de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813606"
---
# <a name="obtaining-schannel-credentials"></a>Obtención de credenciales de Schannel

El proceso de autenticación de Schannel requiere credenciales. tanto el cliente como el servidor deben obtener credenciales válidas para establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes. Para obtener un ejemplo en el que se muestra este procedimiento, vea [obtener credenciales](getting-a-certificate-for-schannel.md).

La aplicación obtiene las credenciales mediante una llamada a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , que devuelve un identificador a las credenciales solicitadas. Dado que los identificadores de credenciales se usan para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor. Esto significa que las aplicaciones que admiten conexiones de cliente y de servidor deben obtener un mínimo de dos identificadores de credenciales.

En Windows XP, una estructura de [**\_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica lo siguiente:

-   Un protocolo de seguridad
-   Cifrados permitidos
-   Intensidad mínima y máxima de cifrado
-   Un certificado [*X. 509*](../secgloss/x-gly.md) que se usa para la autenticación, necesario para el servidor, opcional para el cliente a menos que el servidor solicite la autenticación del cliente.

Pase la [**estructura \_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (a través del parámetro *pAuthData* ) a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Esta función devuelve el identificador de credenciales necesario para establecer un [*contexto de seguridad*](../secgloss/s-gly.md).

Para obtener información detallada sobre cómo establecer los cifrados utilizados con Schannel, consulte [especificar cifrados Schannel y intensidades de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md).

Para obtener información acerca de los certificados, consulte [funciones del almacén](../seccrypto/cryptography-functions.md)de certificados y certificados.

Para obtener un ejemplo en el que se muestra la apertura de un [*almacén de certificados*](../secgloss/c-gly.md) y la ubicación de un certificado que se va a usar para la autenticación Schannel, vea [obtener un certificado](getting-a-certificate-for-schannel.md).

 

 

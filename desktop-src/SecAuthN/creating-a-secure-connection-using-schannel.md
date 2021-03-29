---
description: Cómo crear una conexión segura con Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Crear una conexión segura mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814747"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Crear una conexión segura mediante Schannel

El [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) de Schannel proporciona acceso a cuatro [*protocolos de seguridad*](/windows/desktop/SecGloss/s-gly):

-   [Seguridad de la capa de transporte (TLS 1,2)](transport-layer-security-protocol.md)
-   [Seguridad de la capa de transporte (TLS 1,1)](transport-layer-security-protocol.md)
-   [Seguridad de la capa de transporte (TLS 1,0)](transport-layer-security-protocol.md)
-   [Capa de sockets seguros (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [Capa de sockets seguros (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Los protocolos PCT y SSL 2,0 se han sustituido por el protocolo TLS y no se deben usar para el nuevo desarrollo.

 

**Para configurar una conexión segura entre un cliente y un servidor**

1.  Obtener las credenciales de Schannel ([obtención de credenciales de Schannel](obtaining-schannel-credentials.md)).
2.  Cree un contexto de seguridad de Schannel ([creando un contexto de seguridad de Schannel](creating-an-schannel-security-context.md)).

Una vez establecida una conexión, puede recuperar información sobre sus atributos. Para más información, consulte [obtención de información acerca de las conexiones Schannel](getting-information-about-schannel-connections.md).

Si, después de establecer una conexión, los requisitos de seguridad de la aplicación cambian o se pierde la conexión, puede volver a negociar la conexión. Para obtener más información, consulte [renegociación de una conexión Schannel](renegotiating-an-schannel-connection.md).

Cuando haya terminado de usar una conexión Schannel, debe realizar la limpieza necesaria. Para obtener más información, consulte [apagar una conexión Schannel](shutting-down-an-schannel-connection.md).

Para obtener información acerca de los ejemplos que se incluyen con el kit de desarrollo de software (SDK) de la plataforma que muestra el [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly)de Schannel, consulte los ejemplos de psdk con Schannel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar cifrados Schannel y niveles de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 

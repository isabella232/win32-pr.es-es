---
description: Cómo crear una conexión segura mediante Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Creación de una conexión segura mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008913"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Creación de una conexión segura mediante Schannel

El paquete de [*seguridad de Schannel*](/windows/desktop/SecGloss/s-gly) proporciona acceso a cuatro [*protocolos de seguridad:*](/windows/desktop/SecGloss/s-gly)

-   [Seguridad de la capa de transporte (TLS 1.2)](transport-layer-security-protocol.md)
-   [Seguridad de la capa de transporte (TLS 1.1)](transport-layer-security-protocol.md)
-   [Seguridad de la capa de transporte (TLS 1.0)](transport-layer-security-protocol.md)
-   [Capa de sockets seguros (SSL 3.0)](secure-sockets-layer-protocol.md)
-   [Capa de sockets seguros (SSL 2.0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Los protocolos PCT y SSL 2.0 han sido reemplazados por el protocolo TLS y no deben usarse para el nuevo desarrollo.

 

**Para configurar una conexión segura entre un cliente y un servidor**

1.  Obtenga las credenciales de Schannel ([Obtención de credenciales de Schannel](obtaining-schannel-credentials.md)).
2.  Cree un contexto de seguridad de Schannel ([Crear un contexto de seguridad de Schannel](creating-an-schannel-security-context.md)).

Una vez establecida una conexión, puede recuperar información sobre sus atributos. Para obtener más información, [consulte Obtención de información sobre las conexiones Schannel.](getting-information-about-schannel-connections.md)

Si, después de establecer una conexión, los requisitos de seguridad de la aplicación cambian o se pierde la conexión, puede volver a negociar la conexión. Para más información, consulte [Renegociación de una conexión Schannel.](renegotiating-an-schannel-connection.md)

Cuando haya terminado de usar una conexión Schannel, debe realizar la limpieza necesaria. Para obtener más información, [vea Apagar una conexión Schannel.](shutting-down-an-schannel-connection.md)

Para obtener información sobre los ejemplos incluidos con el Kit de desarrollo de software de plataforma (SDK) que muestran el paquete de seguridad de [*Schannel,*](/windows/desktop/SecGloss/s-gly)consulte los ejemplos de PSDK con Schannel.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificar cifrados de Schannel y puntos fuertes de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 

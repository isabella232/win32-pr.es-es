---
description: Schannel admite las versiones 1,0, 1,1 y 1,2 del protocolo seguridad de la capa de transporte (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocolo de seguridad de la capa de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668125"
---
# <a name="transport-layer-security-protocol"></a>Protocolo de seguridad de la capa de transporte

Schannel admite las versiones 1,0, 1,1 y 1,2 del [*Protocolo seguridad de la capa de transporte (TLS)*](../secgloss/t-gly.md). Este protocolo es un estándar del sector diseñado para proteger la privacidad de la información que se comunica a través de Internet. TLS supone que un transporte orientado a la conexión, normalmente TCP, está en uso. El protocolo TLS permite a las aplicaciones cliente/servidor detectar los riesgos de seguridad siguientes:

-   Manipulación de mensajes
-   Interceptación de mensajes
-   Falsificación de mensajes

La especificación completa del protocolo TLS está disponible en el sitio web de IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organización de TLS

Los siguientes pasos están relacionados con el uso de TLS para la comunicación entre cliente y servidor:

 **Para utilizar TLS para la comunicación entre cliente y servidor**

1.  Negociación del conjunto de protocolos y el protocolo de enlace
2.  Autenticación de entidades
3.  Intercambio de información relacionada con claves
4.  Intercambio de datos de aplicaciones

Los pasos que componen TLS están divididos en dos protocolos que, juntos, proporcionan seguridad de conexión:

-   [Protocolo de enlace TLS](tls-handshake-protocol.md): (pasos 1 a 3)
-   [Protocolo de registro de TLS](tls-record-protocol.md): (paso 4)

## <a name="sspi-with-tls-implementations"></a>SSPI con implementaciones de TLS

Dado que TLS no tiene una especificación GSSAPI, es posible que los implementadores de TLS no estén familiarizados con las funciones SSPI. Las aplicaciones llaman a las funciones SSPI para enumerar los paquetes disponibles, crear y trabajar con identificadores de credenciales, crear contextos de seguridad y garantizar la privacidad de la integridad del mensaje.

Para admitir las funciones SSPI usadas por las aplicaciones de modo de usuario, las funciones enumeradas en [funciones implementadas por SSP/APS de modo de usuario](/windows/desktop/SecAuthN/authentication-functions) deben ser compatibles con las implementaciones de TLS como schannel.dll.

Para obtener más información sobre las funciones SSPI y las funciones SSP, consulte [funciones de autenticación](authentication-functions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de cifrado TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS frente a SSL](tls-versus-ssl.md)
</dt> </dl>

 

 

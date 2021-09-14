---
description: Schannel admite las versiones 1.0, 1.1 y 1.2 del protocolo seguridad de la capa de transporte (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocolo de seguridad de la capa de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160910"
---
# <a name="transport-layer-security-protocol"></a>Protocolo de seguridad de la capa de transporte

Schannel admite las versiones 1.0, 1.1 y 1.2 del protocolo seguridad de la capa de [*transporte (TLS).*](../secgloss/t-gly.md) Este protocolo es un estándar del sector diseñado para ayudar a proteger la privacidad de la información que se comunica mediante Internet. TLS supone que un transporte orientado a la conexión, normalmente TCP, está en uso. El protocolo TLS permite que las aplicaciones cliente/servidor detecten los siguientes riesgos de seguridad:

-   Manipulación de mensajes
-   Interceptación de mensajes
-   Falsificación de mensajes

La especificación completa del protocolo TLS está disponible en el sitio web de IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organización de TLS

Los pasos siguientes intervienen en el uso de TLS para la comunicación entre cliente y servidor:

 **Para usar TLS para la comunicación cliente/servidor**

1.  Protocolo de enlace y negociación del conjunto de cifrado
2.  Autenticación de entidades
3.  Intercambio de información relacionada con claves
4.  Intercambio de datos de aplicación

Los pasos que conste TLS se dividen en dos protocolos que, juntos, proporcionan seguridad de conexión:

-   [Protocolo de protocolo de enlace TLS](tls-handshake-protocol.md)( pasos 1 – 3)
-   [Protocolo de registro TLS](tls-record-protocol.md): (paso 4)

## <a name="sspi-with-tls-implementations"></a>SSPI con implementaciones de TLS

Dado que TLS no tiene una especificación GSSAPI, es posible que los implementadores tls no conozcan las funciones SSPI. Las aplicaciones llaman a las funciones SSPI para enumerar los paquetes disponibles, crear y trabajar con identificadores de credenciales, crear contextos de seguridad y garantizar la privacidad de la integridad de los mensajes.

Para admitir las funciones SSPI que usan las aplicaciones en modo de usuario, las funciones enumeradas en Funciones implementadas por [SSP/AP](/windows/desktop/SecAuthN/authentication-functions) en modo de usuario deben ser compatibles con implementaciones tls como schannel.dll.

Para obtener más información sobre las funciones de SSPI y las funciones de SSP, vea [Funciones de autenticación](authentication-functions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de cifrado TLS](tls-cipher-suites.md)
</dt> <dt>

[TLS frente a SSL](tls-versus-ssl.md)
</dt> </dl>

 

 

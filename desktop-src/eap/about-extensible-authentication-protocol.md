---
title: Acerca de EAP
description: Protocolo de autenticación extensible (EAP), un estándar compatible con muchos componentes de red de Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticación extensible, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421530"
---
# <a name="about-eap"></a>Acerca de EAP

En este tema se describe el protocolo de autenticación extensible (EAP), un estándar que admiten muchos componentes de red de Microsoft.

## <a name="eap-components"></a>Componentes de EAP

EAP es fundamental para proteger la seguridad de LAN inalámbricas (802.1 X), LAN cableadas y redes privadas virtuales (VPN) y de acceso telefónico.

Los componentes siguientes admiten el protocolo EAP.

-   Los clientes y servidores de acceso remoto de Microsoft para acceso telefónico y VPN (PPTP y L2TP/IPSec) implementan EAP como una extensión de PPP. Para obtener más información, consulte [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Los clientes de LAN inalámbrica y cableada compatibles con IEEE 802.1 X de Microsoft implementan EAP tal y como se define en el borrador estándar IEEE 802.1 X.
-   El servidor RADIUS de Microsoft, denominado servicio de autenticación de Internet (IAS), implementa EAP tal y como se define en [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).

Todos los componentes anteriores admiten esta arquitectura extensible a través del kit de desarrollo de software (SDK) de Microsoft Windows, lo que permite integrar módulos de autenticación de terceros. Este mecanismo extensible se puede usar para admitir los protocolos de autenticación de tarjetas de token, Kerberos, clave pública y S/Key.

## <a name="protected-extensible-authentication-protocol"></a>Protocolo de autenticación extensible protegido

Además de EAP, la implementación inalámbrica (802.1 X) y el servidor RADIUS también admiten un estándar emergente denominado EAP protegido (PEAP).

PEAP proporciona varios servicios clave a otros protocolos de autenticación EAP, como se indica a continuación.

-   PEAP cifra los paquetes EAP de otros protocolos de autenticación EAP mediante seguridad de la capa de transporte (TLS), una tecnología basada en capa de sockets seguros (SSL). Para obtener más información, consulte [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP autentica el lado servidor mediante un certificado de servidor, con el servidor RADIUS.
-   PEAP ofrece una funcionalidad de reautenticación rápida que admite la itinerancia eficaz entre dispositivos inalámbricos.
-   PEAP administra la fragmentación y el reensamblado de los paquetes EAP.
-   PEAP genera claves utilizadas para cifrar el tráfico inalámbrico.

PEAP facilita la escritura de un protocolo EAP, ya que el programador ya no tiene que resolver estos problemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de EAP y EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 





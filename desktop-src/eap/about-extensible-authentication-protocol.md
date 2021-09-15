---
title: Acerca de EAP
description: Protocolo de autenticación extensible (EAP), un estándar compatible con muchos componentes de red de Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocolo de autenticación extensible, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569284"
---
# <a name="about-eap"></a>Acerca de EAP

En este tema se describe el Protocolo de autenticación extensible (EAP), un estándar compatible con muchos componentes de red de Microsoft.

## <a name="eap-components"></a>Componentes de EAP

EAP es fundamental para proteger la seguridad de redes LAN inalámbricas (802.1X), LAN cableadas y acceso telefónico y redes privadas virtuales (VPN).

Los componentes siguientes admiten el protocolo EAP.

-   Los clientes y servidores de acceso remoto de Microsoft para acceso telefónico y VPN (PPTP e L2TP/IPSec) implementan EAP como una extensión para PPP. Para obtener más información, [vea RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Los clientes laN inalámbricas y cableadas compatibles con Microsoft IEEE 802.1X implementan EAP como se define en el estándar de borrador IEEE 802.1X.
-   El servidor RADIUS de Microsoft, denominado Servicio de autenticación de Internet (IAS), implementa EAP tal como se define [en RFC 2865.](https://go.microsoft.com/fwlink/p/?linkid=84055)

Todos los componentes anteriores admiten esta arquitectura extensible a través del Kit de desarrollo de software (SDK) de Microsoft Windows, lo que permite integrar módulos de autenticación de terceros. Este mecanismo extensible se puede usar para admitir tarjetas de token, kerberos, clave pública y protocolos de autenticación S/Key.

## <a name="protected-extensible-authentication-protocol"></a>Protocolo de autenticación extensible protegido

Además de EAP, la implementación inalámbrica (802.1X) y el servidor RADIUS también admiten un estándar emergente denominado EAP protegido (PEAP).

PEAP proporciona varios servicios clave para otros protocolos de autenticación EAP, como se muestra a continuación.

-   PEAP cifra los paquetes EAP de otros protocolos de autenticación EAP mediante seguridad de la capa de transporte (TLS), una tecnología basada en capa de sockets seguros (SSL). Para obtener más información, [vea RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP autentica el lado servidor mediante un certificado de servidor, con servidor RADIUS.
-   PEAP ofrece una funcionalidad de re-autenticación rápida que admite la itinerancia eficaz entre dispositivos inalámbricos.
-   PEAP administra la fragmentación y el nuevo ensamblado de paquetes EAP.
-   PEAP genera claves que se usan para cifrar el tráfico inalámbrico.

PEAP facilita mucho la escritura de un protocolo EAP porque el programador ya no tiene que solucionar estos problemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de EAP y EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 





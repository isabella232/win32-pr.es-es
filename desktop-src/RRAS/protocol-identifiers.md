---
title: Identificadores de protocolo
description: Los siguientes identificadores de protocolo también se enumeran en Routprot. h para el Windows SDK y iprtmib. h para el kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ac515eb4b5090c0b4f75fd923d8345538ff5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359244"
---
# <a name="protocol-identifiers"></a>Identificadores de protocolo

Los siguientes identificadores de protocolo también se enumeran en Routprot. h para el Windows SDK y iprtmib. h para el kit de desarrollo de software (SDK) de la plataforma.

## <a name="ip-protocols"></a>Protocolos IP

Los siguientes protocolos de enrutamiento están asociados al transporte IP.



| Protocolo                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROTO \_ IP \_ other, MIB \_ IPPROTO \_ other                        | Otro protocolo no especificado en RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ local, MIB \_ IPPROTO \_ local                        | Una interfaz local.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT, MIB \_ IPPROTO \_ netmgmt                    | Una ruta estática. Este valor se usa para identificar la información de ruta para el enrutamiento IP establecido a través de la administración de redes como el protocolo de configuración dinámica de host (DCHP), el Protocolo simple de administración de redes (SNMP) o llamadas a las funciones [**CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)o [**SetIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry) .                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Resultado de la redirección ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | El protocolo de puerta de enlace exterior (EGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | El protocolo de puerta de enlace a puerta de enlace (GGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ Hello, MIB \_ IPPROTO \_ Hello                        | El protocolo Hellospeak, un protocolo de enrutamiento dinámico. Se trata de una entrada histórica que ya no está en uso y era un protocolo de enrutamiento temprano usado por los enrutadores de ARPANET originales que ejecutaron software especial denominado Protocolo de enrutamiento Fuzzball, que a veces se denomina Hellospeak, como se describe en RFC 891 y RFC 1305. Para más información, vea [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) y [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | El protocolo de información de enrutamiento de Berkeley (RIP) o RIP-II, un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ es \_ , MIB \_ IPPROTO \_ \_ es                      | El protocolo intermedio de sistema a intermediario (IS-IS), un protocolo de enrutamiento dinámico. El protocolo IS-IS se desarrolló para su uso en el conjunto de protocolos de interconexión de sistemas abiertos (OSI).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ es \_ , MIB \_ IPPROTO \_ \_ es                      | El protocolo end-to-Intermediate System (es-IS-IS), un protocolo de enrutamiento dinámico. El protocolo es-es desarrollado para su uso en el conjunto de protocolos de interconexión de sistemas abiertos (OSI).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ Cisco, MIB \_ IPPROTO \_ Cisco                        | El protocolo de enrutamiento de puerta de enlace interior de Cisco (IGRP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | El protocolo de puerta de enlace interior (IGP) Bolt, Beranek y Newman (BBN) que usaba el algoritmo de ruta de acceso más corta (SPF). Se trata de un protocolo de enrutamiento dinámico temprano.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | El protocolo de ruta de acceso más corta (OSPF) abierto, un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | El Protocolo de puerta de enlace de borde (BGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP, MIB \_ IPPROTO \_ BOOTP                        | El protocolo bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPv6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | El protocolo de retransmisión DHCPv6.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ autoestática, MIB \_ IPNT \_ autoestática             | Entrada específica de Windows agregada originalmente por un protocolo de enrutamiento, pero que ahora es estática.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ static, MIB \_ IPNT \_ static                     | Una entrada específica de Windows que se agrega como una ruta estática desde la interfaz de usuario de enrutamiento o un comando de enrutamiento.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ static \_ no \_ DOD, MIB \_ IPNT \_ static \_ no \_ DoD | Una entrada específica de Windows que se agrega como una ruta estática desde la interfaz de usuario de enrutamiento o desde un comando de enrutamiento, excepto en que estas rutas no causan el marcado a petición (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

Las rutas con un identificador de protocolo de PROTO \_ IP \_ local incluyen:

-   La ruta de bucle invertido
-   La ruta de subred
-   Todas las redes retransmiten la ruta para interfaces subredes
-   Toda la ruta de difusión de "1" s
-   Ruta de multidifusión local
-   Ruta al extremo remoto de un vínculo PPP

El identificador del administrador de enrutador IP es:

IPRTRMGR \_ PID

Este identificador se puede usar en lugar de un identificador de protocolo de enrutamiento para llamadas MIB con el administrador de enrutadores IP. Este identificador se usa para MIB-II, la MIB de reenvío y la información específica de la empresa. Este identificador también se muestra en Iprtrmib. h.

## <a name="ipx-protocols"></a>Protocolos IPX

Los siguientes protocolos de enrutamiento están asociados con el transporte IPX.



| Protocolo            | Descripción                          |
|---------------------|--------------------------------------|
| \_RIP del protocolo IPX \_  | Protocolo de información de enrutamiento para IPX |
| protocolo IPX de \_ \_ SAP  | Protocolo de anuncio de servicio       |
| \_protocolo IPX \_ NLSP | Protocolo NetWare Link Services       |



 

El identificador del administrador de enrutadores de IPX es:

\_base del protocolo IPX \_

Use este identificador en lugar de un identificador de protocolo de enrutamiento para llamadas MIB con el administrador de enrutadores de IPX.

 

 
---
title: Identificadores de protocolo
description: Los siguientes identificadores de protocolo también se enumeran en Routprot.h para el SDK de Windows y en iprtmib.h para el Kit de desarrollo de software de plataforma (SDK).
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dafcbcd028b5c8d4f58172565b34c93cff8d8f9ff766c055e3d8a956cfbb0aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036475"
---
# <a name="protocol-identifiers"></a>Identificadores de protocolo

Los siguientes identificadores de protocolo también se enumeran en Routprot.h para el SDK de Windows y en iprtmib.h para el Kit de desarrollo de software de plataforma (SDK).

## <a name="ip-protocols"></a>Protocolos IP

Los siguientes protocolos de enrutamiento están asociados al transporte IP.



| Protocolo                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROTO \_ IP \_ OTHER, MIB \_ IPPROTO \_ OTHER                        | Otro protocolo no especificado en RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ LOCAL, MIB \_ IPPROTO \_ LOCAL                        | Interfaz local.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NETMGMT, MIB \_ IPPROTO \_ NETMGMT                    | Una ruta estática. Este valor se usa para identificar la información de ruta para el enrutamiento IP establecido a través de la administración de red, como el Protocolo de configuración dinámica de host (DCHP), el Protocolo simple de administración de redes (SNMP) o mediante llamadas a las funciones [**CreateIpForwardEntry,**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry) [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)o [**SetIpForwardEntry.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry)                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Resultado de la redirección ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | El protocolo de puerta de enlace exterior (EGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | Protocolo de puerta de enlace a puerta de enlace (GGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ HELLO, MIB \_ IPPROTO \_ HELLO                        | El protocolo Hellospeak, un protocolo de enrutamiento dinámico. Se trata de una entrada histórica que ya no está en uso y era un protocolo de enrutamiento temprano usado por los enrutadores ARPANET originales que ejecutó software especial denominado protocolo de enrutamiento Fuzzball, a veces denominado Hellospeak, como se describe en RFC 891 y RFC 1305. Para más información, vea [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) y [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | Berkeley Protocolo de información de enrutamiento (RIP) o RIP-II, un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ IS \_ IS, MIB \_ IPPROTO \_ IS \_ IS                      | El protocolo de sistema a sistema intermedio (IS-IS), un protocolo de enrutamiento dinámico. El protocolo IS-IS se desarrolló para su uso en el conjunto de protocolos de interconexión de sistemas abiertos (OSI).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ ES \_ IS, MIB \_ IPPROTO \_ ES \_ IS                      | El protocolo End System-to-Intermediate System (ES-IS), un protocolo de enrutamiento dinámico. El protocolo ES-IS se desarrolló para su uso en el conjunto de protocolos de interconexión de sistemas abiertos (OSI).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ CISCO, MIB \_ IPPROTO \_ CISCO                        | Cisco Interior Gateway Routing Protocol (IGRP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | Bolt, Beranek y Newman (BBN) Interior Gateway Protocol (IGP) que usaban el algoritmo Shortest Path First (SPF). Se trata de un protocolo de enrutamiento dinámico temprano.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | El protocolo Open Shortest Path First (OSPF), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | El Protocolo de puerta de enlace de borde (BGP), un protocolo de enrutamiento dinámico.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP, MIB \_ IPPROTO \_ BOOTP                        | El protocolo bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPV6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | El protocolo DHCPv6 Relay.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ AUTOSTATIC, MIB \_ IPNT \_ AUTOSTATIC             | Una Windows específica agregada originalmente por un protocolo de enrutamiento, pero que ahora es estática.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ STATIC, MIB \_ IPNT \_ STATIC                     | Una Windows específica agregada como una ruta estática desde la interfaz de usuario de enrutamiento o un comando de enrutamiento.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ STATIC \_ NON \_ DOD, MIB \_ IPNT \_ STATIC \_ NON \_ DOD | Una Windows específica agregada como una ruta estática desde la interfaz de usuario de enrutamiento o un comando de enrutamiento, salvo que estas rutas no provocan dial a petición (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

Las rutas con un identificador de protocolo de PROTO \_ IP \_ LOCAL incluyen:

-   Ruta de bucle recuperación
-   Ruta de subred
-   Ruta de difusión de todas las redes para interfaces subredadas
-   Ruta de difusión de "1"
-   Ruta de multidifusión local
-   Enrutar al extremo remoto de un vínculo PPP

El identificador del administrador de enrutadores IP es:

PID de \_ IPRTRMGR

Este identificador se puede usar en lugar de un identificador de protocolo de enrutamiento para llamadas MIB con el administrador de enrutadores IP. Este identificador se usa para MIB-II, MIB de reenvío y alguna información específica de la empresa. Este identificador también se muestra en Iprtmidb.h.

## <a name="ipx-protocols"></a>Protocolos IPX

Los siguientes protocolos de enrutamiento están asociados al transporte IPX.



| Protocolo            | Descripción                          |
|---------------------|--------------------------------------|
| IPX \_ PROTOCOL \_ RIP  | Protocolo de información de enrutamiento para IPX |
| IPX \_ PROTOCOL \_ SAP  | Protocolo de anuncio de servicio       |
| PROTOCOLO IPX \_ \_ NLSP | Protocolo de servicios de vínculo de NetWare       |



 

El identificador del administrador de enrutadores IPX es:

IPX \_ PROTOCOL \_ BASE

Use este identificador en lugar de un identificador de protocolo de enrutamiento para llamadas MIB con el administrador de enrutadores IPX.

 

 
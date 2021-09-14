---
title: Constantes de secuencia de protocolo
description: Rpc de Microsoft admite las siguientes secuencias de protocolo.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361920"
---
# <a name="protocol-sequence-constants"></a>Constantes de secuencia de protocolo

Rpc de Microsoft admite las siguientes secuencias de protocolo.



| Constante o valor                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ nb \_ tcp**</dt> <dt>Connection-oriented NetBIOS over Transmission Control Protocol (TCP)</dt> </dl>          | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ nb \_ ipx**</dt> <dt>Connection-oriented NetBIOS over Internet Packet Exchange (IPX)</dt> </dl>               | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ nb \_ nb**</dt> <dt>Connection-oriented NetBIOS Enhanced Interfaz de usuario (NetBEUI)</dt> </dl>                    | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**ncacn \_ ip \_ tcp**</dt> Protocolo de control de transmisión orientado a la <dt>conexión/Protocolo de Internet (TCP/IP)</dt> </dl>  | Solo cliente: MS-DOS, Windows 3. *x* y Apple Macintosh Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>**ncacn \_ np**</dt> <dt>Canalizaciones con nombre orientadas a conexiones</dt> </dl>                                                            | Solo cliente: MS-DOS, Windows 3. *x*, Windows 95 Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ spx**</dt> <dt>Connection-oriented Sequenced Packet Exchange (SPX)</dt> </dl>                                     | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ nsp**</dt> <dt>Transporte de DECnet</dt> orientado a la conexión </dl>                                    | Solo cliente: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ en dsp \_ Connection-oriented**</dt> <dt>AppleTalk DSP (DSP de AppleTalk orientado a la conexión)</dt> </dl>                                             | Cliente: Apple Macintosh Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**ncacn \_ vns \_ spp**</dt> Transporte de procesamiento paralelo escalable <dt>(SPP) orientado</dt> a conexiones </dl>     | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ ip \_ udp**</dt> <dt>Datagram (sin conexión) Protocolo de datagramas de usuario/Protocolo de Internet (UDP/IP)</dt> </dl>   | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_ ipx**</dt> <dt>Datagram (sin conexión) IPX</dt> </dl>                                                           | Solo cliente: MS-DOS, Windows 3. *x* Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ mq**</dt> <dt>Datagram (sin conexión) a través de Microsoft Message Queue Server (MSMQ)</dt> </dl>                   | Solo cliente: Windows Me/98/95 Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4.0 con SP3 y versiones posteriores<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**ncacn \_ http**</dt> <dt>Connection-oriented TCP/IP using Microsoft Internet Information Server as HTTP proxy</dt> </dl> | Solo cliente: Windows Cliente y servidor 98/98/95: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**ncalrpc**</dt> <dt>Local procedure call</dt> </dl>                                                                           | Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Observaciones

El [**transporte ncalrpc**](/windows/desktop/Midl/ncalrpc) solo admite la autenticación WINNT de \_ RPC C \_ \_ AUTHN. Para obtener más información, vea [Security](security.md) and [Authentication-Service Constants](authentication-service-constants.md).

Rpc de Microsoft [**admite RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) solo en aplicaciones cliente, no en aplicaciones de servidor.

 


---
title: Constantes de secuencia de protocolo
description: Microsoft RPC admite las siguientes secuencias de protocolo.
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078198"
---
# <a name="protocol-sequence-constants"></a>Constantes de secuencia de protocolo

Microsoft RPC admite las siguientes secuencias de protocolo.



| Constante o valor                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**NetBIOS \_ ncacn \_ NB**</dt> <dt>orientado a la conexión TCP a través del Protocolo de control de transmisión (TCP)</dt> </dl>          | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ NB \_**</dt> <dt>de conexión IPX orientada a conexiones de NetBIOS sobre el intercambio de paquetes de Internet (IPX)</dt> </dl>               | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>interfaz de usuario mejorada de NetBIOS orientada a la conexión de</dt> <dt>**Ncacn \_ NB \_**</dt> (NetBEUI) </dl>                    | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> ncacn protocolo <dt>de control de transmisión orientado a la conexión TCP IP/protocolo de Internet (TCP/IP)</dt> <dt>**\_ \_**</dt> </dl>  | Solo cliente: MS-DOS, Windows 3. *x* y cliente y servidor de Apple Macintosh: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>canalizaciones con nombre orientadas a</dt> <dt>**ncacn \_ NP**</dt> </dl>                                                            | Solo cliente: MS-DOS, Windows 3. *x*, cliente y servidor de Windows 95: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>intercambio de paquetes secuenciado orientado a la conexión</dt> <dt>**NCACN \_ SPX**</dt> (SPX) </dl>                                     | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>transporte DECnet orientado a la conexión de</dt> <dt>**ncacn \_ dnet \_ NSP**</dt> </dl>                                    | Solo cliente: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ en \_**</dt> DSP <dt>de AppleTalk orientado a la conexión</dt> </dl>                                             | Cliente: Apple Macintosh Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>transporte de procesamiento paralelo escalable (spp) de Vines orientado a</dt> <dt>**ncacn \_ redes virtuales \_ spp**</dt> </dl>     | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**datagrama \_ \_ UDP de IP ncadg**</dt> <dt>(sin conexión) protocolo de datagramas de usuario/protocolo de Internet (UDP/IP)</dt> </dl>   | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**datagrama \_ IPX de ncadg**</dt> <dt>(sin conexión) IPX</dt> </dl>                                                           | Solo cliente: MS-DOS, Windows 3. cliente y servidor *x* : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ MQ**</dt> <dt>Datagram (sin conexión) sobre Microsoft Message Queue Server (MSMQ)</dt> </dl>                   | Solo cliente: cliente y servidor de Windows Me/98/95: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 con SP3 y versiones posteriores<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**NCACN \_**</dt> <dt>TCP/IP orientado a la conexión http con Microsoft Internet Information Server como proxy http</dt> </dl> | Solo cliente: cliente y servidor de Windows Me/98/95: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt></dt> <dt>llamada al procedimiento local</dt> ncalrpc </dl>                                                                           | Cliente y servidor: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Observaciones

El transporte [**ncalrpc**](/windows/desktop/Midl/ncalrpc) solo admite la \_ autenticación de WinNT de RPC C \_ authn \_ . Para obtener más información, consulte [seguridad](security.md) y [autenticación: constantes de servicio](authentication-service-constants.md).

Microsoft RPC solo admite [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) en aplicaciones cliente, no en aplicaciones de servidor.

 


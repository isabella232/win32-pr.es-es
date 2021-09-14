---
description: Página de navegación para Windows sockets de conexión (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opciones de socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965323"
---
# <a name="socket-options"></a>Opciones de socket

En esta sección se describen las opciones de socket de Winsock para varias ediciones Windows sistemas operativos. Use las [**funciones getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) [**y setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obtener y establecer más opciones de socket. Para enumerar los protocolos y detectar las propiedades admitidas para cada protocolo instalado, use la [**función WSAEnumProtocols.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)

Algunas opciones de socket requieren más explicaciones de las que pueden transmitir estas tablas. estas opciones contienen vínculos a páginas adicionales.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IP DE \_ IPPROTO**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel IPv4. Para obtener más información, vea IpPROTO IP Socket Options ( Opciones [**de socket IP DE \_ IPPROTO).**](ipproto-ip-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPV6**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel IPv6. Para obtener más información, vea [**IPPROTO IPV6 Socket Options ( Opciones de \_ socket IPV6 de IPPROTO).**](ipproto-ipv6-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de multidifusión confiable. Para obtener más información, vea IPPROTO RM Socket Options ( Opciones [**de socket de RM \_ de IPPROTO).**](ipproto-rm-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel TCP. Para obtener más información, vea IpPROTO TCP Socket Options ( Opciones [**de socket TCP \_ de IPPROTO).**](ipproto-tcp-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**UDP de \_ IPPROTO**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel UDP. Para obtener más información, vea IpPROTO UDP Socket Options ( Opciones [**de socket UDP \_ de IPPROTO).**](ipproto-udp-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**IPX de NSPROTO \_**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel IPX. Para obtener más información, vea [**NSPROTO IPX Socket Options ( Opciones \_ de socket DE IPX de NSPROTO).**](nsproto-ipx-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de AppleTalk. Para obtener más información, vea [**SOL \_ APPLETALK Socket Options**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de Protocolo de administración de vínculos InfraRed. Para obtener más información, vea [**SOL \_ IRLMP Socket Options ( Opciones de socket de IRLMP de SOL).**](sol-irlmp-socket-options.md)


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOCKET \_ DE SOL**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de socket. Para obtener más información, vea [**SOL \_ SOCKET Socket Options**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Todas las opciones de socket de SO se aplican igualmente a \_ \* IPv4 e IPv6 (excepto SO BROADCAST, ya que la difusión no se \_ implementa en IPv6).

 

 




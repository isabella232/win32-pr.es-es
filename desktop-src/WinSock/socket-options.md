---
description: Página de navegación de las opciones de socket de Windows Sockets (Winsock).
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715111"
---
# <a name="socket-options"></a>Opciones de socket

En esta sección se describen las opciones de socket de Winsock para diversas ediciones de sistemas operativos Windows. Use [**las funciones**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de la opción de socket para obtener más opciones de socket. Para enumerar los protocolos y detectar las propiedades compatibles para cada protocolo instalado, utilice la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

Algunas opciones de socket requieren más explicación de lo que pueden transmitir estas tablas; Estas opciones contienen vínculos a páginas adicionales.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel IPv4. Para obtener más información, consulte [**las \_ Opciones de socket IP IPPROTO**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel IPv6. Para obtener más información, consulte [**IPPROTO \_ IPv6 socket Options**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de multidifusión confiable. Para obtener más información, consulte [**las \_ Opciones de socket de RM de IPPROTO**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de TCP. Para obtener más información, consulte [**las \_ Opciones de socket TCP de IPPROTO**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de UDP. Para obtener más información, consulte [**las \_ Opciones de socket UDP de IPPROTO**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de IPX. Para obtener más información, consulte [**las \_ Opciones de socket IPX NSPROTO**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**de SOL con \_ APPLETALK**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de AppleTalk. Para obtener más información, consulte [**las \_ Opciones de socket de APPLETALK de Apple**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de protocolo de administración de vínculos de infrarrojos. Para obtener más información, consulte [**las \_ Opciones de socket IRLMP de sol**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_socket sol**
</dt> <dd> <dl> <dt>



Opciones de socket aplicables en el nivel de socket. Para obtener más información, consulte [**las \_ Opciones de socket de socket sol**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Todas \_ \* las opciones de socket se aplican por igual a IPv4 e IPv6 (excepto por el caso de la \_ difusión, ya que la difusión no se implementa en IPv6).

 

 




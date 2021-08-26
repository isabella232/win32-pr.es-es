---
description: La API del proveedor de espacios de nombres PNRP usa las siguientes funciones.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Funciones PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f109684be61bf1a9a194acb89b22fd4a50be652a6615a18a789e157ca2a5d909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034385"
---
# <a name="pnrp-functions"></a>Funciones PNRP

La API del proveedor de espacios de nombres PNRP usa las siguientes funciones.



| Función                                                             | Descripción                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codifica el nombre del mismo nivel proporcionado como un formato que se puede usar con una llamada posterior a la función [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets. |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Descodifica un nombre de host devuelto por [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) en la cadena de nombre de mismo nivel que representa.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Inicia el servicio protocolo de resolución de nombres del mismo nivel (PNRP) para el par que realiza la llamada.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Cierra una instancia en ejecución del servicio del Protocolo de resolución de nombres del mismo nivel (PNRP) y libera todos los recursos asociados a él.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registra un par con una nube PNRP y devuelve un identificador que se puede usar para las actualizaciones de registro.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Actualiza la información de registro pnrp de un nombre.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Anula el registro de un par de una nube PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Obtiene las direcciones de punto de conexión registradas para un nombre del mismo nivel específico.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Inicia una operación asincrónica de resolución de nombres del mismo nivel.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Recupera información sobre las nubes del Protocolo de resolución de nombres del mismo nivel (PNRP) en las que participa el par que realiza la llamada.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Cierra el identificador de una operación asincrónica de resolución PNRP iniciada con una llamada anterior a [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Inicia el proceso que permite a una aplicación resolver nombres y enumerar nubes de red.                                                                 |
| [PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Finaliza una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                             |
| [PNRP y WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Coincide con las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                                |
| [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Recibe notificaciones sobre los cambios en la lista de nube de red y la disponibilidad de los resultados de una solicitud de resolución de nombres.                                     |
| [PNRP y WSASetService](pnrp-and-wsasetservice.md)                 | Registra o quita nombres del [mismo nivel.](peer-names.md)                                                                                                           |



 

 

 

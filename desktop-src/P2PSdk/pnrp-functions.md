---
description: La API del proveedor de espacio de nombres PNRP utiliza las siguientes funciones.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Funciones PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667387"
---
# <a name="pnrp-functions"></a>Funciones PNRP

La API del proveedor de espacio de nombres PNRP utiliza las siguientes funciones.



| Función                                                             | Descripción                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codifica el nombre de mismo nivel proporcionado como un formato que se puede usar con una llamada subsiguiente a la función de Windows Sockets [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Descodifica un nombre de host devuelto por [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) en la cadena de nombre del mismo nivel que representa.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Inicia el servicio del Protocolo de resolución de nombres de mismo nivel (PNRP) para el elemento del mismo nivel que realiza la llamada.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Cierra una instancia en ejecución del servicio de protocolo de resolución de nombres de mismo nivel (PNRP) y libera todos los recursos asociados a él.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registra un elemento del mismo nivel con una nube PNRP y devuelve un identificador que se puede usar para las actualizaciones de registro.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Actualiza la información de registro de PNRP para un nombre.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Anula el registro de un elemento del mismo nivel desde una nube PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Obtiene las direcciones de punto de conexión registradas para un nombre de mismo nivel específico.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Inicia una operación asincrónica de resolución de nombres del mismo nivel.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Recupera información sobre las nubes del Protocolo de resolución de nombres de mismo nivel (PNRP) en las que participa el elemento del mismo nivel que realiza la llamada.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Cierra el identificador de una operación de resolución PNRP asincrónica iniciada con una llamada anterior a [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Inicia el proceso que permite a una aplicación resolver nombres y enumerar nubes de red.                                                                 |
| [PNRP y WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Finaliza una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                             |
| [PNRP y WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Coincide con las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                                |
| [PNRP y WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Recibe notificaciones sobre los cambios en la lista de nube de red y la disponibilidad de los resultados de una solicitud de resolución de nombres.                                     |
| [PNRP y WSASetService](pnrp-and-wsasetservice.md)                 | Registra o quita [nombres de mismo nivel](peer-names.md).                                                                                                           |



 

 

 

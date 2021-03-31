---
title: Funciones de servidor de servicios de implementación de Windows
description: Las siguientes funciones se usan con la API del servidor PXE de servicios de implementación de Windows.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419047"
---
# <a name="windows-deployment-services-server-functions"></a>Funciones de servidor de servicios de implementación de Windows

Las siguientes funciones se usan con la API del servidor PXE de servicios de implementación de Windows.



| Función                                                           | Descripción                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Devuelve los resultados asincrónicos de la solicitud de cliente.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Anexa una opción DHCP al paquete de respuesta.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Anexa una opción DHCP al paquete de respuesta.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Recupera un valor de opción de un paquete DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Recupera un valor de opción del campo de información específica del proveedor (43) de un paquete DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Inicializa un paquete de respuesta como un paquete de respuesta DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Valida que un paquete es un paquete DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Devuelve información acerca del servidor PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Asigna un paquete que se va a enviar con la función [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) .                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libera un paquete asignado por la función [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) .                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Cierra la enumeración de los proveedores abiertos por la función [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) .               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Inicia una enumeración de proveedores registrados.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Enumera los proveedores registrados.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libera la memoria asignada por la función [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) .                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Devuelve el índice del proveedor especificado en la lista de proveedores registrados.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Se le llama cuando se recibe una solicitud de un cliente.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registra un proveedor con el sistema.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Se llama cuando el servicio WDS recibe un código de control de servicio.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Especifica los atributos del proveedor.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Se llama para cerrar el proveedor.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Quita un proveedor de la lista de proveedores registrados.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registra funciones de devolución de llamada para diferentes eventos de notificación.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Envía un paquete a una solicitud de cliente.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Agrega una entrada de seguimiento al registro de PXE.                                                                                             |



 

Lo siguiente está disponible a partir de Windows 8 y Windows Server 2012.

| Función                                                               | Descripción                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Anexa una opción DHCPv6 al paquete de respuesta.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Anexa una opción DHCPv6 al paquete de respuesta.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Recupera un valor de opción de un paquete DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Recupera los valores de opción del \_ campo Option VENDOR \_ OPC (17) de un paquete DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Inicializa un paquete de respuesta como un paquete de respuesta DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Valida que un paquete es un paquete DHCPv6 válido.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Devuelve información acerca del servidor PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Permite que un proveedor analice los mensajes de retransmisión-FORW y sus \_ mensajes de mensaje de retransmisión de opción anidados \_ . |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Genera un mensaje de REPL de retransmisión.                                                               |



 

 

 





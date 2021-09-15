---
title: Windows Funciones del servidor de Servicios de implementación
description: Las siguientes funciones se usan con Windows DEPLOYMENT Services PXE Server API.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569405"
---
# <a name="windows-deployment-services-server-functions"></a>Windows Funciones del servidor de Servicios de implementación

Las siguientes funciones se usan con Windows DEPLOYMENT Services PXE Server API.



| Función                                                           | Descripción                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Devuelve los resultados asincrónicos de la solicitud de cliente.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Anexa una opción DHCP al paquete de respuesta.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Anexa una opción DHCP al paquete de respuesta.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Recupera un valor de opción de un paquete DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Recupera un valor de opción del campo Información específica del proveedor (43) de un paquete DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Inicializa un paquete de respuesta como un paquete de respuesta DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Valida que un paquete es un paquete DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Devuelve información sobre el servidor PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Asigna un paquete que se va a enviar con [**la función PxeSendReply.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libera un paquete asignado por la [**función PxePacketAllocate.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Cierra la enumeración de proveedores abierta por la [**función PxeProviderEnumFirst.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Inicia una enumeración de proveedores registrados.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Enumera los proveedores registrados.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libera la memoria asignada por la [**función PxeProviderEnumNext.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Exportación desde una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Devuelve el índice del proveedor especificado en la lista de proveedores registrados.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Se llama cuando se recibe una solicitud de un cliente.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registra un proveedor con el sistema.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Se llama cuando el servicio WDS recibe un código de control de servicio.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Especifica atributos para el proveedor.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Se llama para apagar el proveedor.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Quita un proveedor de la lista de proveedores registrados.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registra funciones de devolución de llamada para distintos eventos de notificación.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Envía un paquete a una solicitud de cliente.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Agrega una entrada de seguimiento al registro PXE.                                                                                             |



 

Lo siguiente está disponible a partir de Windows 8 y Windows Server 2012.

| Función                                                               | Descripción                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Anexa una opción DHCPv6 al paquete de respuesta.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Anexa una opción DHCPv6 al paquete de respuesta.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Recupera un valor de opción de un paquete DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Recupera los valores de opción del campo OPTION \_ VENDOR \_ OPTS (17) de un paquete DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Inicializa un paquete de respuesta como un paquete de respuesta DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Valida que un paquete es un paquete DHCPv6 válido.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Devuelve información sobre el servidor PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Permite a un proveedor analizar los mensajes RELAY-FORW y sus mensajes OPTION \_ RELAY \_ MSG anidados. |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Genera un mensaje RELAY-REPL.                                                               |



 

 

 





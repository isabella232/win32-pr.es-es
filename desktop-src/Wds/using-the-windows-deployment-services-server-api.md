---
title: Uso de la API de servidor de Servicios de implementación de Windows
description: En entornos en los que no se puede usar la solución estándar Windows Deployment Services (WDS), el servidor WDS expone una API que permite a los desarrolladores escribir complementos, denominados proveedores, para controlar las solicitudes del entorno de ejecución previo al arranque (PXE).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows Deployment Services Windows Deployment Services , mediante la API de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ce7516e5279fecdfeecfa90edd8e3a0dad265562fa5ea59336367dbe157c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999575"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Uso de la API de servidor de Servicios de implementación de Windows

En entornos en los que no se puede usar la solución estándar Windows Deployment Services (WDS), el servidor WDS expone una API que permite a los desarrolladores escribir complementos, denominados proveedores, para controlar las solicitudes del entorno de ejecución previo al arranque (PXE). Los desarrolladores deben cumplir las siguientes directrices al escribir proveedores PXE para WDS.

## <a name="install-the-wds-role-on-the-server"></a>Instalar el rol WDS en el servidor

-   Windows Deployment Services (WDS) es la versión revisada de Servicios de instalación remota (RIS), necesitará el rol de servidor WDS para implementar el servidor PXE wds y los proveedores.
-   WDS reemplaza RIS como componente estándar a partir de Windows Server 2008 y Windows Server 2003 por Service Pack 2 (SP2).
-   Debe actualizar el servidor RIS a WDS en Windows Server 2003 con Service Pack 1 (SP1). Puede instalar el rol de servidor WDS con Windows [Automated Installation Kit (WAIK).](https://www.microsoft.com/download/details.aspx?id=10333)

## <a name="register-providers"></a>Registrar proveedores

-   Registre la biblioteca de vínculos dinámicos (DLL) del proveedor durante su instalación e inserte el proveedor en la lista ordenada de proveedores registrados.
    > [!Note]  
    > Al instalar un proveedor nuevo o modificado, deberá reiniciar el servicio PXE de WDS para que los cambios sumen efecto.

     

-   Use la [**función PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) para registrar el proveedor y agregarlo a la lista. Use la [**función PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) para anular el registro de un proveedor registrado y quitarlo de la lista.
-   Especifique la secuencia del proveedor en la lista ordenada. No se puede garantizar el índice de un proveedor de la lista porque otro proveedor puede registrarse más adelante antes que él. Para insertar el proveedor en la lista antes o después de otro proveedor registrado, use primero la función [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) para obtener el índice del proveedor registrado y, a continuación, registre el nuevo proveedor mientras especifica un valor de índice mayor o menor.
-   La instalación puede almacenar información de configuración del proveedor en la clave del Registro devuelta cuando se registra el proveedor. *PhProviderKey* de [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister)recibe la dirección de la clave del Registro. El proveedor recibe un identificador para esta misma clave que el *parámetro hProviderKey* para su devolución de llamada [*PxeProviderInitialize.*](pxeproviderinitialize.md) El proveedor debe almacenar la dirección de esta clave.
-   Instale siempre la biblioteca de vínculos dinámicos (DLL) del proveedor en la carpeta Archivos de programa del servidor.

## <a name="initialize"></a>Inicialización

-   Incluya un archivo DLL que exporte la función de devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) en el proveedor. Cada proveedor requiere una *devolución de llamada PxeProviderInitialize.* Cuando WDS carga un proveedor, llama a la función *PxeProviderInitialize* del proveedor y pasa un identificador a la misma clave que se usa para almacenar información de configuración durante el registro del proveedor.
-   Cuando la devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) devuelve y se realiza correctamente, el proveedor debe inicializarse completamente y estar listo para procesar las solicitudes.
-   Registre cada devolución de llamada en el proveedor durante el procesamiento de [*la función PxeProviderInitialize.*](pxeproviderinitialize.md) Las devoluciones de llamada deben registrarse con la [**función PxeRegisterCallback.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback)
-   Inicialice todos los recursos internos del proveedor dentro del procesamiento de su [*función PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="shutdown"></a>Apagar

-   Implemente la [*devolución de llamada PxeProviderShutdown.*](pxeprovidershutdown.md) Cada proveedor debe tener una devolución *de llamada PxeProviderShutdown.*
-   La función de devolución de [*llamada PxeProviderShutdown*](pxeprovidershutdown.md) debe apagar completamente el proveedor y liberar todos sus recursos.
-   Una vez que se devuelve la devolución de llamada [*PxeProviderShutdown,*](pxeprovidershutdown.md) el identificador *hProvider* pasado a la [*función PxeProviderInitialize*](pxeproviderinitialize.md) ya no es válido y no se debe usar para llamar a WDS.
-   Registre la devolución de llamada [*PxeProviderShutdown*](pxeprovidershutdown.md) llamando a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK \_ SHUTDOWN** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize.*](pxeproviderinitialize.md) No llame a la devolución *de llamada PxeProviderShutdown* si se produce un error en la *función PxeProviderInitialize.*

## <a name="handle-request-packet"></a>Controlar el paquete de solicitud

Implemente la [*devolución de llamada PxeProviderRecvRequest*](pxeproviderrecvrequest.md) para el proveedor. Cada proveedor debe tener una devolución *de llamada PxeProviderRecvRequest.* Cuando WDS recibe una solicitud, llama a la devolución de llamada *PxeProviderRecvRequest* para el primer proveedor de la lista de proveedores registrados.

-   Si el proveedor procesará esta solicitud de forma sincrónica, la [*función PxeProviderRecvRequest*](pxeproviderrecvrequest.md) debe devolver un valor **de ERROR \_ SUCCESS**. Si y solo si el proveedor procesará esta solicitud de forma asincrónica, la devolución de llamada *PxeProviderRecvRequest* debe devolver **ERROR IO \_ \_ PENDING** y llamar a la [**función PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) cuando se haya procesado la solicitud.
-   La devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) y la función [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) devuelven la dirección de una enumeración DE ACCIÓN DE **\_ ARRANQUE \_ PXE** que describe la acción realizada por el proveedor para controlar la solicitud.

    Hay cuatro maneras de que un proveedor controle una solicitud:

    -   El proveedor responde al cliente con un paquete de respuesta DHCP estándar que contiene una ruta de acceso al programa de arranque de red. Devolver el valor **PXE \_ BA \_ NBP** de la enumeración significa que el proveedor ha procesado correctamente el paquete de solicitud y completado la solicitud mediante el envío de un paquete de respuesta mediante una llamada a las funciones [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) y [**PxeSendReply.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply)
    -   El proveedor responde al cliente con un paquete de respuesta personalizado que no se ajusta a DHCP. Devolver el valor **PXE \_ BA \_ CUSTOM** para la enumeración significa que el proveedor ha procesado correctamente el paquete de solicitud y completado la solicitud mediante el envío de un paquete de respuesta personalizado mediante una llamada a las funciones [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) y [**PxeSendReply.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply)
    -   El proveedor determina que se debe omitir la solicitud. Devolver el **valor PXE \_ BA \_ IGNORE** para la enumeración significa que el proveedor ha liberado todos los recursos asociados a la solicitud y la solicitud no se pasa al siguiente proveedor de la lista de proveedores registrados. Los proveedores pueden usar esta opción si detectan que un paquete de solicitud no es válido.
    -   El proveedor rechaza dar servicio a la solicitud. Si se devuelve el valor **\_ PXE BA \_ REJECT** de la enumeración, se indica al sistema que pase la solicitud al siguiente proveedor de la lista de proveedores registrados. Si se trata del último proveedor de la lista, se liberan todos los recursos asociados a la solicitud y se omite la solicitud.
    -   Registre la devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) llamando a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK \_ RECV \_ REQUEST** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="generate-response-packet"></a>Generar paquete de respuesta

-   Use la API para escribir proveedores para controlar la solicitud DHCP y generar paquetes de respuesta.
-   La [**función PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) especifica los atributos utilizados por el proveedor para filtrar paquetes. Los atributos del proveedor se pueden especificar para que el proveedor vea todos los paquetes, el proveedor solo vea paquetes DHCP o el proveedor solo vea paquetes DHCP que especifiquen la opción Identificador de clase de proveedor DHCP (60) como "PXEClient".
-   La [**función PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) comprueba que un paquete es un paquete DHCP válido. Los proveedores pueden usar la función **PxeDhcpIsValid** para comprobar si un paquete del cliente es un paquete DHCP cuando el filtro establecido con la función [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) está establecido para recibir todos los paquetes para determinar si un paquete especificado es un paquete DHCP válido.
-   La [**función PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) inicializa un paquete de respuesta como un paquete de respuesta DHCP que se basa en la información de un paquete recibido del cliente. La [*función PxeProviderInitialize*](pxeproviderinitialize.md) toma la dirección de un paquete DHCP válido recibido del cliente en la devolución de [*llamada PxeProviderRecvRequest.*](pxeproviderrecvrequest.md) La **función PxeDhcpInitialize** toma un puntero a un paquete de respuesta asignado con la [**función PxePacketAllocate.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate)
-   La [**función PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) recupera un valor de opción de un paquete DHCP. La [**función PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) recupera un valor de opción del campo Información específica del proveedor (43) de un paquete DHCP.
-   A continuación, el proveedor puede rellenar el paquete de respuesta con información y usar la [**función PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar el paquete de respuesta al cliente. La [**función PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) anexa una opción DHCP al paquete de respuesta.
-   Un proveedor que responda a las solicitudes de cliente mediante el envío de un paquete debe asignar el paquete de respuesta mediante la [**función PxePacketAllocate.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) A continuación, el proveedor puede rellenar el paquete de respuesta con información y usar la [**función PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar el paquete de respuesta al cliente.
-   Cuando la memoria asignada ya no sea necesaria, el proveedor debe liberarla mediante la [**función PxePacketFree.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree)

## <a name="enumerate-registered-providers"></a>Enumerar proveedores registrados

-   Use la API para escribir proveedores que enumeren y comprueben otros proveedores registrados en la lista.
-   La [**función PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) devuelve información sobre el servidor PXE. La **función PxeGetServerInfo** devuelve **un valor BOOL** que indica si el seguimiento está habilitado para el servidor. **TRUE** indica que el seguimiento está habilitado.
-   La [**función PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) inicia una enumeración de proveedores en la lista de proveedores registrados. La **función PxeProviderEnumFirst** inicia la enumeración y devuelve la dirección del identificador que se debe usar al llamar a la [**función PxeProviderEnumNext.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) La **función PxeProviderEnumNext** devuelve una [**estructura PROVIDER \_ de PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) que contiene la información sobre el proveedor. La [**función PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libera la memoria que la **función PxeProviderEnumNext** ha asignado para la estructura PROVIDER de **PXE. \_** La [**función PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) cierra la enumeración de proveedores en la lista de proveedores registrados.

## <a name="handle-service-control-codes"></a>Controlar códigos de control de servicio

-   Cuando se recibe un mensaje de control de servicio, WDS llama a la devolución [*de llamada PxeProviderServiceControl.*](pxeproviderservicecontrol.md)
-   El proveedor puede definir una función de [*devolución de llamada PxeProviderServiceControl*](pxeproviderservicecontrol.md) para controlar los mensajes de control de servicio.
-   Registre la devolución de llamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) llamando a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK \_ SERVICE \_ CONTROL** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="add-trace-entries-to-pxe-log"></a>Agregar entradas de seguimiento al registro PXE

-   La [**función PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) agrega una entrada de seguimiento al registro PXE. WDSPXE proporciona seguimiento para ayudar a los administradores a solucionar problemas. Los proveedores pueden registrar entradas de seguimiento de diferentes niveles de gravedad. Los administradores pueden configurar WDSPXE para registrar solo entradas para determinados niveles de gravedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API Windows Deployment Services](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso de la API de cliente de Servicios de implementación de Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 





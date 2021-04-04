---
title: Uso de la API de servidor de Servicios de implementación de Windows
description: En entornos donde no se puede usar la solución estándar de servicios de implementación de Windows (WDS), el servidor WDS expone una API que permite a los desarrolladores escribir complementos, denominados proveedores, para controlar las solicitudes del entorno de ejecución previo al arranque (PXE).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Servicios de implementación de Windows servicios de implementación de Windows mediante la API de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3634dffa73eddc9b5db92be6bc807cccbc5248f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789340"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Uso de la API de servidor de Servicios de implementación de Windows

En entornos donde no se puede usar la solución estándar de servicios de implementación de Windows (WDS), el servidor WDS expone una API que permite a los desarrolladores escribir complementos, denominados proveedores, para controlar las solicitudes del entorno de ejecución previo al arranque (PXE). Los desarrolladores deben cumplir las siguientes directrices al escribir proveedores de PXE para WDS.

## <a name="install-the-wds-role-on-the-server"></a>Instalación del rol de WDS en el servidor

-   Servicios de implementación de Windows (WDS) es la versión revisada de los servicios de instalación remota (RIS). necesitará el rol de servidor de WDS para implementar el servidor PXE y los proveedores de WDS.
-   WDS reemplaza a RIS como componente estándar a partir de Windows Server 2008 y Windows Server 2003 con Service Pack 2 (SP2).
-   Debe actualizar el servidor de RIS a WDS en Windows Server 2003 con Service Pack 1 (SP1). Puede instalar el rol de servidor de WDS con el [Kit de instalación automatizada de Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="register-providers"></a>Registrar proveedores

-   Registre la biblioteca de vínculos dinámicos (DLL) del proveedor durante su instalación e inserte el proveedor en la lista ordenada de proveedores registrados.
    > [!Note]  
    > Al instalar un proveedor nuevo o modificado, deberá reiniciar el servicio PXE de WDS para que los cambios surtan efecto.

     

-   Utilice la función [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) para registrar el proveedor y agregarlo a la lista. Use la función [**PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) para anular el registro de un proveedor registrado y quitarlo de la lista.
-   Especifique la secuencia del proveedor en la lista ordenada. No se puede garantizar el índice de un proveedor de la lista porque es posible que otro proveedor se registre más adelante antes. Para insertar el proveedor en la lista antes o después de otro proveedor registrado, utilice primero la función [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) para obtener el índice del proveedor registrado y, a continuación, registre el nuevo proveedor mientras especifica un valor de índice mayor o menor.
-   La instalación puede almacenar la información de configuración del proveedor en la clave del registro devuelta cuando se registra el proveedor. El *phProviderKey* de [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister)recibe la dirección de la clave del registro. El proveedor recibe un identificador a esta misma clave que el parámetro *hProviderKey* en su devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) . El proveedor debe almacenar la dirección de esta clave.
-   Instale siempre la biblioteca de vínculos dinámicos (DLL) del proveedor en la carpeta archivos de programa del servidor.

## <a name="initialize"></a>Inicialización

-   Incluya un archivo DLL que exporte la función de devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) en el proveedor. Cada proveedor requiere una devolución de llamada *PxeProviderInitialize* . Cuando WDS carga un proveedor, llama a la función *PxeProviderInitialize* del proveedor y pasa un identificador a la misma clave que se utiliza para almacenar la información de configuración durante el registro del proveedor.
-   Cuando la devolución de llamada de [*PxeProviderInitialize*](pxeproviderinitialize.md) devuelve y se realiza correctamente, el proveedor debe inicializarse completamente y estar listo para procesar solicitudes.
-   Registre todas las devoluciones de llamada en el proveedor durante el procesamiento de la función [*PxeProviderInitialize*](pxeproviderinitialize.md) . Las devoluciones de llamada se deben registrar con la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) .
-   Inicialice todos los recursos internos del proveedor en el procesamiento de su función [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="shutdown"></a>Apagar

-   Implemente la devolución de llamada [*PxeProviderShutdown*](pxeprovidershutdown.md) . Cada proveedor debe tener una devolución de llamada *PxeProviderShutdown*.
-   La función de devolución de llamada [*PxeProviderShutdown*](pxeprovidershutdown.md) debe cerrar completamente el proveedor y liberar todos sus recursos.
-   Después de que la devolución de llamada de [*PxeProviderShutdown*](pxeprovidershutdown.md) vuelva, el identificador de *hProvider* pasado a la función [*PxeProviderInitialize*](pxeproviderinitialize.md) ya no es válido y no debe usarse para llamar a WDS.
-   Registre la devolución de llamada de [*PxeProviderShutdown*](pxeprovidershutdown.md) llamando a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el apagado de la **devolución de \_ llamada \_ PXE** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) . No llame a la devolución de llamada *PxeProviderShutdown* si se produce un error en la función *PxeProviderInitialize* .

## <a name="handle-request-packet"></a>Controlar el paquete de solicitud

Implemente la devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) para el proveedor. Cada proveedor debe tener una devolución de llamada *PxeProviderRecvRequest* . Cuando WDS recibe una solicitud, llama a la devolución de llamada *PxeProviderRecvRequest* para el primer proveedor de la lista de proveedores registrados.

-   Si el proveedor va a procesar esta solicitud de forma sincrónica, la función [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) debe devolver un valor de **error \_ Success**. Si y solo si el proveedor va a procesar esta solicitud de forma asincrónica, la devolución de llamada de *PxeProviderRecvRequest* debe devolver el **error de \_ e/s \_ pendiente** y llamar a la función [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) cuando se ha procesado la solicitud.
-   La devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) y la función [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) devuelven la dirección de una enumeración de **\_ \_ acción de arranque PXE** que describe la acción realizada por el proveedor para controlar la solicitud.

    Hay cuatro maneras de que un proveedor administre una solicitud:

    -   El proveedor responde al cliente con un paquete de respuesta DHCP estándar que contiene una ruta de acceso al programa de arranque de red. La devolución del valor **\_ \_ NBP** de la cuenta de PXE para la enumeración significa que el proveedor ha procesado correctamente el paquete de solicitud y ha completado la solicitud mediante el envío de un paquete de respuesta llamando a las funciones [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) y [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   El proveedor responde al cliente con un paquete de respuesta personalizado que no se ajusta a DHCP. Devolver el **valor \_ \_ personalizado** de la BA de PXE para la enumeración significa que el proveedor ha procesado correctamente el paquete de solicitud y ha completado la solicitud mediante el envío de un paquete de respuesta personalizado mediante una llamada a las funciones [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) y [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   El proveedor determina que la solicitud se debe omitir. Devolver el **valor \_ \_ Ignore de PXE BA** para la enumeración significa que el proveedor ha liberado todos los recursos asociados a la solicitud y la solicitud no se pasa al siguiente proveedor de la lista de proveedores registrados. Los proveedores pueden usar esta opción si detectan que un paquete de solicitud no es válido.
    -   El proveedor declina el servicio de la solicitud. La devolución del valor de **\_ \_ rechazo** de la instancia de PXE para la enumeración indica al sistema que pase la solicitud al siguiente proveedor de la lista de proveedores registrados. Si este era el último proveedor de la lista, libera todos los recursos asociados a la solicitud y se omite la solicitud.
    -   Registre la devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) llamando a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con la **\_ \_ \_ solicitud de devolución de llamada PXE** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="generate-response-packet"></a>Generar paquete de respuesta

-   Use la API para escribir proveedores con el fin de controlar las solicitudes DHCP y generar paquetes de respuesta.
-   La función [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) especifica los atributos utilizados por el proveedor para filtrar los paquetes. Se pueden especificar los atributos del proveedor para que el proveedor vea todos los paquetes, el proveedor solo ve paquetes DHCP, o el proveedor solo ve los paquetes DHCP que especifican la opción de identificador de clase de proveedor DHCP (60) como "PXEClient".
-   La función [**PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) comprueba que un paquete es un paquete DHCP válido. Los proveedores pueden usar la función **PxeDhcpIsValid** para comprobar si un paquete del cliente es un paquete DHCP cuando el filtro establecido con la función [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) se establece para recibir todos los paquetes y determinar si un paquete especificado es un paquete DHCP válido.
-   La función [**PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) Inicializa un paquete de respuesta como un paquete de respuesta DHCP que se basa en la información de un paquete recibido del cliente. La función [*PxeProviderInitialize*](pxeproviderinitialize.md) toma la dirección de un paquete DHCP válido recibido del cliente en la devolución de llamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) . La función **PxeDhcpInitialize** toma un puntero a un paquete de respuesta asignado con la función [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) .
-   La función [**PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) recupera un valor de opción de un paquete DHCP. La función [**PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) recupera un valor de opción del campo de información específica del proveedor (43) de un paquete DHCP.
-   Después, el proveedor puede rellenar el paquete de respuesta con información y usar la función [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar el paquete de respuesta al cliente. La función [**PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) anexa una opción DHCP al paquete de respuesta.
-   Un proveedor que responde a las solicitudes de cliente mediante el envío de un paquete debe asignar el paquete de respuesta mediante la función [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) . Después, el proveedor puede rellenar el paquete de respuesta con información y usar la función [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar el paquete de respuesta al cliente.
-   Cuando ya no se necesita la memoria asignada, el proveedor debe liberarla mediante la función [**PxePacketFree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) .

## <a name="enumerate-registered-providers"></a>Enumerar proveedores registrados

-   Use la API para escribir proveedores que enumeran y comprueban otros proveedores registrados en la lista.
-   La función [**PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) devuelve información acerca del servidor PXE. La función **PxeGetServerInfo** devuelve un **booleano** que indica si el seguimiento está habilitado para el servidor. **True** indica que el seguimiento está habilitado.
-   La función [**PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) inicia una enumeración de proveedores en la lista de proveedores registrados. La función **PxeProviderEnumFirst** inicia la enumeración y devuelve la dirección del identificador que se debe usar al llamar a la función [**PxeProviderEnumNext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) . La función **PxeProviderEnumNext** devuelve una estructura de [**\_ proveedor PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) que contiene la información sobre el proveedor. La función [**PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libera la memoria asignada para la estructura del **\_ proveedor PXE** mediante la función **PxeProviderEnumNext** . La función [**PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) cierra la enumeración de proveedores en la lista de proveedores registrados.

## <a name="handle-service-control-codes"></a>Controlar códigos de control de servicio

-   Cuando se recibe un mensaje de control de servicio, WDS llama a la devolución de llamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) .
-   El proveedor puede definir una función de devolución de llamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) para controlar los mensajes de control de servicio.
-   Registre la devolución de llamada de [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) mediante una llamada a la función [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el **control de servicio de devolución de \_ llamada \_ \_ PXE** durante el procesamiento de la devolución de llamada [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="add-trace-entries-to-pxe-log"></a>Agregar entradas de seguimiento al registro PXE

-   La función [**PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) agrega una entrada de seguimiento al registro de PXE. WDSPXE proporciona seguimiento para ayudar a los administradores a solucionar problemas. Los proveedores pueden registrar entradas de seguimiento de distintos niveles de gravedad. Los administradores pueden configurar WDSPXE para que solo registren las entradas de determinados niveles de gravedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de servicios de implementación de Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso de la API de cliente de Servicios de implementación de Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 





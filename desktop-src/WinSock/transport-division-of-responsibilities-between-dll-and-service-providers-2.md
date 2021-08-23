---
description: En esta sección se proporciona información general sobre la división de responsabilidad entre los proveedores32.dll Ws2 \_ y los proveedores de servicios de transporte.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: División de responsabilidades de transporte entre dll y proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c256cb03bcc9e3f8746db5196c21fc2de0a8b157304a205587b275acc0bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733225"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>División de responsabilidades de transporte entre dll y proveedores de servicios

En esta sección se proporciona información general sobre la división de responsabilidad entre los proveedores32.dll Ws2 \_ y los proveedores de servicios de transporte.

## <a name="ws2_32dll-functionality-for-transport"></a>Funcionalidad de \_32.dll Ws2 para transporte

La tarea principal de la parte de transporte de datos de la32.dll Ws2 es actuar como administrador de tráfico entre proveedores \_ de servicios y aplicaciones. Con varios proveedores de servicios diferentes que interactúan con la misma aplicación, cada proveedor de servicios interactúa estrictamente con el Ws2 \_32.dll. El archivo DLL se encarga de:

-   Seleccionar un proveedor de servicios adecuado para crear sockets basados en una descripción del protocolo.
-   Reenvío de llamadas a procedimientos de aplicación que implican un socket al proveedor de servicios adecuado que creó o controla ese socket. Los proveedores de servicios no son conscientes de que algo de esto está ocurriendo.

No es necesario preocuparse por los detalles de la cooperación entre sí o incluso por la existencia de otros proveedores de servicios. Al abstraer los proveedores de servicios en una interfaz DLL coherente y realizar esta función de enrutamiento automático del tráfico, el32.dll de Ws2 permite a las aplicaciones interactuar con una variedad de proveedores sin necesidad de que las aplicaciones sean conscientes de las divisiones entre proveedores, donde se instalan proveedores \_ diferentes.

El32.dll Ws2 se basa en los parámetros de las funciones de creación de sockets de \_ API [**(socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket)**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)para determinar qué proveedor de servicios utilizar. El proveedor de servicios de transporte seleccionado se invocará a través de [**la función WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) En el caso de la función de **socket,** el32.dll de Ws2 busca la primera entrada en el conjunto de estructuras info de \_ [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) instaladas que coincide con los valores proporcionados en la tupla formada por los parámetros ( familia de direcciones , *tipo de socket*, *protocolo*). Para conservar la compatibilidad con versiones anteriores, el32.dll Ws2 trata el valor de cero para la familia de direcciones o el tipo de \_ *socket* como un valor comodín.  El valor de cero para el protocolo no se considera un valor comodín por el32.dll Ws2 a menos que este comportamiento se indique para un protocolo determinado al tener la marca PFL MATCHES PROTOCOL ZERO establecida en la estructura INFO de \_ \_ \_ \_ **WSAPROTOCOL. \_**

Para la [**función WSASocket,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) si se proporciona null para *lpProtocolInfo*, el comportamiento es exactamente como se describe para [**el socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). Sin embargo, si se hace referencia a una estructura INFO de [**WSAPROTOCOL, \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) el32.dll de Ws2 no realiza ninguna función de coincidencia, sino que retransmite inmediatamente la solicitud de creación de sockets al proveedor de servicios de transporte asociado a la estructura info de \_ **WSAPROTOCOL \_ indicada.** Los valores de la tupla ( familia de *direcciones,* tipo de *socket,*) se proporcionan intactos al proveedor de servicios en la [**función WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Los proveedores de servicios pueden omitir o prestar atención a los valores de los parámetros ( familia de *direcciones,* tipo  de *socket,*) según corresponda, pero no deben indicar una condición de error cuando el valor de familia de direcciones o tipo de *socket* es cero. Además, los proveedores de servicios no deben indicar una condición de error cuando la constante de manifiesto FROM PROTOCOL INFO está contenida en cualquiera de los parámetros ( familia de direcciones, tipo \_ \_ de *socket,*). Este valor simplemente indica que la aplicación desea usar los valores encontrados en los parámetros correspondientes de la estructura INFO de **WSAPROTOCOL: \_** (**iAddressFamily**, **iSocketType**, **iProtocol**).

Como parte de la creación de sockets, un proveedor de servicios informa a Ws232.dll sobre la asociación entre él mismo y el nuevo socket mediante los parámetros pasados a \_ [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) o [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). El Ws232.dll realiza un seguimiento de esta asociación entre \_ los identificadores de socket y proveedores de servicios determinados. Cada vez que se llama a una función de interfaz de aplicación que hace referencia a un identificador de socket, el32.dll Ws2 busca la asociación y llama a la función de interfaz del proveedor de servicios correspondiente del proveedor de \_ servicios adecuado.

Además de su servicio de enrutamiento de tráfico principal, el servicio Ws232.dll proporciona una serie de otros servicios, como la enumeración de protocolos, Administración de descriptores de socket (asignación, desasignación y asociación de valores de contexto) para proveedores de servicios que no son de sistema de archivos, administración de enlaces de bloqueo por subproceso, utilidades de intercambio de bytes, cola de llamadas a procedimiento asincrónico (APC) para facilitar la invocación de rutinas de finalización de E/S y negociación de versiones entre las aplicaciones y el32.dll de Ws2, así como entre los proveedores de servicios y \_ \_32.dll Ws2. \_

## <a name="transport-service-provider-functionality"></a>Funcionalidad del proveedor de servicios de transporte

Los proveedores de servicios implementan el protocolo de transporte real, que incluye funciones como la configuración de conexiones, la transferencia de datos, el control de flujo y el control de errores, etc. El proveedor de32.dll Ws2 no tiene ningún conocimiento sobre cómo se realizan las solicitudes a los proveedores de servicios; esto es lo que debe hacer la \_ implementación del proveedor de servicios. La implementación de estas funciones puede diferir en gran medida de un proveedor a otro. Los proveedores de servicios ocultan los detalles específicos de la implementación de cómo se logran las operaciones de red.

Los proveedores de servicios de transporte se pueden dividir ampliamente en dos categorías: aquellas cuyos descriptores de socket son identificadores reales del sistema de archivos (y, en adelante, se conocen como proveedores del sistema de archivos instalable (IFS); el resto se conocen como proveedores que no son IFS. El32.dll Ws2 siempre pasa el descriptor de socket del proveedor de servicios de transporte en hasta la aplicación sockets de Windows, por lo que las aplicaciones pueden aprovechar las ventajas de los descriptores de socket que son identificadores del sistema de archivos si así lo \_ eligen.

En resumen: los proveedores de servicios implementan los protocolos específicos de red de bajo nivel. El Ws232.dll proporciona la administración del tráfico de nivel medio que interconecta estos \_ protocolos de transporte con aplicaciones. A su vez, las aplicaciones proporcionan la directiva de cómo se usan estos flujos de tráfico y las operaciones específicas de la red para realizar las funciones deseadas por el usuario.

 

 

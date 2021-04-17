---
description: En esta sección se proporciona una visión general de la división de responsabilidad entre los \_ proveedores de servicios de transporte y32.dll Ws2.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: División del transporte de responsabilidades entre los proveedores de servicios y DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142ac98c95e95c310c2eefb7bfdaf1f70a03bf28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697482"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>División del transporte de responsabilidades entre los proveedores de servicios y DLL

En esta sección se proporciona una visión general de la división de responsabilidad entre los \_ proveedores de servicios de transporte y32.dll Ws2.

## <a name="ws2_32dll-functionality-for-transport"></a>\_Funcionalidad de32.dll de Ws2 para el transporte

La tarea principal de la parte de transporte de datos del \_32.dll Ws2 es actuar como Traffic Manager entre proveedores de servicios y aplicaciones. Con varios proveedores de servicios diferentes que interactúan con la misma aplicación, cada proveedor de servicios interactúa estrictamente con el \_32.dll Ws2. El archivo DLL se encarga de:

-   Seleccionar un proveedor de servicios adecuado para crear sockets basados en una descripción del protocolo.
-   Reenvío de llamadas a procedimientos de la aplicación que implican un socket al proveedor de servicios adecuado que creó o controla ese socket. Los proveedores de servicios no saben que esto ocurre.

No es necesario preocuparse de los detalles de la cooperabilidad entre sí o incluso de la existencia de otros proveedores de servicios. Mediante la abstracción de los proveedores de servicios en una interfaz de DLL coherente y la realización de esta función de enrutamiento de tráfico automática, la \_32.dll Ws2 permite a las aplicaciones interactuar con diversos proveedores sin necesidad de que las aplicaciones sean conscientes de las divisiones entre proveedores, donde se instalan proveedores diferentes.

El \_32.dll Ws2 se basa en los parámetros de las funciones de creación de sockets de API ( [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)) para determinar qué proveedor de servicios se va a emplear. El proveedor de servicios de transporte seleccionado se invocará a través de la función [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . En el caso de la función de **socket** , Ws2 \_32.dll encuentra la primera entrada en el conjunto de estructuras instaladas de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que coincide con los valores proporcionados en la tupla formada por los parámetros (*familia de direcciones*, tipo de *socket*, *Protocolo*). Para mantener la compatibilidad con versiones anteriores, Ws2 \_32.dll trata el valor de cero para la *familia de direcciones* o el *tipo de socket* como un valor comodín. El valor de cero para el Protocolo no se considera un valor comodín por el \_32.dll Ws2 a menos que se indique este comportamiento para un protocolo determinado al hacer que el PFL \_ coincida con la \_ \_ marca de protocolo cero establecida en la estructura de **\_ información de WSAPROTOCOL** .

En el caso de la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , si se proporciona null para *lpProtocolInfo*, el comportamiento es exactamente el mismo que se describe para [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). Sin embargo, si se hace referencia a una estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) , el32.dll de Ws2 \_ no realiza ninguna función coincidente, pero transmite inmediatamente la solicitud de creación de socket al proveedor de servicios de transporte asociado a la estructura de **\_ información WSAPROTOCOL** indicada. Los valores de la tupla (*familia de direcciones,* *tipo de socket,*) se proporcionan intactos al proveedor de servicios en la función [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . Los proveedores de servicios pueden omitir o prestar atención a los valores de los parámetros (*familia de direcciones,* *tipo de socket*) como corresponda, pero no deben indicar una condición de error cuando el valor de la *familia de direcciones* o el tipo de *socket* es cero. Además, los proveedores de servicios no deben indicar una condición de error cuando la constante del manifiesto de la \_ información del protocolo \_ está contenida en cualquiera de los parámetros (*familia de direcciones,* *tipo de socket*). Este valor simplemente indica que la aplicación desea usar los valores que se encuentran en los parámetros correspondientes de la estructura de **\_ información de WSAPROTOCOL** : (**iAddressFamily**, **iSocketType**, **iProtocol**).

Como parte de la creación de un socket, un proveedor de servicios informa al32.dll de Ws2 \_ sobre la asociación entre él mismo y el nuevo socket por medio de los parámetros pasados a [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) o [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). El \_32.dll Ws2 realiza un seguimiento de esta asociación entre los identificadores de socket y los proveedores de servicios concretos. Cada vez que se llama a una función de interfaz de aplicación que hace referencia a un identificador de socket, el \_32.dll Ws2 busca la asociación y llama a la función de interfaz del proveedor de servicios correspondiente del proveedor de servicios adecuado.

Además de su servicio de enrutamiento de tráfico principal, el \_32.dll Ws2 proporciona otros servicios, como enumeración de protocolos, administración de descriptores de sockets (asignación, desasignación y asociación del valor de contexto para proveedores de servicios que no son del sistema de archivos, administración de enlaces de bloqueo por subproceso, utilidades de intercambio de bytes, puesta en cola de llamadas a procedimiento asincrónicas (APC) para facilitar la invocación de rutinas de finalización de e/s y la negociación de la versión entre aplicaciones y el32.dll de Ws232.dll \_ \_

## <a name="transport-service-provider-functionality"></a>Funcionalidad del proveedor de servicios de transporte

Los proveedores de servicios implementan el protocolo de transporte real, que incluye funciones como la configuración de conexiones, la transferencia de datos, el control de flujo y el control de errores, etc. El \_32.dll Ws2 no tiene conocimiento sobre cómo se realizan las solicitudes a los proveedores de servicios; esto depende de la implementación del proveedor de servicios. La implementación de estas funciones puede diferir considerablemente de un proveedor a otro. Los proveedores de servicios ocultan los detalles específicos de la implementación de cómo se realizan las operaciones de red.

Los proveedores de servicios de transporte se pueden dividir ampliamente en dos categorías: aquellos cuyos descriptores de socket son identificadores del sistema de archivos reales (y a los que se hace referencia a continuación como proveedores del sistema de archivos instalables (IFS); el resto se conocen como proveedores que no son IFS. El \_32.dll Ws2 siempre pasa el descriptor de socket del proveedor de servicios de transporte a la aplicación de Windows Sockets, por lo que las aplicaciones pueden aprovechar las ventajas de los descriptores de socket que son identificadores del sistema de archivos si así lo desean.

En Resumen: los proveedores de servicios implementan los protocolos específicos de red de bajo nivel. El \_32.dll Ws2 proporciona la administración de tráfico de nivel medio que conecta estos protocolos de transporte con las aplicaciones. A su vez, las aplicaciones proporcionan la Directiva de cómo se usan estos flujos de tráfico y las operaciones específicas de la red para realizar las funciones deseadas por el usuario.

 

 

---
description: Un proveedor de espacios de nombres implementa una asignación de interfaz entre el SPI del espacio de nombres Winsock y la interfaz de programación nativa de un servicio de nombres existente como DNS, X. 500 o Servicios de directorio NetWare (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Proveedores de servicios de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e975c7ad0e5df29910624bb8f0b9d94fd24d9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648187"
---
# <a name="namespace-service-providers"></a>Proveedores de servicios de espacio de nombres

Un proveedor de espacios de nombres implementa una asignación de interfaz entre el SPI del espacio de nombres Winsock y la interfaz de programación nativa de un servicio de nombres existente como DNS, X. 500 o Servicios de directorio NetWare (NDS). Aunque un proveedor de espacios de nombres admite exactamente un espacio de nombres, es posible que se instalen varios proveedores para un espacio de nombres determinado. También es posible que un solo archivo DLL cree una instancia de varios proveedores de espacios de nombres. A medida que se instalan proveedores de espacios de nombres, se mantiene un catálogo de las estructuras de [**\_ información de WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) . Una aplicación puede utilizar [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) para detectar qué espacios de nombres se admiten en un equipo.

En Windows Vista y versiones posteriores, se proporcionan una estructura [**WSANAMESPACE \_ INFOEX**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) mejorada y una función [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) .

En las plataformas de 64 bits, se proporcionan funciones similares [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) y [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) para enumerar el catálogo de 32 bits.

Consulte [requisitos del proveedor de servicios de espacio de nombres Winsock](winsock-namespace-service-provider-requirements.md) para obtener información detallada.

## <a name="legacy-getxbyy-service-providers"></a>Proveedores de servicios GetXbyY heredados

Windows Sockets 2 es totalmente compatible con las funciones de resolución de nombres específicas de TCP/IP que se encuentran en la versión 1,1 de Windows Sockets. Para ello, incluye el conjunto de funciones **GetXbyY** en el SPI. Sin embargo, el tratamiento de este conjunto de funciones es algo diferente del resto de las funciones SPI. Las funciones **GetXbyY** que aparecen en el SPI están precedidas de GETXBYYSP \_ y se resumen en la tabla siguiente.

Funciones de estilo Berkeley



| Nombre de la función SPI           | Descripción                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Proporciona una estructura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para la dirección de host especificada.        |
| GETXBYYSP \_ gethostbyname    | Proporciona una estructura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para el nombre de host especificado.           |
| GETXBYYSP \_ getprotobyname   | Proporciona una estructura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para el nombre de protocolo especificado.     |
| GETXBYYSP \_ getprotobynumber | Proporciona una estructura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para el número de protocolo especificado.   |
| GETXBYYSP \_ getservbyname    | Proporciona una estructura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio especificado. e        |
| GETXBYYSP \_ getservbyport    | Proporciona una estructura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio en el puerto especificado. |
| GETXBYYSP \_ GetHostName (      | Devuelve el nombre de host estándar para el equipo local.                                   |



 

Funciones de estilo Async



| Nombre de la función SPI                   | Descripción                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Proporciona una estructura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para la dirección de host especificada.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Proporciona una estructura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para el nombre de host especificado.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Proporciona una estructura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para el nombre de protocolo especificado.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Proporciona una estructura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para el número de protocolo especificado.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Proporciona una estructura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) para el nombre de servicio especificado.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Proporciona una estructura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio en el puerto especificado. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Cancela una operación **GetXbyY** asincrónica.                                           |



 

La sintaxis y la semántica de estas funciones **GetXbyY** en el SPI son exactamente iguales que las documentadas en la especificación de la API y, por lo tanto, no se repiten aquí.

La DLL de Windows Sockets 2 permite que exactamente un proveedor de servicios ofrezca estos servicios. Por lo tanto, no es necesario incluir punteros a estas funciones en la tabla de procedimientos recibida de los proveedores de servicios en el inicio. En entornos Windows, la ruta de acceso al archivo DLL que implementa estas funciones se recupera del valor que se encuentra en la siguiente ruta de acceso del registro. Esta entrada del registro no existe de forma predeterminada:

**HKEY \_ \_** Parámetros de WinSock2 de \\ **sistema del** equipo local \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In proveedor de servicios GetXbyY predeterminado

Un proveedor de servicios de **GetXbyY** predeterminado se integra en los componentes estándar de tiempo de ejecución de Windows Sockets 2. Este proveedor predeterminado implementa todas las funciones anteriores, por lo que no es necesario para que las implemente cualquier proveedor de espacios de nombres. Sin embargo, un proveedor de espacios de nombres es gratuito para proporcionar cualquiera de estas funciones (y, por tanto, invalidar los valores predeterminados) simplemente almacenando la cadena que es la ruta de acceso al archivo DLL que implementa estas funciones en la clave del registro indicada. Cualquiera de las funciones de **GetXbyY** no exportadas por la dll de proveedor con nombre se proporcionará a través de los valores predeterminados integrados. Tenga en cuenta, sin embargo, que si un proveedor elige proporcionar cualquiera de las versiones asincrónicas de las funciones de **GetXbyY** , debe proporcionar todas las funciones asincrónicas para que la operación de cancelación funcione correctamente.

La implementación actual del proveedor de servicios **GetXbyY** predeterminado reside en el Wsock32.dll. En función de cómo se haya establecido la configuración de TCP/IP a través del panel de control, se producirá una resolución de nombres mediante los archivos de host local o DNS. Cuando se usa DNS, el proveedor de servicios de **GetXbyY** predeterminado utiliza las llamadas de API estándar de Windows sockets 1,1 para comunicarse con el servidor DNS. Estas transacciones se producirán con cualquier pila TCP/IP configurada como la pila TCP/IP predeterminada. Sin embargo, dos casos especiales merecen mención especial.

La implementación predeterminada de GETXBYYSP \_ GetHostName (obtiene el nombre de host local del registro. Se corresponderá con el nombre asignado a "Mi PC". La implementación predeterminada de GETXBYYSP \_ gethostbyname y GETXBYYSP \_ WSAAsyncGetHostByName siempre compara el nombre de host proporcionado con el nombre de host local. Si coinciden, la implementación predeterminada usa una interfaz privada para sondear la pila TCP/IP de Microsoft con el fin de detectar su dirección IP local. Por lo tanto, para ser totalmente independientes de la pila TCP/IP de Microsoft, un proveedor de espacios de nombres debe implementar GETXBYYSP \_ gethostbyname y GETXBYYSP \_ WSAAsyncGetHostByName.

 

 




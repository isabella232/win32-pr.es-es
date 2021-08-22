---
description: Un proveedor de espacios de nombres implementa una asignación de interfaz entre el SPI del espacio de nombres Winsock y la interfaz de programación nativa de un servicio de nombres existente, como DNS, X.500 o Servicios de directorio NetWare (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Proveedores de servicios de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e6ecc9ad0dcb9667bdd3d08049b9d41c3211de422cae0530506f6103494527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822643"
---
# <a name="namespace-service-providers"></a>Proveedores de servicios de espacio de nombres

Un proveedor de espacios de nombres implementa una asignación de interfaz entre el SPI del espacio de nombres Winsock y la interfaz de programación nativa de un servicio de nombres existente, como DNS, X.500 o Servicios de directorio NetWare (NDS). Aunque un proveedor de espacios de nombres admite exactamente un espacio de nombres, es posible que se instalen varios proveedores para un espacio de nombres determinado. También es posible que un solo archivo DLL cree una instancia de varios proveedores de espacios de nombres. A medida que se instalan los proveedores de espacios de nombres, se mantiene un catálogo de estructuras [**WSANAMESPACE \_ INFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) Una aplicación puede usar [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) para detectar qué espacios de nombres se admiten en un equipo.

En Windows Vista y versiones posteriores, se proporcionan una estructura [**\_ INFOEX mejorada de WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) y la función [**WSAEnumNameSpaceProvidersEx.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)

En plataformas de 64 bits, se proporcionan funciones [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) y [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) similares para enumerar el catálogo de 32 bits.

Consulte [Winsock Namespace Service Provider Requirements (Requisitos del proveedor](winsock-namespace-service-provider-requirements.md) de servicios del espacio de nombres Winsock) para obtener información detallada.

## <a name="legacy-getxbyy-service-providers"></a>Proveedores de servicios GetXbyY heredados

Windows Sockets 2 es totalmente compatible con las funciones de resolución de nombres específicas de TCP/IP que se encuentran en Windows Sockets versión 1.1. Para ello, incluye el conjunto de **funciones GetXbyY** en el SPI. Sin embargo, el tratamiento de este conjunto de funciones es algo diferente del resto de las funciones SPI. Las **funciones GetXbyY** que aparecen en el SPI van precedida de GETXBYYSP y se resumen \_ en la tabla siguiente.

Funciones de estilo de Berkeley



| Nombre de función SPI           | Descripción                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Proporciona una [**estructura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para la dirección de host especificada.        |
| GETXBYYSP \_ gethostbyname    | Proporciona una [**estructura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para el nombre de host especificado.           |
| GETXBYYSP \_ getprotobyname   | Proporciona una [**estructura de prototipos**](/windows/desktop/api/winsock/ns-winsock-protoent) para el nombre de protocolo especificado.     |
| GETXBYYSP \_ getprotobynumber | Proporciona una [**estructura de prototipos**](/windows/desktop/api/winsock/ns-winsock-protoent) para el número de protocolo especificado.   |
| GETXBYYSP \_ getservbyname    | Proporciona una [**estructura de servicio**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio especificado nam.e        |
| GETXBYYSP \_ getservbyport    | Proporciona una [**estructura de servicio**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio en el puerto especificado. |
| GETXBYYSP \_ gethostname      | Devuelve el nombre de host estándar del equipo local.                                   |



 

Funciones de estilo asincrónico



| Nombre de función SPI                   | Descripción                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Proporciona una [**estructura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para la dirección de host especificada.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Proporciona una [**estructura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para el nombre de host especificado.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Proporciona una [**estructura de prototipos**](/windows/desktop/api/winsock/ns-winsock-protoent) para el nombre de protocolo especificado.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Proporciona una [**estructura de prototipos**](/windows/desktop/api/winsock/ns-winsock-protoent) para el número de protocolo especificado.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Proporciona una [**estructura de servicio**](/windows/desktop/api/winsock/ns-winsock-servent) para el nombre de servicio especificado.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Proporciona una [**estructura de servicio**](/windows/desktop/api/winsock/ns-winsock-servent) para el servicio en el puerto especificado. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Cancela una operación **GetXbyY asincrónica.**                                           |



 

La sintaxis y semántica de estas funciones **GetXbyY** en spi son exactamente las mismas que las documentadas en la especificación de API y, por lo tanto, no se repiten aquí.

La dll Windows Sockets 2 permite que exactamente un proveedor de servicios ofrezca estos servicios. Por lo tanto, no es necesario incluir punteros a estas funciones en la tabla de procedimientos recibida de los proveedores de servicios en el inicio. En Windows entornos, la ruta de acceso al archivo DLL que implementa estas funciones se recupera del valor que se encuentra en la siguiente ruta de acceso del Registro. Esta entrada del Registro no existe de forma predeterminada:

**HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **WinSock2** \\ **Parameters** \\ **GetXByyLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In proveedor de servicios GetXbyY predeterminado

Un proveedor **de servicios GetXbyY predeterminado** se integra en los componentes estándar Windows Sockets 2 en tiempo de ejecución. Este proveedor predeterminado implementa todas las funciones anteriores, por lo que no es necesario que estas funciones las implemente ningún proveedor de espacios de nombres. Sin embargo, un proveedor de espacios de nombres puede proporcionar cualquiera o todas estas funciones (y, por tanto, invalidar los valores predeterminados) simplemente almacenando la cadena que es la ruta de acceso al archivo DLL que implementa estas funciones en la clave del Registro indicada. Cualquiera de las **funciones GetXbyY** no exportadas por el archivo DLL del proveedor con nombre se suministrará a través de los valores predeterminados integrados. Sin embargo, tenga en cuenta que si un proveedor decide proporcionar cualquiera de las versiones asincrónicas de las funciones **GetXbyY,** debe proporcionar todas las funciones asincrónicas para que la operación de cancelación funcione correctamente.

La implementación actual del proveedor de **servicios GetXbyY** predeterminado reside dentro del Wsock32.dll. En función de cómo se haya establecido la configuración de TCP/IP mediante Panel de control, la resolución de nombres se producirá mediante DNS o archivos host locales. Cuando se usa DNS, el proveedor de servicios **GetXbyY predeterminado** usa llamadas API estándar Windows Sockets 1.1 para comunicarse con el servidor DNS. Estas transacciones se producirán con cualquier pila TCP/IP configurada como pila TCP/IP predeterminada. Sin embargo, dos casos especiales merecen una mención especial.

La implementación predeterminada de GETXBYYSP \_ gethostname obtiene el nombre de host local del registro. Esto corresponderá al nombre asignado a "Mi PC". La implementación predeterminada de GETXBYYSP \_ gethostbyname y GETXBYYSP WSAAsyncGetHostByName siempre compara el nombre de host proporcionado con el nombre de \_ host local. Si coinciden, la implementación predeterminada usa una interfaz privada para sondear la pila TCP/IP de Microsoft con el fin de detectar su dirección IP local. Por lo tanto, para ser completamente independiente de la pila TCP/IP de Microsoft, un proveedor de espacios de nombres debe implementar GETXBYYSP \_ gethostbyname y GETXBYYSP \_ WSAAsyncGetHostByName.

 

 




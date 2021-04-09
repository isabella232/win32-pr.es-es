---
description: 'Las funciones de resolución de nombres se pueden agrupar en tres categorías: instalación del servicio, consultas de cliente y aplicación auxiliar (con macros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Resumen de las funciones de resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809698"
---
# <a name="summary-of-name-resolution-functions"></a>Resumen de las funciones de resolución de nombres

Las funciones de resolución de nombres se pueden agrupar en tres categorías: instalación del servicio, consultas de cliente y aplicación auxiliar (con macros). Las secciones siguientes identifican las funciones de cada categoría y describen brevemente su uso previsto. También se describen las estructuras de datos clave.

## <a name="service-installation"></a>Instalación del servicio

-   [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Cuando la clase de servicio necesaria todavía no existe, una aplicación utiliza [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) para instalar una nueva clase de servicio proporcionando un nombre de clase de servicio, un GUID para el identificador de clase de servicio y una serie de estructuras [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Estas estructuras son específicas de un espacio de nombres determinado y proporcionan valores comunes, como los números de puerto TCP recomendados o los identificadores de SAP SAP. Se puede quitar una clase de servicio llamando a [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) y proporcionando el GUID correspondiente al identificador de clase.

Una vez que existe una clase de servicio, se pueden instalar o quitar instancias específicas de un servicio a través de [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea). Esta función toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como parámetro de entrada junto con un código de operación y marcas de operación. El código de operación indica si el servicio se está instalando o quitando. La estructura **WSAQUERYSET** proporciona toda la información relevante sobre el servicio, incluido el identificador de clase de servicio, el nombre de servicio (para esta instancia), la información del protocolo y el identificador de espacio de nombres aplicable, y un conjunto de direcciones de transporte en el que el servicio realiza escuchas. Los servicios deben invocar **WSASetService** cuando se inicializan para anunciar su presencia en espacios de nombres dinámicos.

## <a name="client-query"></a>Consulta de cliente

-   [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

La función [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) permite a una aplicación detectar los espacios de nombres a los que se puede tener acceso a través de las funciones de resolución de nombres de Winsock. También permite que una aplicación determine si un espacio de nombres determinado es compatible con más de un proveedor de espacios de nombres y para detectar el identificador de proveedor para cualquier proveedor de espacio de nombres concreto. Mediante el uso de un identificador de proveedor, la aplicación puede restringir una operación de consulta a un proveedor de espacio de nombres especificado.

Espacio de nombres Winsock: las operaciones de consulta implican una serie de llamadas: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguidas de una o varias llamadas a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) y finalizando con una llamada a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **WSALookupServiceBegin** toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir los parámetros de consulta junto con un conjunto de marcas para proporcionar un mayor control sobre la operación de búsqueda. Devuelve un identificador de consulta que se utiliza en las llamadas subsiguientes a **WSALookupServiceNext** y **WSALookupServiceEnd**.

La aplicación llama a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) para obtener los resultados de la consulta, con los resultados proporcionados en un búfer de [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionado por la aplicación. La aplicación continúa llamando a **WSALookupServiceNext** hasta que se devuelve el código de error WSA \_ E, lo que indica que se han \_ \_ recuperado todos los resultados. La búsqueda se termina con una llamada a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). La función **WSALookupServiceEnd** también se puede usar para cancelar un **WSALookupServiceNext** pendiente actualmente cuando se llama desde otro subproceso.

En Windows Sockets 2, se definen códigos de error conflictivos para WSAENOMORE (10102) y WSA \_ e \_ no \_ más (10110). El código de error WSAENOMORE se quitará en una versión futura y solo \_ \_ \_ se conservará WSA E. En el caso de Windows Sockets 2, sin embargo, las aplicaciones deben comprobar tanto WSAENOMORE como WSA \_ e \_ no \_ más para la compatibilidad más amplia posible con proveedores de espacio de nombres que usan cualquiera de ellos.

## <a name="helper-functions"></a>Funciones del asistente

-   [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**WSAGetServiceClassInfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

Las funciones auxiliares de resolución de nombres incluyen una función para recuperar un nombre de clase de servicio a partir de un identificador de clase de servicio, un par de funciones que se usan para traducir una dirección de transporte entre una estructura [**SOCKADDR**](sockaddr-2.md) y una representación de cadena ASCII, una función para recuperar la información de esquema de la clase de servicio para una clase de servicio determinada y un conjunto de macros para asignar servicios

Las siguientes macros de WinSock2. h ayudan a asignar entre las clases de servicio conocidas y los espacios de nombres siguientes:

| Macro                                                                                                            | Descripción                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| SVCID \_ TCP (puerto) SVCID \_ UDP (puerto)<br/> SVCID \_ NetWare (tipo de objeto)<br/>                              | Dado un puerto para TCP/IP o UDP/IP, o el tipo de objeto en el caso de NetWare, devuelve el GUID (número de puerto en el orden del host). |
| IS \_ SVCID \_ TCP (GUID) \_ SVCID \_ UDP (GUID)<br/> ES \_ SVCID \_ NetWare (GUID)<br/>                          | Devuelve **true** si el GUID está dentro del intervalo permitido.                                                                |
| ESTABLECER \_ TCP \_ SVCID (GUID, puerto) establecer \_ UDP \_ SVCID (GUID, puerto)<br/>                                                | Inicializa una estructura GUID con el GUID equivalente para un número de puerto TCP o UDP (el número de puerto debe estar en el orden del host).    |
| Puerto \_ del \_ \_ puerto TCP de SVCID (GUID) \_ de \_ SVCID \_ UDP (GUID)<br/> SAPID \_ de \_ SVCID \_ NetWare (GUID)<br/> | Devuelve el puerto o el tipo de objeto asociado al GUID (número de puerto en el orden del host).                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Estructuras de datos de resolución de nombres](name-resolution-data-structures-2.md)
</dt> <dt>

[Modelo de resolución de nombres](name-resolution-model-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 





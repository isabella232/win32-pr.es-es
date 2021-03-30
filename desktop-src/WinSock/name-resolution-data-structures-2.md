---
description: Estructuras de datos de resolución de nombres en Windows Sockets (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Estructuras de datos de resolución de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1f76607ade81503a1057dc21890ac38d5ec265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553600"
---
# <a name="name-resolution-data-structures"></a>Estructuras de datos de resolución de nombres

Hay varias estructuras de datos importantes que se usan en gran medida a lo largo de las funciones de resolución de nombres.

## <a name="query-related-data-structures"></a>Query-Related estructuras de datos

La estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) se usa para formar consultas de [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)y se usa para proporcionar los resultados de la consulta para [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta). Es una estructura compleja, ya que contiene punteros a otras estructuras, algunas de las cuales hacen referencia a otras estructuras. La relación entre la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) y las estructuras a las que hace referencia se ilustra de la siguiente manera.

![relación entre wsaqueryset y sus estructuras asociadas](images/ovrvw3-2.png)

Dentro de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la mayoría de los miembros se explican por sí solos, pero algunos merecen una explicación adicional. El miembro **dwSize** siempre se debe rellenar con sizeof (**WSAQUERYSET**), ya que lo usan los proveedores de espacios de nombres para detectar y adaptarse a las diferentes versiones de la estructura **WSAQUERYSET** que pueden aparecer con el tiempo.

Un proveedor de espacios de nombres usa el miembro **dwOutputFlags** para proporcionar información adicional sobre los resultados de la consulta. Para obtener más información, consulte la función [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

La estructura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a la que hace referencia el miembro **lpversion** se utiliza para la restricción de consulta y los resultados. En el caso de las consultas, el miembro **dwVersion** indica la versión deseada del servicio. El miembro **ecHow** es un tipo enumerado que especifica cómo se puede realizar la comparación. Las opciones son \_ igual a, lo que requiere que se produzca una coincidencia exacta en la versión, o COMP \_ NOTLESS, que especifica que el número de versión del servicio no es menor que el valor del miembro **dwVersion** .

La interpretación de **dwNameSpace** y **lpNSProviderId** depende de cómo se use la estructura y se describe con más detalle en las descripciones de funciones individuales que utilizan esta estructura.

El miembro **lpszContext** se aplica a los espacios de nombres jerárquicos y especifica el punto inicial de una consulta o la ubicación dentro de la jerarquía en la que reside el servicio. Las reglas generales son las siguientes:

-   Un valor **null**, en blanco ("") inicia la búsqueda en el contexto predeterminado.
-   Un valor de " \\ " inicia la búsqueda en la parte superior del espacio de nombres.
-   Cualquier otro valor inicia la búsqueda en el punto designado.

Los proveedores que no admiten la contención pueden devolver un error si se especifica un valor distinto de "" o " \\ ". Los proveedores que admiten la contención limitada, como los grupos, deben aceptar "", " \\ " o un punto designado. Los contextos son específicos del espacio de nombres. Si el miembro **dwNameSpace** es NS \_ All, solo se debe pasar "" o " \\ " como contexto, ya que todos los espacios de nombres lo reconocen.

El miembro **lpszQueryString** se usa para proporcionar información adicional sobre la consulta específica del espacio de nombres, como una cadena que describe un servicio conocido y un nombre de protocolo de transporte, como en "FTP/TCP".

La estructura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a la que hace referencia el miembro **lpafpProtocols** se usa solo con fines de consulta y proporciona una lista de protocolos para restringir la consulta. Estos protocolos se representan como pares de familia de direcciones, protocolo, ya que los valores de protocolo solo tienen significado dentro del contexto de una familia de direcciones.

La matriz de la estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a la que hace referencia el miembro **lpcsaBuffer** contiene toda la información necesaria para que un servicio pueda usarse en el establecimiento de una escucha, o para que un cliente lo use en el establecimiento de una conexión al servicio. Los miembros **LocalAddr** y **RemoteAddr** contienen directamente una estructura [**de \_ dirección de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) .

Un servicio crearía un socket mediante una llamada a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la tupla de *LocalAddr. lpSockaddr->SA \_ Family*, *iSocketType* y *iProtocol* como parámetros. Un servicio enlazaría el socket a una dirección local llamando a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) mediante *localaddr. lpSockaddr* y *localaddr. lpSockaddrLength* como parámetros.

Un cliente crea su socket mediante una llamada a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la tupla de *LocalAddr. lpSockaddr->SA \_ Family*, *iSocketType* y *iProtocol* como parámetros. Un cliente usa la combinación de *RemoteAddr. lpSockaddr* y *RemoteAddr. lpSockaddrLength* como parámetros al establecer una conexión remota con la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)o [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) .

## <a name="service-class-data-structures"></a>Estructuras de datos de clase de servicio

Cuando se instala una nueva clase de servicio, se debe preparar y proporcionar una estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Esta estructura también consta de subestructuras que contienen una serie de miembros que se aplican a espacios de nombres específicos. Una estructura de datos de información de clase es la siguiente:

![arquitectura de estructuras de datos de clase de servicio](images/ovrvw3-3.png)

Para cada clase de servicio, hay una única estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Dentro de la estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) , el identificador único de la clase de servicio está contenido en el miembro **lpServiceClassId** y el miembro **lpServiceClassName** hace referencia a una cadena de presentación asociada. Esta es la cadena devuelta por la función [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) .

El miembro **lpClassInfos** de la estructura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) hace referencia a una matriz de estructuras **WSANSCLASSINFO** , cada una de las cuales proporciona un miembro con nombre y con tipo que se aplica a un espacio de nombres especificado. Algunos ejemplos de valores para el miembro **lpszName** son: "SapId", "TcpPort", "puertoudp", etc. Estas cadenas suelen ser específicas del espacio de nombres identificado en el miembro **dwNameSpace** . Los valores típicos para el miembro **dwValueType** podrían ser reg \_ DWORD, REG \_ SZ, etc. El miembro **dwValueSize** indica la longitud del elemento de datos al que apunta **lpValue**.

La colección completa de datos representada en una estructura **WSASERVICECLASSINFO** se proporciona a cada proveedor de espacios de nombres cuando se invoca la función [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) . Cada proveedor de espacios de nombres individual filtra la lista de estructuras **WSANSCLASSINFO** y conserva la información aplicable a ella.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**información de CSADDR \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Modelo de resolución de nombres](name-resolution-model-2.md)
</dt> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> <dt>

[**Dirección de SOCKET \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Resumen de las funciones de resolución de nombres](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 

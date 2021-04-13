---
description: La estructura WSAQUERYSET se usa para crear consultas para la función NSPLookupServiceBegin y se usa para proporcionar los resultados de la consulta para la función NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related estructuras de datos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ce5a7016bd2ad96f464137177036b470c64a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568531"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related estructuras de datos en el SPI

La estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) se usa para formar consultas de [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)y se usa para proporcionar los resultados de la consulta para [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext). Es una estructura compleja porque contiene punteros a varias estructuras, algunas de las cuales hacen referencia a otras estructuras. La relación entre **WSAQUERYSET** y las estructuras a las que hace referencia se ilustra de la manera siguiente:

![estructuras wsaqueryset](images/ovrvw3-2.png)

Dentro de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , la mayoría de los miembros se explican por sí solos, pero algunos merecen una explicación adicional. El **dwSize** se rellenará con sizeof ( **WSAQUERYSET**) y los proveedores de espacios de nombres pueden utilizarlo para detectar y adaptarse a las diferentes versiones de la estructura **WSAQUERYSET** que pueden aparecer.

Un proveedor de espacios de nombres usa el miembro **dwOutputFlags** para proporcionar datos adicionales sobre los resultados de la consulta. Para obtener más información, vea [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

La estructura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a la que hace referencia **lpversion** se utiliza para la restricción de consulta y los resultados. En el caso de las consultas, el miembro **dwVersion** indica la versión deseada del servicio. El miembro **ecHow** es un tipo enumerado que especifica cómo se realizará la comparación. Las opciones son \_ igual a, lo que requiere que se produzca una coincidencia exacta en la versión, o COMP \_ NOTLESS, que especifica que el número de versión del servicio no es menor que el valor de **dwVersion**.

La interpretación de **dwNameSpace** y **lpNSProviderId** depende de cómo se use la estructura y se describe con más detalle en las descripciones de funciones individuales que utilizan esta estructura.

El miembro **lpszContext** se aplica a los espacios de nombres jerárquicos y especifica el punto inicial de una consulta o la ubicación dentro de la jerarquía en la que reside el servicio. Las reglas generales son las siguientes:

-   Un valor **null** en blanco ("") iniciará la búsqueda en el contexto predeterminado.
-   Un valor de " \\ " inicia la búsqueda en la parte superior del espacio de nombres.
-   Cualquier otro valor inicia la búsqueda en el punto designado.

Los proveedores que no admiten la contención pueden devolver un error si se especifica un valor distinto de "" o " \\ ". Los proveedores que admiten la contención limitada, como los grupos, deben aceptar "", " \\ " o un punto designado. Los contextos son específicos del espacio de nombres. Si **dwNameSpace** es NS \_ All, solo se debe pasar "" o " \\ " como contexto, ya que todos los espacios de nombres lo reconocen.

El miembro **lpszQueryString** se usa para proporcionar información adicional sobre la consulta específica del espacio de nombres, como una cadena que describe un servicio conocido y un nombre de protocolo de transporte, como en "FTP/TCP".

La estructura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a la que hace referencia **lpafpProtocols** se usa solo con fines de consulta y proporciona una lista de protocolos para restringir la consulta. Estos protocolos se representan como pares de familia de direcciones, protocolos, porque los valores de protocolo solo tienen significado dentro del contexto de una familia de direcciones.

La matriz de la estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a la que hace referencia **lpcsaBuffer** contiene toda la información necesaria para que un servicio pueda usarse en el establecimiento de una escucha, o un cliente para usarlo en el establecimiento de una conexión con el servicio. Los miembros **LocalAddr** y **RemoteAddr** contienen directamente una estructura [**de \_ dirección de socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) . Un servicio crearía un socket mediante la tupla (LocalAddr. lpSockaddr->\_ familia SA, iSocketType, iProtocol). Enlazaría el socket a una dirección local mediante LocalAddr. lpSockaddr y LocalAddr. lpSockaddrLength. El cliente crea su socket con la tupla (RemoteAddr. lpSockaddr->\_ familia SA, iSocketType, iProtocol) y usa la combinación de RemoteAddr. lpSockaddr y RemoteAddr. lpSockaddrLength al establecer una conexión remota.

 

 

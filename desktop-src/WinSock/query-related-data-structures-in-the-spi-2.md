---
description: La estructura WSAQUERYSET se usa para formar consultas para la función NSPLookupServiceBegin y para entregar los resultados de la consulta para la función NSPLookupServiceNext.
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: Query-Related estructuras de datos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcbd83ab427a6ec3f09c67f416fe5eb8d7ebaad165bf4e687dfd31dce882cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569375"
---
# <a name="query-related-data-structures-in-the-spi"></a>Query-Related estructuras de datos en el SPI

La [**estructura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) se usa para formar consultas para [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)y se usa para entregar los resultados de la consulta [**para NSPLookupServiceNext.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) Se trata de una estructura compleja porque contiene punteros a otras estructuras, algunas de las cuales hacen referencia a otras estructuras. La relación entre **WSAQUERYSET y** las estructuras a las que hace referencia se ilustra de la siguiente manera:

![estructuras wsaqueryset](images/ovrvw3-2.png)

Dentro de [**la estructura WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) la mayoría de los miembros se explican por sí solos, pero algunos merecen una explicación adicional. **DwSize** se rellenará con sizeof( **WSAQUERYSET**) y los proveedores de espacios de nombres pueden utilizar para detectar y adaptarse a las distintas versiones de la estructura **WSAQUERYSET** que pueden aparecer.

Un proveedor de espacios de nombres usa el miembro **dwOutputFlags** para proporcionar datos adicionales sobre los resultados de la consulta. Para obtener más información, [**vea NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext).

La [**estructura WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) a la que hace referencia **lpversion** se usa tanto para la restricción de consulta como para los resultados. Para las consultas, el **miembro dwVersion** indica la versión deseada del servicio. El **miembro ecHow** es un tipo enumerado que especifica cómo se realizará la comparación. Las opciones son COMP EQUALS, que requiere que se produzca una coincidencia exacta en la versión, o COMP NOTLESS, que especifica que el número de versión del servicio no sea menor que el valor \_ \_ de **dwVersion**.

La interpretación de **dwNameSpace** y **lpNSProviderId** depende de cómo se use la estructura y se describe más detalladamente en las descripciones de funciones individuales que usan esta estructura.

El **miembro lpszContext** se aplica a los espacios de nombres jerárquicos y especifica el punto inicial de una consulta o la ubicación dentro de la jerarquía donde reside el servicio. Las reglas generales son las siguientes:

-   Un valor **null**, blank ("") iniciará la búsqueda en el contexto predeterminado.
-   Un valor de " \\ " inicia la búsqueda en la parte superior del espacio de nombres.
-   Cualquier otro valor inicia la búsqueda en el punto designado.

Los proveedores que no admiten la contención pueden devolver un error si se especifica algo distinto de "" \\ o "". Los proveedores que admiten la contención limitada, como los grupos, deben aceptar "", " \\ " o un punto designado. Los contextos son específicos del espacio de nombres. Si **dwNameSpace** es NS ALL, solo se debe pasar "" o "" como contexto porque todos los espacios de nombres los \_ \\ reconocen.

El **miembro lpszQueryString** se usa para proporcionar información de consulta adicional específica del espacio de nombres, como una cadena que describe un nombre de protocolo de transporte y servicio conocido, como en "ftp/tcp".

La [**estructura AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) a la que hace referencia **lpafpProtocols** solo se usa con fines de consulta y proporciona una lista de protocolos para restringir la consulta. Estos protocolos se representan como pares (familia de direcciones, protocolo), porque los valores de protocolo solo tienen significado en el contexto de una familia de direcciones.

La matriz de la estructura INFO de [**CSADDR \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) a la que hace referencia **lpcsaBuffer** contiene toda la información necesaria para que un servicio use para establecer una escucha o un cliente para establecer una conexión con el servicio. Los **miembros LocalAddr** y **RemoteAddr** contienen directamente una [**estructura SOCKET \_ ADDRESS.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) Un servicio crearía un socket mediante la tupla (LocalAddr.lpSockaddr->sa \_ family, iSocketType, iProtocol). Enlazaría el socket a una dirección local mediante LocalAddr.lpSockaddr y LocalAddr.lpSockaddrLength. El cliente crea su socket con la tupla (RemoteAddr.lpSockaddr->sa \_ family, iSocketType, iProtocol) y usa la combinación de RemoteAddr.lpSockaddr y RemoteAddr.lpSockaddrLength al realizar una conexión remota.

 

 

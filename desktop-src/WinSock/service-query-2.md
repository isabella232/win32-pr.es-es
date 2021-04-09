---
description: Consulta de servicio de nombres en Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Consulta de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082452"
---
# <a name="service-query"></a>Consulta de servicio

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Una consulta de servicio de nombres implica una serie de llamadas: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), seguida de una o varias llamadas a [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) y finalizando con una llamada a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir los parámetros de consulta junto con un conjunto de marcas para proporcionar un mayor control sobre la operación de búsqueda. Devuelve un identificador de consulta que se utiliza en las llamadas subsiguientes a **NSPLookupServiceNext** y **NSPLookupServiceEnd**.

El cliente del SPI del espacio de nombres invoca [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) para obtener los resultados de la consulta, con los resultados proporcionados en un búfer de [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) proporcionado por el cliente. El cliente sigue llamando a **NSPLookupServiceNext** hasta que se devuelve el código de error WSA \_ E, lo que indica que se han \_ \_ recuperado todos los resultados. La búsqueda se termina con una llamada a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). La función **NSPLookupServiceEnd** también se puede usar para cancelar un **NSPLookupServiceNext** pendiente actualmente cuando se llama desde otro subproceso.

En Windows Sockets 2, se definen códigos de error conflictivos para WSAENOMORE (10102) y WSA \_ e \_ no \_ más (10110). El código de error WSAENOMORE se quitará en una versión futura y solo \_ \_ \_ se conservará WSA E. Los proveedores de espacios de nombres deben cambiar al uso de la WSA \_ E \_ no hay \_ más código de error tan pronto como sea posible para mantener la compatibilidad con la gama más amplia posible de aplicaciones.

 

 




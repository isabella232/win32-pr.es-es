---
description: Consulta de servicio de nombres en Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Consulta de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168561"
---
# <a name="service-query"></a>Consulta de servicio

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Una consulta de servicio de nombres implica una serie de llamadas: [**NSPLookupServiceBegin,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)seguida de una o varias llamadas a [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) y terminando con una llamada a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) toma una estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) como entrada para definir los parámetros de consulta junto con un conjunto de marcas para proporcionar control adicional sobre la operación de búsqueda. Devuelve un identificador de consulta que se usa en las llamadas posteriores a **NSPLookupServiceNext** y **NSPLookupServiceEnd**.

El cliente SPI del espacio de nombres invoca [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) para obtener los resultados de la consulta, con los resultados proporcionados en un búfer [**WSAQUERYSET proporcionado**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) por el cliente. El cliente sigue llamada a **NSPLookupServiceNext** hasta que se devuelve el código de error WSA E NO MORE que indica que se han recuperado todos \_ \_ los \_ resultados. A continuación, la búsqueda finaliza mediante una llamada a [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). La **función NSPLookupServiceEnd** también se puede usar para cancelar un **NSPLookupServiceNext** pendiente cuando se llama desde otro subproceso.

En Windows Sockets 2, se definen códigos de error en conflicto para WSAENOMORE (10102) y WSA \_ E \_ NO MORE \_ (10110). El código de error WSAENOMORE se quitará en una versión futura y solo permanecerá WSA \_ E \_ NO \_ MORE. Los proveedores de espacios de nombres deben cambiar al código de error WSA E NO MORE lo antes posible para mantener la compatibilidad con la gama más \_ \_ amplia posible de \_ aplicaciones.

 

 




---
title: Bluetooth y BLOB
description: Bluetooth utiliza la estructura BLOB para pasar o recibir datos específicos del transporte a la estructura WSAQUERYSET durante las llamadas a las funciones WSASetService o WSALookupService\.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth y BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974626"
---
# <a name="bluetooth-and-blob"></a>Bluetooth y BLOB

Bluetooth utiliza la estructura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) para pasar o recibir datos específicos del transporte a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante las llamadas a las funciones [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService.** \*

Para su uso con Bluetooth y la función [**WSASetService,**](bluetooth-and-wsasetservice.md) los miembros de la estructura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) deben tener la siguiente configuración:

-   El **miembro cbsize** debe establecerse en el tamaño de la estructura [**BTH SET \_ \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) usada en el **miembro pBlobData,** en bytes.
-   El **miembro pBlobData** debe ser un puntero a una [**estructura BTH SET \_ \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

Para su uso con Bluetooth [y WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)la consulta de dispositivos, use la siguiente configuración:

-   El **miembro cbsize** debe establecerse en el tamaño de la estructura [**\_ BTH QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) usada en el **miembro pBlobData,** en bytes.
-   El **miembro pBlobData** debe ser un puntero a una estructura [**\_ BTH QUERY \_ DEVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)

Para su uso con Bluetooth [y WSALookupServiceBegin para la](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)detección de servicios, use la siguiente configuración:

-   El **miembro cbsize** debe establecerse en el tamaño de la estructura [**\_ BTH QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) usada en el **miembro pBlobData,** en bytes.
-   El **miembro pBlobData** debe ser un puntero a una estructura [**\_ BTH QUERY \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)

Para obtener más información, vea la sección Comentarios de la página de referencia de la estructura [**del servicio BTH \_ SET. \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 
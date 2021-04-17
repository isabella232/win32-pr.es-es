---
title: Bluetooth y BLOB
description: Bluetooth usa la estructura de BLOBs para pasar o recibir datos específicos del transporte a la estructura WSAQUERYSET durante las llamadas a las funciones WSASetService o WSALookupService \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth y BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656385"
---
# <a name="bluetooth-and-blob"></a>Bluetooth y BLOB

Bluetooth usa la estructura de [**blobs**](/windows/desktop/api/nspapi/ns-nspapi-blob) para pasar o recibir datos específicos del transporte a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante las llamadas a las funciones [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* .

Para su uso con Bluetooth y la función [**WSASetService**](bluetooth-and-wsasetservice.md) , los miembros de la estructura de [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) deben tener la siguiente configuración:

-   El miembro **cbsize** debe establecerse en el tamaño de la estructura de [**\_ \_ servicio del conjunto BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) que se usa en el miembro **pBlobData** , en bytes.
-   El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ servicio establecida en BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

Para su uso con Bluetooth y [WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use la siguiente configuración:

-   El miembro **cbsize** debe establecerse en el tamaño de la estructura del [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilizada en el miembro **pBlobData** , en bytes.
-   El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

Para su uso con Bluetooth y [WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use la siguiente configuración:

-   El miembro **cbsize** debe establecerse en el tamaño de la estructura del [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilizada en el miembro **pBlobData** , en bytes.
-   El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Para obtener más información, vea la sección Comentarios en la página de referencia de la estructura de [**\_ \_ servicio de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_servicio de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ establecer \_ servicio**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 
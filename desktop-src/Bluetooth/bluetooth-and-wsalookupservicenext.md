---
title: Bluetooth y WSALookupServiceNext
description: Bluetooth usa la función WSALookupServiceNext para buscar coincidencias con las consultas especificadas en una llamada anterior a WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth y WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010397"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth y WSALookupServiceNext

Bluetooth usa la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para buscar coincidencias con las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). Los resultados de la función **WSALookupServiceNext** se determinan mediante la configuración establecida en la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pasada en la llamada de función **WSALookupServiceBegin** inicial.

Los pasos para la consulta de dispositivos y la detección de Bluetooth son lo suficientemente diferentes como para merecer un tratamiento independiente. Para obtener más información sobre Bluetooth y la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivos, vea [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Para obtener más información sobre Bluetooth y la función **WSALookupServiceBegin** para la detección de servicios, vea [Bluetooth y WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)para la detección de servicios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 
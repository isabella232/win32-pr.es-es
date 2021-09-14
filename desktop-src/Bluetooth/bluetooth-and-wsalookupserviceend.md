---
title: Bluetooth y WSALookupServiceEnd
description: Bluetooth usa la función WSALookupServiceEnd para finalizar una consulta iniciada en una llamada anterior a WSALookupServiceBegin y quizás extendida en llamadas posteriores a WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160368"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth y WSALookupServiceEnd

Bluetooth usa la función [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para finalizar una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)y quizás extendida en llamadas posteriores a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta). La llamada a **WSALookupServiceEnd** finaliza la consulta y limpia el contexto.

Los pasos para la consulta de dispositivos y la detección de Bluetooth son lo suficientemente diferentes como para merecer un tratamiento independiente. Para obtener más información sobre Bluetooth y la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivos, vea [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Para obtener más información sobre Bluetooth y la función **WSALookupServiceBegin** para la detección de servicios, vea [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
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
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
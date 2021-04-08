---
title: Bluetooth y WSALookupServiceEnd
description: Bluetooth usa la función WSALookupServiceEnd para finalizar una consulta iniciada en una llamada anterior a WSALookupServiceBegin y, quizás, extendida en llamadas posteriores a WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995341"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth y WSALookupServiceEnd

Bluetooth usa la función [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para finalizar una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)y, quizás, extendida en llamadas posteriores a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta). La llamada a **WSALookupServiceEnd** finaliza la consulta y limpia el contexto.

Los pasos para la consulta de dispositivos y la detección de servicios en Bluetooth son lo suficientemente diferentes como para merecer un trato independiente. Para obtener más información sobre Bluetooth y la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para las consultas de dispositivos, consulte [Bluetooth y WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)consultar los dispositivos. Para obtener más información sobre Bluetooth y la función **WSALookupServiceBegin** para la detección de servicios, consulte [Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Detección de dispositivos y servicios Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**\_servicio de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**conéctelo**](/windows/desktop/api/winsock2/nf-winsock2-connect)
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

 

 
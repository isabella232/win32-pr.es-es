---
title: Detección de dispositivos y servicios Bluetooth
description: Para facilitar la detección de Bluetooth dispositivos y servicios, Windows asigna el protocolo de detección de servicios (SDP) de Bluetooth a las interfaces del espacio de nombres Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tareas, detectar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474029"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Detección de dispositivos y servicios Bluetooth

Para facilitar la detección de Bluetooth dispositivos y servicios, Windows asigna el protocolo de detección de servicios (SDP) de Bluetooth a las interfaces del espacio de nombres Windows Sockets. Las funciones principales que se usan para esta asignación son las funciones [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin,**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)y [**WSALookupServiceEnd.**](bluetooth-and-wsalookupserviceend.md) La [**estructura WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) también se usa junto con estas funciones.

Dado que ciertos conceptos y parámetros de Bluetooth SDP no se asignan necesariamente directamente a la estructura [**WSAQUERYSET,**](bluetooth-and-wsaqueryset-for-set-service.md) se debe prestar atención a cómo se crean y usan sus miembros. Para muchas operaciones Bluetooth complejas, como la creación de registros SDP, se usa el miembro **lpBlob** del **WSAQUERYSET.** Cuando es necesaria esta consideración especial, se describe específicamente, como en páginas de referencia como [**Bluetooth y WSALookupServiceNext,**](bluetooth-and-wsalookupservicenext.md)entre otras.

Es importante comprender que el registro de SDP es independiente del control de socket. Cuando una aplicación de servidor está preparada para aceptar la conexión de cliente, debe llamar a la función [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar un registro de SDP de Bluetooth correspondiente a ese servicio. Esa Bluetooth aplicación debe llamar de nuevo a la función **WSASetService** antes de cerrarse para anular el registro Bluetooth registro de SDP.

Al usar las funciones de asignación descritas en esta página, se asigna el espacio de nombres \_ NS BTH.

Para más información sobre cómo detectar dispositivos y servicios, consulte las siguientes páginas de referencia:

-   [**Bluetooth y WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth y WSALookupServiceBegin para la consulta de dispositivos**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth y WSALookupServiceBegin para la detección de servicios**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth y WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth y WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth y BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth y WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

También puede descargar el ejemplo de [conexión Bluetooth para](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) obtener un ejemplo completo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth Programación con Windows sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Bluetooth de conexión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





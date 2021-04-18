---
title: Detección de dispositivos y servicios Bluetooth
description: Para facilitar la detección de dispositivos y servicios Bluetooth, Windows asigna el protocolo de detección de servicios Bluetooth (SDP) a las interfaces del espacio de nombres de Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tareas, detectar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "105656313"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Detección de dispositivos y servicios Bluetooth

Para facilitar la detección de dispositivos y servicios Bluetooth, Windows asigna el protocolo de detección de servicios Bluetooth (SDP) a las interfaces del espacio de nombres de Windows Sockets. Las funciones principales que se usan para esta asignación son las funciones [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)y [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . La estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) también se utiliza junto con estas funciones.

Dado que determinados conceptos y parámetros del SDP de Bluetooth no se asignan necesariamente directamente a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , se debe prestar atención a cómo se crean y se usan sus miembros. Para muchas operaciones de Bluetooth complejas, como la creación de registros SDP, se usa el miembro **lpBlob** de **WSAQUERYSET** . Cuando es necesaria una consideración especial, se describe específicamente, como en páginas de referencia como [**Bluetooth y WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre otros.

Es importante comprender que el registro de SDP es independiente del control de socket. Cuando una aplicación de servidor está preparada para aceptar la conexión de cliente, debe llamar a la función [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar un registro SDP de Bluetooth que se corresponda con ese servicio. La aplicación Bluetooth debe volver a llamar a la función **WSASetService** antes de cerrar, para anular el registro del registro SDP de Bluetooth.

Al usar las funciones de asignación descritas en esta página, \_ se asigna el espacio de nombres NS BTH.

Para obtener más información acerca de la detección de dispositivos y servicios, consulte las siguientes páginas de referencia:

-   [**Bluetooth y WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth y WSALookupServiceBegin para la consulta de dispositivo**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth y WSALookupServiceBegin para la detección de servicios**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth y WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth y WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth y BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth y WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

También puede descargar el [ejemplo de conexión Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obtener un ejemplo completo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación de Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Ejemplo de conexión Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





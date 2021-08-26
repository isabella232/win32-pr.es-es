---
title: Detección de dispositivos y servicios Bluetooth
description: Para facilitar la detección de Bluetooth dispositivos y servicios, Windows asigna el Protocolo de detección de servicios (SDP) de Bluetooth a las interfaces del espacio de nombres Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tareas, detectar dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004045"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Detección de dispositivos y servicios Bluetooth

Para facilitar la detección de Bluetooth dispositivos y servicios, Windows asigna el Protocolo de detección de servicios (SDP) de Bluetooth a las interfaces del espacio de nombres Windows Sockets. Las funciones principales que se usan para esta asignación son las funciones [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin,**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)y [**WSALookupServiceEnd.**](bluetooth-and-wsalookupserviceend.md) La [**estructura WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) también se usa junto con estas funciones.

Dado que ciertos conceptos y parámetros de Bluetooth SDP no se asignan necesariamente directamente a la estructura [**WSAQUERYSET,**](bluetooth-and-wsaqueryset-for-set-service.md) se debe prestar atención a cómo se crean y usan sus miembros. Para muchas operaciones Bluetooth complejas, como la creación de registros SDP, se usa el miembro **lpBlob** de **WSAQUERYSET.** Cuando es necesaria esta consideración especial, se describe específicamente, como en páginas de referencia como [**Bluetooth y WSALookupServiceNext,**](bluetooth-and-wsalookupservicenext.md)entre otras.

Es importante comprender que el registro de SDP es independiente del control de socket. Cuando una aplicación de servidor está preparada para aceptar la conexión de cliente, debe llamar a la función [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar un registro SDP de Bluetooth correspondiente a ese servicio. Esa Bluetooth aplicación debe llamar de nuevo a la función **WSASetService** antes de cerrar, para anular el registro Bluetooth de SDP.

Al usar las funciones de asignación descritas en esta página, se asigna el espacio \_ de nombres NS BTH.

Para obtener más información sobre cómo detectar dispositivos y servicios, consulte las siguientes páginas de referencia:

-   [**Bluetooth y WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth y WSALookupServiceBegin para la consulta de dispositivos**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth y WSALookupServiceBegin para la detección de servicios**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth y WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth y WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth y BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth y WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

También puede descargar el ejemplo [de Bluetooth de conexión para](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) obtener un ejemplo completo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth Programación con Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Bluetooth ejemplo de conexión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





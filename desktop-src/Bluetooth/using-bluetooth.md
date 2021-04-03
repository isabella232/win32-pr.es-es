---
title: Uso de Bluetooth
description: En esta sección se describen las tareas relacionadas con la escritura de aplicaciones basadas en Windows para Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797049"
---
# <a name="using-bluetooth"></a>Uso de Bluetooth

En esta sección se describen las tareas relacionadas con la escritura de aplicaciones basadas en Windows para Bluetooth.

Bluetooth proporciona definiciones de programación en los archivos Ws2bth. h y BluetoothAPIs. h. El archivo Bthsdpdef. h se debe incluir antes de BluetoothAPIs. h. El archivo Ws2bth. h debe estar incluido después de WinSock2. h para usar sockets Bluetooth. Vincule solo a Bthprops. lib y evite la vinculación a Irprops. lib. Irprops. lib solo se proporciona por motivos de compatibilidad con versiones anteriores. Bthprops. lib está disponible en el SDK de Windows Vista. Puede usar el SDK de Windows Vista para desarrollar aplicaciones para Windows XP con Service Pack 2 (SP2). El SDK de Windows Vista está disponible en el [centro de descarga](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Todos los mecanismos sincrónicos y superpuestos estándar para leer y escribir datos que se admiten actualmente con otras familias de direcciones funcionan correctamente con la \_ familia de direcciones AF BTH también.

Hay algún código de ejemplo incluido en el SDK que muestra una aplicación Bluetooth sencilla que usa el protocolo de Winsock 2,2 y RFCOMM. El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.

En esta sección se describen los temas siguientes.



| Sección                                                                                      | Contenido                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Programación de Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Explica cómo usar las interfaces de Windows Sockets para implementar una red Bluetooth. |



 

 

 





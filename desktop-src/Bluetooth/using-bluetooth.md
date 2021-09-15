---
title: Uso de Bluetooth
description: En esta sección se describen las tareas relacionadas con la escritura de Windows aplicaciones basadas en Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474019"
---
# <a name="using-bluetooth"></a>Uso de Bluetooth

En esta sección se describen las tareas relacionadas con la escritura de Windows aplicaciones basadas en Bluetooth.

Bluetooth proporciona definiciones de programación en los archivos Ws2bth.h y BluetoothAPIs.h. El archivo Bthsdpdef.h debe incluirse antes de BluetoothAPIs.h. El archivo Ws2bth.h debe incluirse después de Winsock2.h para usar Bluetooth sockets. Vincule solo a Bthprops.lib y evite la vinculación a Irprops.lib. Irprops.lib solo se proporciona por compatibilidad con versiones anteriores. Bthprops.lib está disponible en el SDK Windows Vista. Puede usar el SDK Windows Vista para desarrollar aplicaciones para Windows XP con Service Pack 2 (SP2). El Windows SDK de Vista está disponible en el [Centro de descarga.](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)

Todos los mecanismos estándar sincrónicos y superpuestos para leer y escribir datos que actualmente se admiten con otras familias de direcciones también funcionan correctamente con la familia de direcciones \_ BTH de AF.

Hay algún código de ejemplo incluido con el SDK que muestra una aplicación Bluetooth con Winsock 2.2 y el protocolo RFCOMM. El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: Archivos de programa SDK de \\ \\ Microsoft Windows Samples \\ \\ <version number> \\ \\ NetDs \\ winsock \\ Bluetooth.

En esta sección se describen los temas siguientes.



| Sección                                                                                      | Contenido                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth Programación con Windows sockets](bluetooth-programming-with-windows-sockets.md) | Explica cómo usar interfaces Windows Sockets para implementar una red Bluetooth datos. |



 

 

 





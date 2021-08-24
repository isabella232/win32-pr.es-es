---
title: Uso de Bluetooth
description: En esta sección se describen las tareas relacionadas con la escritura de Windows aplicaciones basadas en Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80d57d12b2594ab5bbaeb5ad5d026552ab180ae409ba81446288ac396c746a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701835"
---
# <a name="using-bluetooth"></a>Uso de Bluetooth

En esta sección se describen las tareas relacionadas con la escritura de Windows aplicaciones basadas en Bluetooth.

Bluetooth proporciona definiciones de programación en los archivos Ws2bth.h y BluetoothAPIs.h. El archivo Bthsdpdef.h debe incluirse antes de BluetoothAPIs.h. El archivo Ws2bth.h debe incluirse después de Winsock2.h para usar Bluetooth sockets. Vincule solo a Bthprops.lib y evite vincular a Irprops.lib. Irprops.lib solo se proporciona por compatibilidad con versiones anteriores. Bthprops.lib está disponible en el SDK Windows Vista. Puede usar el SDK Windows Vista para desarrollar aplicaciones para Windows XP con Service Pack 2 (SP2). El SDK Windows Vista está disponible en el Centro [de descarga.](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)

Todos los mecanismos estándar sincrónicos y superpuestos para leer y escribir datos que se admiten actualmente con otras familias de direcciones también funcionan correctamente con la familia de direcciones \_ BTH de AF.

Hay un código de ejemplo incluido con el SDK que muestra una aplicación Bluetooth con Winsock 2.2 y el protocolo RFCOMM. El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: Archivos de programa SDK de Microsoft Windows Ejemplos de \\ \\ \\ \\ <version number> \\ \\ netDs \\ winsock \\ Bluetooth.

En esta sección se describen los temas siguientes.



| Sección                                                                                      | Content                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth Programación con Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Explica cómo usar interfaces Windows Sockets para implementar una Bluetooth red. |



 

 

 





---
title: Administración de dispositivos y servicios Bluetooth
description: Dos enfoques de programación Bluetooth principales para la programación de Windows con la interfaz de Windows Sockets y la administración de dispositivos directamente con interfaces Bluetooth que no son de socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Administración de dispositivos y servicios Bluetooth
- Dispositivos y servicios Bluetooth, administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149302"
---
# <a name="managing-bluetooth-devices-and-services"></a>Administración de dispositivos y servicios Bluetooth

En esta sección se describe cómo usar la API de Bluetooth para controlar directamente los dispositivos y servicios Bluetooth.

Para obtener información sobre el uso de la interfaz de Windows Sockets para programar Bluetooth en Windows, consulte [compatibilidad con Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).

> [!Note]  
> Bluetooth no impide que las características de administración de energía interrumpan las transmisiones Bluetooth. Las aplicaciones habilitadas para Bluetooth pueden supervisar los mensajes de energía para evitar la interrupción. Para obtener más información, consulte uso de la [Administración de energía](/windows/desktop/Power/using-power-management).

 

Esta sección contiene los temas siguientes.

| Sección                                                                               | Contenido                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Selección de un dispositivo Bluetooth](selecting-a-bluetooth-device.md)                      | Describe cómo seleccionar un dispositivo Bluetooth.                                   |
| [Mensajes de DEVICECHANGE de Bluetooth y WM \_](bluetooth-and-wm-devicechange-messages.md) | Explica la interacción entre los mensajes Bluetooth y **\_ DEVICECHANGE de WM** . |



 

 

 
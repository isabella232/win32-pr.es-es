---
description: Las siguientes funciones se usan en la administración de dispositivos.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Administración de dispositivos functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164402"
---
# <a name="device-management-functions"></a>Administración de dispositivos functions

Las siguientes funciones se usan en la administración de dispositivos.



| Función                                                             | Descripción                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Envía un código de control directamente a un controlador de dispositivo especificado.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Instala un nuevo dispositivo. Se pide al usuario que seleccione el dispositivo.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registra el dispositivo o el tipo de dispositivo para el que una ventana recibirá notificaciones. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Cierra el identificador de notificación de dispositivo especificado.                                      |



 

Las siguientes funciones se usan con unidades de CD-ROM y DVD.



| Función                                                               | Descripción                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Deshabilita la reproducción digital para la unidad de CD-ROM o DVD especificada.                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Habilita la reproducción digital para la unidad de CD-ROM o DVD especificada.                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Determina si la reproducción digital está habilitada para la unidad de CD-ROM o DVD especificada.               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Determina si la unidad de CD-ROM o DVD especificada tiene una reproducción digital que se sabe que es buena. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.                       |



 

 

 

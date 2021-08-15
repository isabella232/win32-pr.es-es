---
description: La función DeviceIoControl proporciona una interfaz de control de entrada y salida de dispositivo (IOCTL) a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Control de entrada y salida del dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5885ad3eb327e9c2df07977c7a1e16cbc962a9466b019ce8e14cbb3a3a82b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004623"
---
# <a name="device-input-and-output-control-ioctl"></a>Control de entrada y salida del dispositivo (IOCTL)

La [**función DeviceIoControl proporciona**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) una interfaz de control de entrada y salida de dispositivo (IOCTL) a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo. La **función DeviceIoControl** es una interfaz de uso general que puede enviar códigos de control a una variedad de dispositivos. Cada código de control representa una operación que debe realizar el controlador. Por ejemplo, un código de control puede pedir a un controlador de dispositivo que devuelva información sobre el dispositivo correspondiente o dirigir al controlador para que lleve a cabo una acción en el dispositivo, como dar formato a un disco.

Se definen varios códigos de control estándar en los archivos de encabezado del SDK. Además, los controladores de dispositivos pueden definir sus propios códigos de control específicos del dispositivo. Para obtener una lista de los códigos de control estándar incluidos en la documentación del SDK, consulte la sección Comentarios de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

Los tipos de códigos de control que puede especificar dependen del dispositivo al que se accede y de la plataforma en la que se ejecuta la aplicación. Las aplicaciones pueden usar los códigos de control estándar o los códigos de control específicos del dispositivo para realizar operaciones de entrada y salida directas en una unidad de disquete, unidad de disco duro, unidad de cinta o unidad de CD-ROM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamada a DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 

---
description: La función DeviceIoControl proporciona una interfaz de control de entrada y salida (IOCTL) de dispositivo a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Control de entrada y salida de dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907409"
---
# <a name="device-input-and-output-control-ioctl"></a>Control de entrada y salida de dispositivo (IOCTL)

La función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) proporciona una interfaz de control de entrada y salida (ioctl) de dispositivo a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo. La función **DeviceIoControl** es una interfaz de uso general que puede enviar códigos de control a una variedad de dispositivos. Cada código de control representa una operación que el controlador debe realizar. Por ejemplo, un código de control puede pedir a un controlador de dispositivo que devuelva información sobre el dispositivo correspondiente, o bien dirigir el controlador para llevar a cabo una acción en el dispositivo, como el formato de un disco.

En los archivos de encabezado del SDK se definen varios códigos de control estándar. Además, los controladores de dispositivo pueden definir sus propios códigos de control específicos del dispositivo. Para obtener una lista de los códigos de control estándar que se incluyen en la documentación del SDK, consulte la sección Comentarios de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

Los tipos de códigos de control que puede especificar dependen del dispositivo al que se está accediendo y de la plataforma en la que se ejecuta la aplicación. Las aplicaciones pueden usar códigos de control estándar o códigos de control específicos del dispositivo para realizar operaciones de entrada y salida directas en una unidad de disquete, en una unidad de disco duro, en una unidad de cinta o en una unidad de CD-ROM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 

---
description: Las baterías pueden proporcionar energía a equipos portátiles y equipos que ejecutan un sistema de alimentación ininterrumpida (SAI).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Información de la batería
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667225"
---
# <a name="battery-information"></a>Información de la batería

Las baterías pueden proporcionar energía a equipos portátiles y equipos que ejecutan un sistema de alimentación ininterrumpida (SAI). En estos equipos, el sistema operativo proporciona información sobre el estado de la batería para que las aplicaciones puedan proporcionar funciones útiles para el usuario. (No se admiten sistemas de batería y SAI anteriores no estándar).

Tenga en cuenta que en esta información general se supone que está familiarizado con la [Administración de dispositivos](/windows/desktop/DevIO/device-management).

Para obtener información sobre el estado de la batería, utilice la función [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) , que devuelve información general acerca de todas las fuentes de alimentación del sistema. Debe usar **GetSystemPowerStatus** siempre que sea posible.

En algunos casos, sin embargo, es necesario obtener información detallada acerca de cada batería individual. Para este propósito, cada dispositivo de batería expone una interfaz IOCTL. Las siguientes operaciones IOCTL se realizan mediante la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) :

<dl>

[**\_información de \_ consulta de batería ioctl \_**](ioctl-battery-query-information.md)  
[**Estado de la \_ consulta de batería ioctl \_ \_**](ioctl-battery-query-status.md)  
[**\_etiqueta de \_ consulta ioctl Battery \_**](ioctl-battery-query-tag.md)  
[**\_información del \_ conjunto de baterías de ioctl \_**](ioctl-battery-set-information.md)  
</dl>

Para usar esta interfaz, una aplicación debe seguir varios pasos. En primer lugar, debe usar rutinas de instalación para enumerar todos los dispositivos que tienen una interfaz de clase de batería. Tenga en cuenta que estos dispositivos representan los puertos de la batería, no las baterías reales presentes en el sistema. A continuación, la aplicación debe abrir un identificador de cada dispositivo para que pueda usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar solicitudes al dispositivo y, a continuación, adquirir etiquetas para las baterías que se inserten. Después de completar estos pasos, la aplicación puede enviar consultas a cada dispositivo de batería.

## <a name="battery-tags"></a>Etiquetas de la batería

Dado que cada dispositivo de batería representa una ranura en la que se puede insertar una batería, debe haber una manera de determinar cuándo se quita la batería y se reinserta, se reemplaza o se cambia de otra manera. Para ello, se asigna una etiqueta a cada batería de una ranura determinada. Esta etiqueta se debe usar para todas las consultas de información. Si la etiqueta proporcionada por la aplicación no coincide con la batería, se produce un error en la consulta, lo que indica a la aplicación que la batería ha cambiado de alguna manera. Para completar correctamente la consulta, se necesita una nueva etiqueta de batería. Adquiera la etiqueta mediante la operación de etiqueta de consulta de la [**\_ batería \_ \_ ioctl**](ioctl-battery-query-tag.md) . Si hay una batería en esa ranura, la etiqueta devuelta se puede pasar a cualquiera de los demás ioctl de la batería para realizar otras funciones. En un sistema de varias baterías, cada dispositivo de batería emite etiquetas de batería por separado, por lo que la etiqueta de dos dispositivos independientes podría en ocasiones ser idénticas.

Un cambio en la etiqueta de la batería no significa necesariamente que la batería se haya quitado y reinsertado o reemplazado. Se puede generar una nueva etiqueta si hay un cambio en alguno de los datos que normalmente sería estático. Por ejemplo, cuando se realiza la carga de una batería, es posible que haya cambiado la última capacidad cargada. La etiqueta también puede cambiar si la comunicación de la batería se ha perdido temporalmente o si se ha producido una notificación incorrecta del BIOS. En algunos sistemas, la etiqueta de la batería puede actualizarse cada vez que cambie el estado de AC. Este comportamiento se debe a una característica del sistema de la batería y no es común.

Cada vez que se actualiza la etiqueta de la batería, la batería debe tratarse como si fuera una nueva batería y se deben volver a leer todos los datos almacenados en caché. Si una aplicación necesita saber si existe la misma batería física, debe comprobar el valor de **BatteryUniqueID** en el búfer de salida de la información de la consulta de la batería de ioctl cuando se llama con el nivel de información **BatteryUniqueID** . [**\_ \_ \_**](ioctl-battery-query-information.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Enumerar dispositivos de batería](enumerating-battery-devices.md)
</dt> </dl>

 

 

---
description: Las baterías pueden proporcionar energía para equipos portátiles y equipos que se ejecutan en una fuente de alimentación ininterrumpida (UPS).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Información de batería
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b1afd2461985ec85a07d40bd309c588a5404e4b59be7555a01fc6c147eb221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143698"
---
# <a name="battery-information"></a>Información de batería

Las baterías pueden proporcionar energía para equipos portátiles y equipos que se ejecutan en una fuente de alimentación ininterrumpida (UPS). En estos equipos, el sistema operativo proporciona información sobre el estado de la batería para que las aplicaciones puedan proporcionar funciones útiles para el usuario. (No se admiten algunos sistemas de batería y UPS antiguos no estándar).

Tenga en cuenta que en esta introducción se da por supuesto que está familiarizado con la administración [de dispositivos.](/windows/desktop/DevIO/device-management)

Para obtener información sobre el estado de la batería, use la función [**GetSystemPowerStatus,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) que devuelve información general sobre todas las fuentes de alimentación del sistema. Debe usar **GetSystemPowerStatus siempre** que sea posible.

Sin embargo, en algunos casos se necesita información detallada sobre cada batería individual. Para ello, cada dispositivo de batería expone una interfaz IOCTL. Las siguientes operaciones de IOCTL se realizan mediante [**la función DeviceIoControl:**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

<dl>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)  
[**ESTADO DE CONSULTA \_ DE LA BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-status.md)  
[**ETIQUETA DE CONSULTA \_ DE BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-tag.md)  
[**INFORMACIÓN DEL CONJUNTO \_ DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Para usar esta interfaz, una aplicación debe seguir varios pasos. En primer lugar, debe usar rutinas de configuración para enumerar todos los dispositivos que tienen una interfaz de clase de batería. Tenga en cuenta que estos dispositivos representan los puertos de la batería, no las baterías reales presentes en el sistema. A continuación, la aplicación debe abrir un identificador para cada dispositivo, de modo que pueda usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar solicitudes al dispositivo y, a continuación, adquirir etiquetas para las baterías que se insertan. Después de completar estos pasos, la aplicación puede enviar consultas a cada dispositivo de batería.

## <a name="battery-tags"></a>Etiquetas de batería

Dado que cada dispositivo de batería representa una ranura en la que se puede insertar una batería, debe haber una manera de determinar cuándo se quita y se vuelve a insertar, reemplazar o cambiar la batería de cualquier otra manera. Para ello, a cada batería de una ranura determinada se le asigna una etiqueta. Esta etiqueta debe usarse para todas las consultas para obtener información. Si la etiqueta proporcionada por la aplicación no coincide con la batería, se produce un error en la consulta, lo que indica a la aplicación que la batería ha cambiado de alguna manera. Para completar correctamente la consulta, se requiere una nueva etiqueta de batería. Adquiera la etiqueta mediante la operación [**IOCTL \_ BATTERY QUERY \_ \_ TAG.**](ioctl-battery-query-tag.md) Si hay una batería en esa ranura, la etiqueta devuelta se puede pasar a cualquiera de las otras ICTL de batería para realizar otras funciones. En un sistema con varias baterías, cada dispositivo de batería (ranura) emite etiquetas de batería de forma independiente, por lo que la etiqueta de dos dispositivos independientes a veces podría ser idéntica.

Un cambio en la etiqueta de la batería no significa necesariamente que la batería se quitó y se reinsertó o se reemplazó. Se puede generar una nueva etiqueta si hay un cambio en cualquiera de los datos que normalmente sería estático. Por ejemplo, cuando una batería ha terminado de cargarse, la última capacidad totalmente cargada puede haber cambiado. La etiqueta también puede cambiar si la comunicación con la batería se perdió temporalmente o si se ha comunicado incorrectamente desde el BIOS. En algunos sistemas, la etiqueta de batería se puede actualizar cada vez que cambia el estado de la ca. Este comportamiento se debe a una característica del sistema de batería y no es común.

Cada vez que se actualiza la etiqueta de la batería, la batería debe tratarse como si fuera una nueva batería y todos los datos almacenados en caché deben volver a leerse. Si una aplicación necesita saber si hay la misma batería física, debe comprobar el valor de BatteryUniqueID en el búfer de salida de [**IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) cuando se llama con el nivel de información **BatteryUniqueID.** 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Enumeración de dispositivos de batería](enumerating-battery-devices.md)
</dt> </dl>

 

 

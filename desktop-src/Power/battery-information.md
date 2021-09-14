---
description: Las baterías pueden proporcionar energía para equipos portátiles y equipos que se ejecutan en una fuente de alimentación ininterrumpida (UPS).
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Información de la batería
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069176"
---
# <a name="battery-information"></a>Información de la batería

Las baterías pueden proporcionar energía para equipos portátiles y equipos que se ejecutan en una fuente de alimentación ininterrumpida (UPS). En estos equipos, el sistema operativo proporciona información sobre el estado de la batería para que las aplicaciones puedan proporcionar funciones útiles para el usuario. (No se admiten algunos sistemas de batería y UPS antiguos no estándar).

Tenga en cuenta que en esta introducción se da por supuesto que está familiarizado con la administración [de dispositivos.](/windows/desktop/DevIO/device-management)

Para obtener información sobre el estado de la batería, use la función [**GetSystemPowerStatus,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) que devuelve información general sobre todas las fuentes de alimentación del sistema. Debe usar **GetSystemPowerStatus siempre** que sea posible.

Sin embargo, en algunos casos, se necesita información detallada sobre cada batería individual. Para ello, cada dispositivo de batería expone una interfaz IOCTL. Las siguientes operaciones de IOCTL se realizan mediante la [**función DeviceIoControl:**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

<dl>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)  
[**ESTADO DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-status.md)  
[**ETIQUETA DE CONSULTA \_ DE BATERÍA \_ DE IOCTL \_**](ioctl-battery-query-tag.md)  
[**INFORMACIÓN DEL \_ CONJUNTO DE \_ BATERÍAS DE IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Para usar esta interfaz, una aplicación debe seguir varios pasos. En primer lugar, debe usar rutinas de configuración para enumerar todos los dispositivos que tienen una interfaz de clase de batería. Tenga en cuenta que estos dispositivos representan los puertos de batería, no las baterías reales presentes en el sistema. A continuación, la aplicación debe abrir un identificador en cada dispositivo para poder usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar solicitudes al dispositivo y, a continuación, adquirir etiquetas para las baterías que se insertan. Después de completar estos pasos, la aplicación puede enviar consultas a cada dispositivo de batería.

## <a name="battery-tags"></a>Etiquetas de batería

Dado que cada dispositivo de batería representa una ranura en la que se puede insertar una batería, debe haber una manera de determinar cuándo se quita y se vuelve a insertar, reemplazar o cambiar la batería de cualquier otra manera. Para ello, a cada batería de una ranura determinada se le asigna una etiqueta. Esta etiqueta debe usarse para todas las consultas para obtener información. Si la etiqueta proporcionada por la aplicación no coincide con la batería, se produce un error en la consulta, lo que indica a la aplicación que la batería ha cambiado de alguna manera. Para completar correctamente la consulta, se requiere una nueva etiqueta de batería. Adquiera la etiqueta mediante la operación [**IOCTL \_ BATTERY QUERY \_ \_ TAG.**](ioctl-battery-query-tag.md) Si hay una batería en esa ranura, la etiqueta devuelta se puede pasar a cualquiera de las otras ICTL de batería para realizar otras funciones. En un sistema de varias baterías, cada dispositivo de batería (ranura) emite etiquetas de batería de forma independiente, por lo que la etiqueta de dos dispositivos independientes a veces podría ser idéntica.

Un cambio en la etiqueta de la batería no significa necesariamente que la batería se quitó y se reinsertó o se reemplazó. Se puede generar una nueva etiqueta si hay un cambio en cualquiera de los datos que normalmente sería estático. Por ejemplo, cuando se carga una batería, puede que haya cambiado la última capacidad totalmente cargada. La etiqueta también puede cambiar si se perdió temporalmente la comunicación de la batería o si se ha comunicado incorrectamente el BIOS. En algunos sistemas, la etiqueta de batería se puede actualizar cada vez que cambia el estado de la ca. Este comportamiento se debe a una característica del sistema de baterías y no es común.

Cada vez que se actualiza la etiqueta de batería, la batería debe tratarse como si fuera una nueva batería y se deben volver a leer todos los datos almacenados en caché. Si una aplicación necesita saber si la misma batería física está presente, debe comprobar el valor de BatteryUniqueID en el búfer de salida de [**IOCTL \_ BATTERY QUERY \_ \_ INFORMATION**](ioctl-battery-query-information.md) cuando se llama con el nivel de información **BatteryUniqueID.** 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> <dt>

[Enumeración de dispositivos de batería](enumerating-battery-devices.md)
</dt> </dl>

 

 

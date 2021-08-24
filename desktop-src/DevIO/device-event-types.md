---
description: Para determinar el tipo de evento de dispositivo al procesar un mensaje \_ DEVICECHANGE de WM, examine el parámetro wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Tipos de eventos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4d807cd7524d1906e86113c546306e08051ea80770900d42c1233364430e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636645"
---
# <a name="device-event-types"></a>Tipos de eventos de dispositivo

Para determinar el tipo de evento de dispositivo al procesar un [**mensaje \_ DEVICECHANGE de WM,**](wm-devicechange.md) examine el *parámetro wParam.* El valor de *wParam* determina el significado de los datos específicos del evento en el *parámetro lParam.* En general, los datos específicos del evento identifican el dispositivo y proporcionan detalles adicionales sobre el evento. El formato de estos datos depende del tipo de dispositivo, pero los primeros bytes siempre tienen el mismo formato que la estructura [**\_ BROADCAST HDR \_ de DEV.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Para determinar el formato de los datos, compruebe el **miembro dbch \_ devicetype.**

El sistema difunde un evento de dispositivo de tipo [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (es decir, un mensaje [**DE WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT DEVICEARRIVAL) cada vez que se ha insertado un dispositivo y está disponible para su \_ uso. Las aplicaciones suelen comprobar el tipo de dispositivo y empezar a usar el dispositivo inmediatamente si es adecuado.

El sistema difunde un evento [de dispositivo \_ DBT DEVICEQUERYREMOVE](dbt-devicequeryremove.md) para solicitar permiso para quitar un dispositivo. Para determinar si necesita el dispositivo, una aplicación puede mostrar un cuadro de diálogo para pedir instrucciones al usuario. Si una aplicación determina que necesita el dispositivo, puede denegar esta solicitud y cancelar la eliminación devolviendo BROADCAST \_ QUERY \_ DENY. Si la aplicación no necesita el dispositivo, debe devolver **TRUE**. El sistema envía inmediatamente un mensaje [ \_ DBT DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) si alguna aplicación o controlador canceló una solicitud anterior para quitar un dispositivo.

El sistema difunde un evento de [dispositivo DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) como última advertencia antes de quitar un dispositivo. En este momento, la aplicación no puede cancelar la eliminación, por lo que si usa el dispositivo, debe prepararse para su eliminación para evitar la pérdida de datos. Esto es especialmente importante cuando se quita una conexión de red. La aplicación debe determinar si alguno de sus archivos o canalizaciones abiertos están en esa conexión. Para ello, compare el identificador de recursos de red de los datos específicos del evento del mensaje con los identificadores de recursos obtenidos anteriormente para los archivos y canalizaciones. El sistema difunde un evento de [dispositivo \_ DBT DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) cuando se ha quitado un dispositivo y ya no está disponible.

El sistema difunde un evento de [dispositivo \_ DBT QUERYCHANGECONFIG](dbt-querychangeconfig.md) para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar). Cualquier aplicación puede devolver BROADCAST \_ QUERY DENY para denegar la solicitud y cancelar el \_ cambio. Si una aplicación deniega la solicitud, el sistema envía un mensaje [ \_ CONFIGCHANGECANCELED de DBT.](dbt-configchangecanceled.md) Si la configuración actual ha cambiado, debido a un acoplamiento o desacoplado, el sistema envía un mensaje [ \_ CONFIGCHANGED de DBT.](dbt-configchanged.md)

El sistema difunde un evento [de dispositivo \_ DBT DEVICETYPESPECIFIC](dbt-devicetypespecific.md) cada vez que se produce un evento específico del dispositivo.

Los controladores pueden crear sus propios tipos de eventos personalizados. Los eventos personalizados solo se envían a la aplicación que se ha registrado para la notificación de eventos de dispositivo en un dispositivo determinado y solo se pueden iniciar mediante controladores en modo kernel. Para obtener más información, [vea DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 




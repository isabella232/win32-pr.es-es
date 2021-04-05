---
description: Para determinar el tipo de evento de dispositivo al procesar un mensaje de DEVICECHANGE de WM \_ , examine el parámetro wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Tipos de eventos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ece6b810ba4d1310638bbfbdcdcaa7f67f79d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080193"
---
# <a name="device-event-types"></a>Tipos de eventos de dispositivo

Para determinar el tipo de evento de dispositivo al procesar un mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) , examine el parámetro *wParam* . El valor de *wParam* determina el significado de los datos específicos del evento en el parámetro *lParam* . En general, los datos específicos del evento identifican el dispositivo y proporcionan detalles adicionales sobre el evento. El formato de estos datos depende del tipo de dispositivo, pero los primeros bytes siempre tienen el mismo formato que la estructura [**\_ \_ HDR de la difusión dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Para determinar el formato de los datos, compruebe el miembro de **dbch \_ DeviceType** .

El sistema difunde un evento de dispositivo de tipo [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (es decir, un mensaje de [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* establecido en DBT \_ DEVICEARRIVAL) siempre que se ha insertado un dispositivo y está disponible para su uso. Normalmente, las aplicaciones comprueban el tipo de dispositivo y empiezan a usar el dispositivo inmediatamente si es adecuado.

El sistema difunde un evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) para solicitar permiso para quitar un dispositivo. Para determinar si necesita el dispositivo, una aplicación puede mostrar un cuadro de diálogo para pedir instrucciones al usuario. Si una aplicación determina que necesita el dispositivo, puede denegar esta solicitud y cancelar la eliminación devolviendo la consulta de difusión \_ \_ denegar. Si la aplicación no necesita el dispositivo, debe devolver **true**. El sistema envía inmediatamente un mensaje [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) si alguna aplicación o controlador canceló una solicitud anterior para quitar un dispositivo.

El sistema difunde un evento de dispositivo [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) como última ADVERTENCIA antes de que se quite un dispositivo. En este punto, la aplicación no puede cancelar la eliminación, por lo que si usa el dispositivo, debe preparar su eliminación para evitar la pérdida de datos. Esto es especialmente importante cuando se quita una conexión de red. La aplicación debe determinar si alguno de los archivos o canalizaciones abiertos están en esa conexión. Para ello, puede comparar el identificador de recursos de red en los datos específicos del evento del mensaje con los identificadores de recursos obtenidos previamente para los archivos y las canalizaciones. El sistema difunde un evento de dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) cuando se ha quitado un dispositivo y ya no está disponible.

El sistema difunde un evento de dispositivo [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) para solicitar permiso para cambiar la configuración actual (acoplar o desacoplar). Cualquier aplicación puede devolver la \_ consulta de difusión \_ Deny para denegar la solicitud y cancelar el cambio. Si una aplicación deniega la solicitud, el sistema envía un [mensaje \_ CONFIGCHANGECANCELED de DBT](dbt-configchangecanceled.md) . Si la configuración actual ha cambiado, debido a un acoplamiento o desacoplamiento, el sistema envía un [mensaje \_ CONFIGCHANGED de DBT](dbt-configchanged.md) .

El sistema difunde un evento de dispositivo [DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md) cada vez que se produce un evento específico del dispositivo.

Los controladores pueden crear sus propios tipos de eventos personalizados. Los eventos personalizados solo se envían a la aplicación que se ha registrado para la notificación de eventos de dispositivo en un dispositivo determinado y solo los pueden iniciar controladores en modo kernel. Para obtener más información, vea [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 




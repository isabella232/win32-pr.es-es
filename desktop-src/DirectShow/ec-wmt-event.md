---
description: Enviado por el filtro de lector ASF de WM cuando lee archivos ASF protegidos por la administración de derechos digitales (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653393"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (DShow. h)

Enviado por el filtro de [lector ASF de WM](wm-asf-reader-filter.md) cuando lee archivos ASF protegidos por la administración de derechos digitales (DRM).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Uno de los siguientes valores de **\_ Estado de WMT** :



| Value                         | Descripción                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_licencia de adquisición de WMT \_         | Se envía cuando el componente DRM ha completado el proceso de adquisición de licencias, ya sea correcta o incorrectamente. |
| individual de WMT \_            | Se ha completado el proceso de actualización de seguridad, ya sea correctamente o sin éxito.                                |
| WMT \_ necesita la \_ individualización | El archivo requiere que una aplicación reciba una actualización de seguridad antes de realizar la acción solicitada.          |
| \_sin \_ derechos de WMT               | La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por la versión 1 de DRM.                |
| \_no hay \_ derechos de WMT \_ ex           | La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por la versión 7 de DRM.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ datos de evento WMT de AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contiene información sobre el evento o **null**. El miembro **pdata** de esta estructura apunta a datos adicionales, cuyo tipo depende del valor de **lParam1**, como se muestra en la tabla siguiente.



| lParam1                       | \_Datos de evento WMT de AM \_ \_ . pdata                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_licencia de adquisición de WMT \_         | Puntero a una estructura de [**datos de licencia de Get de WM \_ \_ \_**](/windows/desktop/wmformat/wm-get-license-data) . Esta estructura se documenta en el SDK de Windows Media Format. |
| individual de WMT \_            | Puntero a una estructura de estado de la [**\_ \_ individualización de WM**](/windows/desktop/wmformat/wm-individualize-status) .                                                        |
| WMT \_ necesita la \_ individualización | **Null**.                                                                                                                                        |
| \_sin \_ derechos de WMT               | Puntero a una cadena de caracteres anchos que contiene una dirección URL de desafío.                                                                                   |
| \_no hay \_ derechos de WMT \_ ex           | Puntero a una estructura de [**datos de licencia de Get de WM \_ \_ \_**](/windows/desktop/wmformat/wm-get-license-data) .                                                               |



 

El valor de *lParam2* puede ser **null**. Compruebe el valor antes de desreferenciar el puntero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Consulte la documentación del SDK de Windows Media Format para obtener más información sobre cómo habilitar la reproducción de archivos protegidos con DRM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 


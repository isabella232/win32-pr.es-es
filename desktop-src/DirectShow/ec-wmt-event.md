---
description: Enviado por el filtro lector de ASF de WM cuando lee archivos ASF protegidos por administración de derechos digitales (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2ae2659c26d170bef14a76c0528eb5159e92ef3598fb999215e1fbd848ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819928"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (Dshow.h)

Enviado por el [filtro lector de ASF de WM](wm-asf-reader-filter.md) cuando lee archivos ASF protegidos por administración de derechos digitales (DRM).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Uno de los siguientes **valores de ESTADO \_ DE WMT:**



| Valor                         | Descripción                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| ADQUISICIÓN DE LICENCIA DE WMT \_ \_         | Se envía cuando el componente DRM ha completado el proceso de adquisición de licencias, ya sea correcta o incorrectamente. |
| WMT \_ INDIVIDUALIZE            | El proceso de actualización de seguridad se ha completado correctamente o incorrectamente.                                |
| WMT \_ NECESITA \_ INDIVIDUALIZACIÓN | El archivo requiere que una aplicación reciba una actualización de seguridad antes de realizar la acción solicitada.          |
| WMT \_ NO \_ RIGHTS               | La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por DRM versión 1.                |
| WMT \_ NO \_ RIGHTS \_ EX           | La aplicación no tiene derechos para realizar la acción solicitada en un archivo protegido por DRM versión 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntero a una [**estructura \_ AM WMT EVENT \_ \_ DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que contiene información sobre el evento o **NULL.** El **miembro pData** de esta estructura apunta a datos adicionales, cuyo tipo depende del valor **de lParam1**, como se muestra en la tabla siguiente.



| lParam1                       | AM \_ WMT \_ EVENT \_ DATA.pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| ADQUISICIÓN DE LICENCIA DE WMT \_ \_         | Puntero a una [**estructura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data) Esta estructura se documenta en el SDK Windows Media Format. |
| WMT \_ INDIVIDUALIZE            | Puntero a una [**estructura WM \_ INDIVIDUALIZE \_ STATUS.**](/windows/desktop/wmformat/wm-individualize-status)                                                        |
| WMT \_ NECESITA \_ INDIVIDUALIZACIÓN | **NULL.**                                                                                                                                        |
| WMT \_ NO \_ RIGHTS               | Puntero a una cadena de caracteres anchos que contiene una dirección URL de desafío.                                                                                   |
| WMT \_ NO \_ RIGHTS \_ EX           | Puntero a una [**estructura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data)                                                               |



 

El valor de *lParam2* podría ser **NULL.** Compruebe el valor antes de desreferenciar el puntero.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Consulte la documentación Windows SDK de formato multimedia para obtener más información sobre cómo habilitar la reproducción de archivos protegidos con DRM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 


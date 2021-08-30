---
description: Se envía cuando una aplicación usa el filtro WM ASF Writer para indexar Windows archivos de vídeo multimedia.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f76518e72249eb325cb07626c66c66ad7668d772f4b4bc8fe2e0236ff4b37b44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928415"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (Dshow.h)

Se envía cuando una aplicación usa el filtro [WM ASF Writer](wm-asf-writer-filter.md) para indexar Windows archivos de vídeo multimedia.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Puede ser uno de los siguientes **mensajes DE ESTADO \_ DE WMT.**



| Valor                | Descripción              |
|----------------------|--------------------------|
| WMT \_ STARTED         | La indexación ha comenzado.      |
| WMT \_ CLOSED          | Se ha completado la indexación.  |
| PROGRESO DEL \_ ÍNDICE WMT \_ | La indexación está en curso. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *lParam1* es WMT \_ CLOSED o WMT \_ STARTED, *lParam2* es cero. Si *lParam1* es WMT \_ INDEX \_ PROGRESS, *lParam2* es **un DWORD** que especifica el progreso actual como un porcentaje del tamaño total de descarga.

</dd> </dl>

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

 

 





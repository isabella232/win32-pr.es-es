---
description: Se envía cuando una aplicación usa el filtro de escritor ASF de WM para indizar Windows Media Video archivos.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679537"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (DShow. h)

Se envía cuando una aplicación usa el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) para indizar Windows Media Video archivos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Puede ser uno de los siguientes mensajes de **\_ Estado de WMT** .



| Value                | Descripción              |
|----------------------|--------------------------|
| WMT \_ iniciado         | La indización ha comenzado.      |
| WMT \_ cerrado          | La indización ha finalizado.  |
| \_progreso del índice WMT \_ | La indexación está en curso. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *lParam1* es WMT \_ Closed o WMT \_ iniciado, entonces *lParam2* es cero. Si *lParam1* es \_ \_ el progreso del índice WMT, *lParam2* es un **valor DWORD** que especifica el progreso actual como un porcentaje del tamaño total de la descarga.

</dd> </dl>

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

 

 





---
description: El usuario ha finalizado la reproducción.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a546a963a5fe6a2afc0a0d48d086ad59598adb0072e96095a50ac35cf10ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965525"
---
# <a name="ec_userabort"></a>\_USERABORT DE EC

El usuario ha finalizado la reproducción.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno. La aplicación debe decidir si se debe detener el gráfico.

## <a name="remarks"></a>Comentarios

Este código de evento indica que el usuario ha finalizado la reproducción normal del grafo. Por ejemplo, los representadores de vídeo envían este evento si el usuario cierra la ventana de vídeo.

Después de enviar este evento, el filtro debe rechazar todas las muestras y no enviar ningún evento [**\_ EC REPAINT,**](ec-repaint.md) hasta que el filtro se detenga y se restablezca.

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

 

 





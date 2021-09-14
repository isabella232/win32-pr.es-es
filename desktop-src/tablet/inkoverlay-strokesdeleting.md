---
description: Se produce antes de que se eliminen los trazos de la propiedad Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay.StrokesDeleting (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256617"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay.StrokesDeleting

Se produce antes de que se eliminen los trazos de la [**propiedad Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)

## <a name="syntax"></a>Sintaxis


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Trazos* \[ En\]
</dt> <dd>

La [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) se elimina cuando se produce el evento **StrokesDeleting.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IOEStrokesDeleting.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Ink Property \[ InkCollector/InkOverLay (Clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 


---
description: Se produce antes de que se eliminen los trazos de la propiedad de entrada de lápiz.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002715"
---
# <a name="inkoverlaystrokesdeleting-event"></a>Evento InkOverlay. StrokesDeleting

Se produce antes de que se eliminen los trazos de la propiedad de [**entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .

## <a name="syntax"></a>Sintaxis


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Trazos* \[ de\]
</dt> <dd>

Colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) eliminada cuando se desencadena el evento **StrokesDeleting** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEStrokesDeleting.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Propiedad de entrada manuscrita \[ InkCollector/InkOverLay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 


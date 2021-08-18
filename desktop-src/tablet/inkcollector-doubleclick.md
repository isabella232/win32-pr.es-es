---
description: 'Evento InkCollector.DoubleClick: se produce cuando se hace doble clic en el objeto InkCollector o InkOverlay.'
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector.DoubleClick (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f0d523ac34f22da1ce37bf106e980343fb12f09cd8fcfe2bb4be454769bf9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718171"
---
# <a name="inkcollectordoubleclick-event"></a>InkCollector.DoubleClick, evento

Se produce cuando se hace doble clic en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)

## <a name="syntax"></a>Sintaxis


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar el evento del control primario; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEDblClick.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> </dl>

 

 





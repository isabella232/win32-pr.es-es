---
description: Se produce cuando el objeto InkOverlay o el control InkPicture han completado el propio dibujo.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay.Painted (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f433f18d5e94be1163be519f4ee33fbe0b8d08a2e33feadd363a8eb3a43a6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218947"
---
# <a name="inkoverlaypainted-event"></a>Evento InkOverlay.Painted

Se produce cuando el [**objeto InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) han completado el propio dibujo.

## <a name="syntax"></a>Sintaxis


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDC* \[ En\]
</dt> <dd>

Contexto del dispositivo en el que se produjo el evento.

</dd> <dt>

*Rect* \[ En\]
</dt> <dd>

[**InkRectangle**](inkrectangle-class.md) que se ha repintado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IOEPainted.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> </dl>

 

 





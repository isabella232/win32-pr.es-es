---
description: Se produce cuando el objeto InkOverlay o el control InkPicture han terminado de volver a dibujarse.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay.Painted (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360262"
---
# <a name="inkoverlaypainted-event"></a>Evento InkOverlay.Painted

Se produce cuando el [**objeto InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) han terminado de volver a dibujarse.

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

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de DISPID \_ IOEPainted.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> </dl>

 

 





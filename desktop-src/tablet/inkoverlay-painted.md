---
description: Se produce cuando el objeto InkOverlay o el control InkPicture han terminado de volver a dibujarse.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498076"
---
# <a name="inkoverlaypainted-event"></a>InkOverlay. pintado (evento)

Se produce cuando el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) han terminado de volver a dibujarse.

## <a name="syntax"></a>Sintaxis


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HDC* \[ de\]
</dt> <dd>

Contexto de dispositivo en el que se produjo el evento.

</dd> <dt>

*Rectángulo* \[ de\]
</dt> <dd>

[**InkRectangle**](inkrectangle-class.md) que se ha repintado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEPainted.

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
</dt> </dl>

 

 





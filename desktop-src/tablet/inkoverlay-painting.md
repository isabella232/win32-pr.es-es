---
description: Se produce antes de que el objeto InkOverlay o el InkPicture hayan terminado de volver a dibujarse.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. Painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546563"
---
# <a name="inkoverlaypainting-event"></a>Evento InkOverlay. Painting

Se produce antes de que el objeto [**InkOverlay**](inkoverlay-class.md) o el [InkPicture](inkpicture-control-reference.md) hayan terminado de volver a dibujarse.

## <a name="syntax"></a>Sintaxis


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HDC* \[ de\]
</dt> <dd>

Contexto de dispositivo en el que se producirá el dibujo.

</dd> <dt>

*Rectángulo* \[ de\]
</dt> <dd>

Rectángulo que se va a volver a dibujar.

</dd> <dt>

*Permitir* \[ in, out\]
</dt> <dd>

Indica si se debe volver a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEPainting.

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

 

 





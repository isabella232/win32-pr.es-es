---
description: Se produce antes de que el objeto InkOverlay o InkPicture haya terminado de volver a dibujarse.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay.Painting (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42075f6ae8641c895611196b80a904228cc27c45e5d84bdc798b5cc9242e7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218948"
---
# <a name="inkoverlaypainting-event"></a>Evento InkOverlay.Painting

Se produce antes de que [**el objeto InkOverlay**](inkoverlay-class.md) o [InkPicture](inkpicture-control-reference.md) haya terminado de volver a dibujarse.

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

*hDC* \[ En\]
</dt> <dd>

Contexto del dispositivo en el que se realizará la pintura.

</dd> <dt>

*Rect* \[ En\]
</dt> <dd>

Rectángulo que se va a volver a dibujar.

</dd> <dt>

*Permitir* \[ in, out\]
</dt> <dd>

Si se va a volver a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IOEPainting.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> </dl>

 

 





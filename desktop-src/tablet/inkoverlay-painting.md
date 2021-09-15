---
description: Se produce antes de que el objeto InkOverlay o InkPicture haya terminado de volver a dibujarse.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay.Painting (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360261"
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

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IOEPainting.

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

 

 





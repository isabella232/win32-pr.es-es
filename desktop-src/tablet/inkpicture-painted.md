---
description: Se produce cuando el control InkPicture ha completado el propio dibujo.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture.Painted (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201027ba2626cd3a3dd8d76a8794a1a5430785e0e1602633ee9f39ac36caa023
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451072"
---
# <a name="inkpicturepainted-event"></a>Evento InkPicture.Painted

Se produce cuando el control [InkPicture](inkpicture-control-reference.md) ha completado el propio dibujo.

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

Este método de evento se define en las interfaces **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ IOEPainted.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 





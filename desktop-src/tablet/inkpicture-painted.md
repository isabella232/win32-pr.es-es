---
description: Se produce cuando el control InkPicture ha terminado de volver a dibujarse.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716304"
---
# <a name="inkpicturepainted-event"></a>InkPicture. pintado (evento)

Se produce cuando el control [InkPicture](inkpicture-control-reference.md) ha terminado de volver a dibujarse.

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

Este método de evento se define en las interfaces dispinterface **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con un identificador de DISPID \_ IOEPainted.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 





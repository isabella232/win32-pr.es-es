---
description: El método SetTargetRect establece el rectángulo de destino.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Método CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670733"
---
# <a name="cdrawimagesettargetrect-method"></a>CDrawImage. SetTargetRect, método

El `SetTargetRect` método establece el rectángulo de destino.

## <a name="syntax"></a>Sintaxis


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntero a una estructura **Rect** que define el nuevo rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método si cambia el rectángulo de origen; por ejemplo, en respuesta a una llamada a [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .

Antes de llamar a este método, valide el rectángulo dado en *pTargetRect* con respecto a la ventana de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 





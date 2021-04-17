---
description: El método SetDrawContext establece los contextos de dispositivo que se usan para dibujar.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Método CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660424"
---
# <a name="cdrawimagesetdrawcontext-method"></a>CDrawImage. SetDrawContext, método

El `SetDrawContext` método establece los contextos de dispositivo que se usan para dibujar.

## <a name="syntax"></a>Sintaxis


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método recupera los contextos de dispositivo de memoria y de ventana del objeto [**CBaseWindow**](cbasewindow.md) propietario. Llame a este método después de que se inicialice la ventana, pero antes de comenzar el dibujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 





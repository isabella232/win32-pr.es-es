---
description: El método CancelNotification cancela el evento de temporizador que programa la representación.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Método CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671079"
---
# <a name="cbaserenderercancelnotification-method"></a>CBaseRenderer. CancelNotification, método

El `CancelNotification` método cancela el evento de temporizador que programa la representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | No había ningún evento de temporizador pendiente.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                          |



 

## <a name="remarks"></a>Observaciones

El filtro llama a este método cuando se detiene el streaming. El método cancela cualquier representación programada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





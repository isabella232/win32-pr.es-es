---
description: El método CancelNotification cancela el evento de temporizador que programa la representación.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Método CBaseRenderer.CancelNotification (Renbase.h)
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
ms.openlocfilehash: be7366e6e22aa7e984fe4b50ea29edfa840d78380373d521c6cd8bfd226e1a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635175"
---
# <a name="cbaserenderercancelnotification-method"></a>Método CBaseRenderer.CancelNotification

El `CancelNotification` método cancela el evento de temporizador que programa la representación.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No había ningún evento de temporizador pendiente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                          |



 

## <a name="remarks"></a>Comentarios

El filtro llama a este método cuando se detiene el streaming. El método cancela cualquier representación programada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





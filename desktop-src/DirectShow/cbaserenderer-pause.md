---
description: El método PAUSE pausa el filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Método CBaseRenderer. PAUSE (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671734"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer. PAUSE (método)

El `Pause` método pausa el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | La transición se ha completado.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | La transición no está completa.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter::P ause**](cbasefilter-pause.md) . Realiza los pasos siguientes:

-   Llama al método **CBaseFilter::P ause** .
-   Confirma el asignador. (Vea [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)).
-   Si se detuvo el estado anterior, el filtro libera cualquier muestra que contiene. (El ejemplo ya no es válido).
-   Llama al método [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) y devuelve el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





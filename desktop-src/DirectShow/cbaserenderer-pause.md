---
description: El método Pause pausa el filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Método CBaseRenderer.Pause (Renbase.h)
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
ms.openlocfilehash: 9769a1243fdbd69037e275fc083a9b1b0766f7f404190b2e68920f238e2bf140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586085"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer.Pause (método)

El `Pause` método pausa el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                             | Descripción                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | La transición se ha completado.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La transición no se ha completado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseFilter::P ause.**](cbasefilter-pause.md) Realiza los pasos siguientes:

-   Llama al **método CBaseFilter::P ause.**
-   Confirma el asignador. (Vea [**IMemAllocator::Commit).**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)
-   Si se detuvo el estado anterior, el filtro libera cualquier muestra que esté manteniendo. (El ejemplo ya no es válido).
-   Llama al [**método CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) y devuelve el valor .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





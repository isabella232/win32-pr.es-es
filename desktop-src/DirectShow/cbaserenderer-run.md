---
description: El método Run ejecuta el filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Método CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671729"
---
# <a name="cbaserendererrun-method"></a>CBaseRenderer. Run (método)

El `Run` método ejecuta el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter:: Run**](cbasefilter-run.md) . Las acciones que realiza son las siguientes:

-   Llama al método **CBaseFilter:: Run** .
-   Confirma el asignador. (Vea [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)).
-   Si se detuvo el estado anterior, el filtro libera cualquier muestra que contiene. (El ejemplo ya no es válido).
-   Llama al método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) y devuelve el resultado. Si hay un ejemplo pendiente, el método **StartStreaming** lo programa para su representación.

Si el filtro no está conectado, publica un evento [**de \_ finalización de EC**](ec-complete.md) inmediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





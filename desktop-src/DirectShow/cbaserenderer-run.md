---
description: El método Run ejecuta el filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Método CBaseRenderer.Run (Renbase.h)
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
ms.openlocfilehash: 4c07c89354d1885fcc70799b3aaf4cc651668bda80ddadd30dbe74c77a2b6275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999695"
---
# <a name="cbaserendererrun-method"></a>Método CBaseRenderer.Run

El `Run` método ejecuta el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseFilter::Run.**](cbasefilter-run.md) Las acciones que realiza son las siguientes:

-   Llama al **método CBaseFilter::Run.**
-   Confirma el asignador. (Vea [**IMemAllocator::Commit).**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)
-   Si se detuvo el estado anterior, el filtro libera cualquier muestra que esté manteniendo. (El ejemplo ya no es válido).
-   Llama al [**método CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) y devuelve el resultado. Si hay un ejemplo pendiente, el **método StartStreaming** lo programa para su representación.

Si el filtro no está conectado, publica un [**evento EC \_ COMPLETE**](ec-complete.md) inmediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





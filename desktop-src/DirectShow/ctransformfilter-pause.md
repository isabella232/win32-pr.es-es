---
description: 'Método CTransformFilter.Pause: el método Pause pausa el filtro. Este método implementa el método IMediaFilter::P ause.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Método CTransformFilter.Pause (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51584bc38c49345f6bb1d940aed24a052e9a4f9cd05fc2dc84246a6ba1168fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953504"
---
# <a name="ctransformfilterpause-method"></a>CTransformFilter.Pause (método)

El `Pause` método pausa el filtro. Este método implementa el [**método IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método llama al [**método StartStreaming.**](ctransformfilter-startstreaming.md) El **método StartStreaming** no hace nada en la clase base, pero la clase derivada puede invalidarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 





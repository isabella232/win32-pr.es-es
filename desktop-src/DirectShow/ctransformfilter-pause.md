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
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095103"
---
# <a name="ctransformfilterpause-method"></a>Método CTransformFilter.Pause

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

Este método llama al [**método StartStreaming.**](ctransformfilter-startstreaming.md) El **método StartStreaming** no hace nada en la clase base, pero la clase derivada puede invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 





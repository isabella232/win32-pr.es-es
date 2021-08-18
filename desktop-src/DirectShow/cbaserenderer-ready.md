---
description: El método Ready indica que se ha completado una transición de estado.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Método CBaseRenderer.Ready (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757525"
---
# <a name="cbaserendererready-method"></a>CBaseRenderer.Ready (método)

El `Ready` método indica que se ha completado una transición de estado.

## <a name="syntax"></a>Sintaxis


```C++
void Ready();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método hace que [**el método CBaseRenderer::GetState**](cbaserenderer-getstate.md) devuelva S OK, lo que indica que el filtro ha completado la transición \_ a su estado actual. El filtro llama a este método cada vez que completa una transición de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer::NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 





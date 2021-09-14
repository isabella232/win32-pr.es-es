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
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070113"
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

## <a name="remarks"></a>Observaciones

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

 

 





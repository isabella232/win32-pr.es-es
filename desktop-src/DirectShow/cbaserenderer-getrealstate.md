---
description: El método GetRealState recupera el estado del filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Método CBaseRenderer.GetRealState (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c65ac4310abddc619296776981040cc5e1e6c5ad48ce37ea24210bc5a85d94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403424"
---
# <a name="cbaserenderergetrealstate-method"></a>Método CBaseRenderer.GetRealState

El `GetRealState` método recupera el estado del filtro.

## <a name="syntax"></a>Sintaxis


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CBaseFilter::m \_ State**](cbasefilter-m-state.md). El valor es un miembro del [**tipo enumerado FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

## <a name="remarks"></a>Comentarios

Este método proporciona una alternativa más sencilla al método [**CBaseRenderer::GetState,**](cbaserenderer-getstate.md) para uso interno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





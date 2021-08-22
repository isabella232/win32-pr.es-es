---
description: El método NotReady indica que aún no se ha completado una transición de estado.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Método CBaseRenderer.NotReady (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954834"
---
# <a name="cbaserenderernotready-method"></a>CBaseRenderer.NotReady (método)

El método indica que aún no se ha completado una `NotReady` transición de estado.

## <a name="syntax"></a>Sintaxis


```C++
void NotReady();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método hace que el método [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) devuelva VFW S STATE INTERMEDIATE, lo que indica que el filtro sigue en transición \_ a su estado \_ \_ actual. El filtro llama a este método cada vez que hay una transición de estado pendiente. (Esto ocurre cuando el filtro se detiene, hasta que recibe una muestra).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 





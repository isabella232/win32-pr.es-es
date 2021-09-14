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
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261479"
---
# <a name="cbaserenderernotready-method"></a>Método CBaseRenderer.NotReady

El método indica que aún no se ha completado `NotReady` una transición de estado.

## <a name="syntax"></a>Sintaxis


```C++
void NotReady();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método hace que el método [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) devuelva VFW S STATE INTERMEDIATE, lo que indica que el filtro sigue en transición \_ a su estado \_ \_ actual. El filtro llama a este método cada vez que hay pendiente una transición de estado. (Esto ocurre cuando el filtro se detiene, hasta que recibe un ejemplo).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 





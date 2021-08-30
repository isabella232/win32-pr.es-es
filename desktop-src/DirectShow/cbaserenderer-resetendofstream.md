---
description: El método ResetEndOfStream restablece las marcas de fin de secuencia.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Método CBaseRenderer.ResetEndOfStream (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f65bb1c4a63f1aac004dcbe0e1da267c1f14cf095d9c60e2f68391b50d53a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131435"
---
# <a name="cbaserendererresetendofstream-method"></a>Método CBaseRenderer.ResetEndOfStream

El `ResetEndOfStream` método restablece las marcas de fin de flujo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método borra la condición de final de secuencia anterior. En ese momento, el filtro puede recibir nuevos datos. Los [**métodos CBaseRenderer::Stop**](cbaserenderer-stop.md) y [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) llaman a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





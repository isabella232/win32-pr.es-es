---
description: El método OnWaitStart actualiza los tiempos dedicados a esperar y no a esperar.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Método CBaseVideoRenderer.OnWaitStart (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bc3b895f27490377fd5de188b7cea8ccd429c55d36a5cdd0fea4ce025bac29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502605"
---
# <a name="cbasevideorendereronwaitstart-method"></a>Método CBaseVideoRenderer.OnWaitStart

El `OnWaitStart` método actualiza los tiempos dedicados a esperar y no a esperar.

## <a name="syntax"></a>Sintaxis


```C++
void OnWaitStart();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se llama a esta función miembro cuando se empieza a esperar un evento de representación. Solo se usa para las medidas de rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 





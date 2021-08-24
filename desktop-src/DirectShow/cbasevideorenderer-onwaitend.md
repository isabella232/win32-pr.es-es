---
description: Se llama al método OnWaitEnd cuando finaliza un tiempo de espera.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Método CBaseVideoRenderer.OnWaitEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b130bf38833951cad4f82fd559c0299d2aea86854ca0ab5545f3f2794ab9b4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432475"
---
# <a name="cbasevideorendereronwaitend-method"></a>Método CBaseVideoRenderer.OnWaitEnd

Se llama al método OnWaitEnd cuando finaliza un tiempo de espera.

## <a name="syntax"></a>Sintaxis


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro solo realiza el registro de rendimiento. Se llama cuando el subproceso no espera en la ventana o cuando se debe representar el ejemplo siguiente. Finalmente, se podría usar para recopilar información que controla la sincronización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 





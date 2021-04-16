---
description: Se llama al método OnWaitStart cuando el filtro empieza a esperar el tiempo de presentación de un ejemplo.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Método CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671735"
---
# <a name="cbaserendereronwaitstart-method"></a>CBaseRenderer. OnWaitStart, método

`OnWaitStart`Se llama al método cuando el filtro empieza a esperar el tiempo de presentación de un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) llama a este método cuando comienza a esperar el tiempo de presentación de un ejemplo. Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

Si está implementando el control de calidad, puede invalidar este método junto con el método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) . Puede utilizar estos métodos para realizar el seguimiento del rendimiento del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





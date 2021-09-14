---
description: Se llama al método OnWaitStart cuando el filtro comienza a esperar el tiempo de presentación de una muestra.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Método CBaseRenderer.OnWaitStart (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261412"
---
# <a name="cbaserendereronwaitstart-method"></a>Método CBaseRenderer.OnWaitStart

Se `OnWaitStart` llama al método cuando el filtro comienza a esperar el tiempo de presentación de una muestra.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El [**método CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) llama a este método cuando comienza a esperar el tiempo de presentación de un ejemplo. Este método no hace nada en la clase base, pero la clase derivada puede invalidarla.

Si va a implementar el control de calidad, puede invalidar este método junto con el [**método CBaseRenderer::OnWaitEnd.**](cbaserenderer-onwaitend.md) Puede usar estos métodos para realizar un seguimiento del rendimiento del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





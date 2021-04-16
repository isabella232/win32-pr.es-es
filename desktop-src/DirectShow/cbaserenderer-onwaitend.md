---
description: Se llama al método OnWaitEnd cuando el filtro se realiza en espera de un tiempo de presentación de un ejemplo.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Método CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671736"
---
# <a name="cbaserendereronwaitend-method"></a>CBaseRenderer. OnWaitEnd, método

`OnWaitEnd`Se llama al método cuando el filtro se realiza en espera de un tiempo de presentación de un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) llama a este método cuando ha terminado de esperar el tiempo de presentación de un ejemplo. Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

Si está implementando el control de calidad, puede invalidar este método junto con el método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) . Puede utilizar estos métodos para realizar el seguimiento del rendimiento del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





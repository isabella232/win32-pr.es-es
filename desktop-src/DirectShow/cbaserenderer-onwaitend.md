---
description: Se llama al método OnWaitEnd cuando se realiza el filtro a la espera del tiempo de presentación de una muestra.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Método CBaseRenderer.OnWaitEnd (Renbase.h)
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
ms.openlocfilehash: 451f475f8830e1b6e2c51f3e0fc571f86f520030fe8ec3dad6acf3d9d5e5c6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537445"
---
# <a name="cbaserendereronwaitend-method"></a>Método CBaseRenderer.OnWaitEnd

Se `OnWaitEnd` llama al método cuando se realiza el filtro esperando el tiempo de presentación de una muestra.

## <a name="syntax"></a>Sintaxis


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El [**método CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) llama a este método cuando ha terminado de esperar el tiempo de presentación de un ejemplo. Este método no hace nada en la clase base, pero la clase derivada puede invalidarla.

Si va a implementar el control de calidad, puede invalidar este método junto con el [**método CBaseRenderer::OnWaitStart.**](cbaserenderer-onwaitstart.md) Puede usar estos métodos para realizar un seguimiento del rendimiento del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





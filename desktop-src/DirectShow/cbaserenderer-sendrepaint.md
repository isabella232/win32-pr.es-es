---
description: El método SendRepaint envía un evento de repintado al administrador de gráficos de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer.SendRepaint (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9057d1ff733c30da3b3b0d7e960607eadd033dcee0b26994478c6da9156a183e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954794"
---
# <a name="cbaserenderersendrepaint-method"></a>Método CBaseRenderer.SendRepaint

El `SendRepaint` método envía un evento de repintado al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método envía un [**evento \_ EC REPAINT**](ec-repaint.md) al administrador de gráficos de filtros si se cumplen las condiciones siguientes:

-   El pin de entrada está conectado.
-   El filtro no vacía los datos.
-   No se alcanzó el final de la secuencia.
-   La [**marca CBaseRenderer::m \_ bAbort**](cbaserenderer-m-babort.md) es **FALSE.**
-   La [**marca CBaseRenderer::m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) es **TRUE.**

En función del estado del gráfico, el evento EC REPAINT puede hacer que el filtro ascendente vuelva a enviar una muestra, el gráfico de filtros busque su ubicación actual o que el administrador del gráfico de filtros se pause \_ momentáneamente. (Vea [**EC \_ REPAINT**](ec-repaint.md)). Este evento es potencialmente ineficaz, por lo que debe usarse con moderación. Sin embargo, los representadores de vídeo a veces necesitan actualizar la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





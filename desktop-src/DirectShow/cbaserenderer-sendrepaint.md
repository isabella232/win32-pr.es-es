---
description: El método SendRepaint envía un evento Repaint al administrador de gráficos de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer. SendRepaint (Renbase. h)
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
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671100"
---
# <a name="cbaserenderersendrepaint-method"></a>CBaseRenderer. SendRepaint, método

El `SendRepaint` método envía un evento Repaint al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método envía un [**evento \_ Repaint de EC**](ec-repaint.md) al administrador de gráficos de filtro si se cumplen las condiciones siguientes:

-   El PIN de entrada está conectado.
-   El filtro no está vaciando datos.
-   No se ha alcanzado el final de la secuencia.
-   La marca [**CBaseRenderer:: m \_ BAbort**](cbaserenderer-m-babort.md) es **false**.
-   La marca [**CBaseRenderer:: m \_ BRepaintStatus**](cbaserenderer-m-brepaintstatus.md) es **true**.

Dependiendo del estado del gráfico, el \_ evento de Repaint de EC puede hacer que el filtro de nivel superior vuelva a enviar una muestra, el gráfico de filtro para buscar en su ubicación actual o el administrador de gráficos de filtro para que se PAUSE momentáneamente. (Consulte [**EC \_ Repaint**](ec-repaint.md)). Este evento es potencialmente ineficaz, por lo que debe usarse con moderación. Sin embargo, en ocasiones, los representadores de vídeo necesitan actualizar la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





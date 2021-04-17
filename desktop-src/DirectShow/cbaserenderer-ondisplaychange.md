---
description: El método OnDisplayChange envía un \_ evento de visualización de \_ modificación de EC al administrador de gráficos de filtro.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Método CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661334"
---
# <a name="cbaserendererondisplaychange-method"></a>CBaseRenderer. OnDisplayChange, método

El `OnDisplayChange` método envía un evento de [**\_ visualización de \_ modificación de EC**](ec-display-changed.md) al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se ha expuesto el evento o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Los representadores de vídeo deben llamar a este método en respuesta a \_ los mensajes de WM DISPLAYCHANGE. Si el PIN de entrada está conectado, el método envía un \_ evento de visualización de \_ modificación de EC al administrador de gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





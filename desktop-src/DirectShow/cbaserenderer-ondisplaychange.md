---
description: El método OnDisplayChange publica un evento \_ EC DISPLAY CHANGED en el administrador de \_ gráficos de filtros.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Método CBaseRenderer.OnDisplayChange (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261468"
---
# <a name="cbaserendererondisplaychange-method"></a>Método CBaseRenderer.OnDisplayChange

El `OnDisplayChange` método publica un evento EC DISPLAY [**\_ \_ CHANGED**](ec-display-changed.md) en el administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se ha publicado el evento o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Los representadores de vídeo deben llamar a este método en respuesta a los mensajes \_ DISPLAYCHANGE de WM. Si el pin de entrada está conectado, el método envía un evento EC \_ DISPLAY CHANGED al administrador de \_ gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





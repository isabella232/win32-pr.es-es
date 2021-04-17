---
description: Pausa el objeto. Implementa el método IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Método CBaseMediaFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670499"
---
# <a name="cbasemediafilterpause-method"></a>CBaseMediaFilter. PAUSE (método)

Pausa el objeto. Implementa el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

En la clase base, este método establece la variable miembro de [**\_ Estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) en el estado \_ pausado, pero no hace nada más.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 





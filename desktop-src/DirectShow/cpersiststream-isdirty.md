---
description: Indica si el objeto ha cambiado desde que se guardó por última vez en su flujo actual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream. IsDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670999"
---
# <a name="cpersiststreamisdirty-method"></a>CPersistStream. IsDirty (método)

Indica si el objeto ha cambiado desde que se guardó por última vez en su flujo actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si es necesario guardar el filtro y s \_ false si no es necesario guardarlo.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método **IPersistStream:: IsDirty** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 





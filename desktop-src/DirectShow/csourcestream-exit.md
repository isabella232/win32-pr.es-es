---
description: El método Exit indica al subproceso de streaming que salga.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Método CSourceStream. Exit (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660743"
---
# <a name="csourcestreamexit-method"></a>CSourceStream. Exit (método)

El `Exit` método indica al subproceso de streaming que salga.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto o E \_ inesperados.

## <a name="remarks"></a>Observaciones

El método [**CSourceStream:: Inactive**](csourcestream-inactive.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





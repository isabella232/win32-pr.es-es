---
description: Se llama al método StartStreaming cuando el filtro cambia al estado en pausa. Este método invalida el método CTransformFilter::StartStreaming.
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Método CVideoTransformFilter.StartStreaming (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53d448228a650718f8c57d6019dcfb1f3f23f03468e86a77fae167e6481e718c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998475"
---
# <a name="cvideotransformfilterstartstreaming-method"></a>Método CVideoTransformFilter.StartStreaming

Se `StartStreaming` llama al método cuando el filtro cambia al estado en pausa. Este método invalida el [**método CTransformFilter::StartStreaming.**](ctransformfilter-startstreaming.md)

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método restablece todas las estadísticas de rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 





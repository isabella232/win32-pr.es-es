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
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266431"
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

## <a name="remarks"></a>Observaciones

Este método restablece todas las estadísticas de rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 





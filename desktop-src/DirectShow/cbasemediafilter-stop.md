---
description: El método Stop detiene el objeto . Este método implementa el método IMediaFilter::Stop.
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Método CBaseMediaFilter.Stop (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273228"
---
# <a name="cbasemediafilterstop-method"></a>Método CBaseMediaFilter.Stop

El `Stop` método detiene el objeto . Este método implementa el [**método IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

En la clase base, este método establece la variable miembro [**CBaseMediaFilter::m \_ State**](cbasemediafilter-m-state.md) en State Stopped, pero \_ no hace nada más.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





---
description: 'Método CSourceSeeking.SetRate: el método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking::SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Método CSourceSeeking.SetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f51b0425837cc48176490ea5d5d35cd2eae1851e7e56fa35b3578e37898afdd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053885"
---
# <a name="csourceseekingsetrate-method"></a>Método CSourceSeeking.SetRate

El `SetRate` método establece la velocidad de reproducción. Este método implementa el [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dRate* 
</dt> <dd>

Velocidad de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método actualiza el valor de la variable miembro [**CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) y, a continuación, llama al método virtual [**puro CSourceSeeking::ChangeRate**](csourceseeking-changerate.md). El método no valida el *parámetro dRate.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





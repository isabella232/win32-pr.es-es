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
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098743"
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
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





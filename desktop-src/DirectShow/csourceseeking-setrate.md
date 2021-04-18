---
description: 'El método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking:: SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Método CSourceSeeking. SetRate (Ctlutil. h)
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690466"
---
# <a name="csourceseekingsetrate-method"></a>CSourceSeeking. SetRate, método

El `SetRate` método establece la velocidad de reproducción. Este método implementa el método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .

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

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método actualiza el valor de la variable miembro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) y, a continuación, llama al método virtual puro [**CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md). El método no valida el parámetro *dRate* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





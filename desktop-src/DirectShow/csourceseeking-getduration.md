---
description: 'El método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Método CSourceSeeking. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660785"
---
# <a name="csourceseekinggetduration-method"></a>CSourceSeeking. GetDuration, método

El `GetDuration` método recupera la duración de la secuencia. Este método implementa el método [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDuration* 
</dt> <dd>

Puntero a una variable que recibe la duración, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl> | Valor de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

La duración se especifica mediante la variable miembro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 





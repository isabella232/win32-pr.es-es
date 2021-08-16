---
description: 'Método CSourceSeeking.GetRate: el método GetRate recupera la velocidad de reproducción. Este método implementa el método IMediaSeeking::GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Método CSourceSeeking.GetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b734a5fafba9e38abbe853a8f3592a212130bf9a68de0efe7125aeea0ea01b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083955"
---
# <a name="csourceseekinggetrate-method"></a>Método CSourceSeeking.GetRate

El `GetRate` método recupera la velocidad de reproducción. Este método implementa el [**método IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdRate* 
</dt> <dd>

Puntero a una variable que recibe la velocidad de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

La velocidad de reproducción se especifica mediante la variable miembro [**CSourceSeeking::m \_ dRateSeeking.**](csourceseeking-m-drateseeking.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





---
description: 'Método CSourceSeeking.GetAvailable: el método GetAvailable recupera el intervalo de veces en que la búsqueda es eficaz. Este método implementa el método IMediaSeeking::GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking.GetAvailable (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae42efad42bf9f1e0df0f4f791f1e4e8abb76fe8252818a8e35eda4dd6e6b87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953754"
---
# <a name="csourceseekinggetavailable-method"></a>Método CSourceSeeking.GetAvailable

El `GetAvailable` método recupera el intervalo de veces en que la búsqueda es eficaz. Este método implementa el [**método IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEarliest* 
</dt> <dd>

Puntero a una variable que recibe la primera hora para una búsqueda eficaz. La variable se establece en cero.

</dd> <dt>

*pLatest* 
</dt> <dd>

Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz. La variable se establece en el valor de la variable miembro [**CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





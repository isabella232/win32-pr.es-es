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
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085243"
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
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





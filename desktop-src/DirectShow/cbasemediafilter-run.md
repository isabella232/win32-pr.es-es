---
description: El método Run ejecuta el objeto . Este método implementa el método IMediaFilter::Run.
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Método CBaseMediaFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273231"
---
# <a name="cbasemediafilterrun-method"></a>Método CBaseMediaFilter.Run

El `Run` método ejecuta el objeto . Este método implementa el [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Tiempo de referencia correspondiente al tiempo de secuencia 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Si el objeto se detiene, este método pausa el objeto llamando al método [**CBaseMediaFilter::P ause.**](cbasemediafilter-pause.md) A continuación, establece la variable [**miembro de estado \_ CBaseMediaFilter::m**](cbasemediafilter-m-state.md) en State \_ Running.

El tiempo de la secuencia se calcula como el tiempo de referencia actual menos *tStart.* Un ejemplo multimedia con una marca de tiempo de cero debe representarse en el *momento tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseMediaFilter (clase)**](cbasemediafilter.md)
</dt> </dl>

 

 





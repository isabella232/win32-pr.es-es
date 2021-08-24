---
description: El método Run ejecuta el filtro. Este método implementa el método IMediaFilter::Run.
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793285"
---
# <a name="cbasefilterrun-method"></a>CBaseFilter.Run (método)

El `Run` método ejecuta el filtro. Este método implementa el [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

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

Hora de referencia correspondiente al tiempo de secuencia 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Si se detiene el filtro, este método pausa el filtro llamando al método [**CBaseFilter::P ause.**](cbasefilter-pause.md) A continuación, llama [**al método CBasePin::Run**](cbasepin-run.md) en cada uno de los pines conectados del filtro. Por último, establece la variable [**miembro de estado CBaseFilter::m \_**](cbasefilter-m-state.md) en State \_ Running.

El tiempo de secuencia se calcula como el tiempo de referencia actual menos *tStart.* Un ejemplo multimedia con una marca de tiempo de cero debe representarse en el *momento tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 





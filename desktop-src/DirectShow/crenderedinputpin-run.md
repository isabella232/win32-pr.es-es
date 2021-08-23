---
description: El método Run notifica al pin que el filtro se está ejecutando. Este método invalida el método CBasePin::Run.
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Método CRenderedInputPin.Run (Arendertra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c372101aee2817e08545080048c98a25af7efb152f4873e54366e73571763065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652025"
---
# <a name="crenderedinputpinrun-method"></a>Método CRenderedInputPin.Run

El `Run` método notifica al pin que el filtro se está ejecutando. Este método invalida el [**método CBasePin::Run.**](cbasepin-run.md)

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

Hora de inicio que se pasó al método [**IMediaFilter::Run del**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Anicetra.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRenderedInputPin (clase)**](crenderedinputpin.md)
</dt> </dl>

 

 





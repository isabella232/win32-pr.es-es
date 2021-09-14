---
description: El método Run notifica al pin que el filtro se está ejecutando. Este método invalida el método CBasePin::Run.
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Método CRenderedInputPin.Run (Amextra.h)
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
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160193"
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
| Encabezado<br/>  | <dl> <dt>Amextra.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRenderedInputPin (clase)**](crenderedinputpin.md)
</dt> </dl>

 

 





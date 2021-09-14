---
description: El método GetStopPosition recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaSeeking::GetStopPosition.
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Método CSourceSeeking.GetStopPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361365"
---
# <a name="csourceseekinggetstopposition-method"></a>Método CSourceSeeking.GetStopPosition

El `GetStopPosition` método recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el [**método IMediaSeeking::GetStopPosition.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que recibe la hora de detenerse, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="remarks"></a>Observaciones

La hora de detenerse se especifica mediante la variable miembro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





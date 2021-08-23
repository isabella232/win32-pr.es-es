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
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073329"
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
| <dl> <dt>**S \_ OK**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

La hora de detenerse se especifica mediante la variable miembro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





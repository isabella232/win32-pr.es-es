---
description: El método GetStopPosition recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaSeeking::GetStopPosition.
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Método CPosPassThru.GetStopPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9c6798d03e2935c991e12cded4d85a4972d54e7800d6aa79c70525b10276f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084075"
---
# <a name="cpospassthrugetstopposition-method"></a>Método CPosPassThru.GetStopPosition

El método recupera la hora a la que se detendrá `GetStopPosition` la reproducción, en relación con la duración de la secuencia. Este método implementa el [**método IMediaSeeking::GetStopPosition.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition)

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

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





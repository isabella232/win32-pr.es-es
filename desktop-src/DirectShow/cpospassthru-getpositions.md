---
description: El método GetPositions recupera la posición actual y la posición de detenerse, con respecto a la duración total de la secuencia. Este método implementa el método IMediaSeeking::GetPositions.
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Método CPosPassThru.GetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 948deeb61c5a514bc4bd385c387f10961c21cbaf6090b5e281e1f245e1d23225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108275"
---
# <a name="cpospassthrugetpositions-method"></a>Método CPosPassThru.GetPositions

El `GetPositions` método recupera la posición actual y la posición de detenerse, con respecto a la duración total de la secuencia. Este método implementa el [**método IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que recibe la posición de detenerse, en unidades del formato de hora actual.

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

 

 





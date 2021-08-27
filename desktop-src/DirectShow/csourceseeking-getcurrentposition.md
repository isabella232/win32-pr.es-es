---
description: El método GetCurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Sin implementar.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Método CSourceSeeking.GetCurrentPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4069c8b1a83ade6897fedf87c16b89b1c63d3c1cef18d21a3bdbd594a3b2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084062"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Método CSourceSeeking.GetCurrentPosition

El `GetCurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia. Sin implementar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

Normalmente, los filtros de origen no admiten este método. En su lugar, los filtros de representador informan de la posición actual a través [**de la clase CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





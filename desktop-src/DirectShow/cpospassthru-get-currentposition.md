---
description: 'El \_ método get CurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaPosition:: get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Método CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660491"
---
# <a name="cpospassthruget_currentposition-method"></a>CPosPassThru. Get \_ CurrentPosition (método)

El `get_CurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método [**IMediaPosition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntero a una variable que recibe la posición actual, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





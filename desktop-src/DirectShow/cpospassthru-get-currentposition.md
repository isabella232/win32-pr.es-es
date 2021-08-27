---
description: El método \_ get CurrentPosition recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el método IMediaPosition::get \_ CurrentPosition.
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: CPosPassThru.get_CurrentPosition método (Ctlutil.h)
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
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084245"
---
# <a name="cpospassthruget_currentposition-method"></a>Método CPosPassThru.get \_ CurrentPosition

El `get_CurrentPosition` método recupera la posición actual, en relación con la duración total de la secuencia. Este método implementa el [**método IMediaPosition::get \_ CurrentPosition.**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition)

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

 

 





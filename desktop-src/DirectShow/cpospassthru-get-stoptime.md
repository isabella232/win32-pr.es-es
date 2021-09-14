---
description: El método get StopTime recupera la hora a la que se detendrá la \_ reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaPosition::get \_ StopTime.
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: CPosPassThru.get_StopTime método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062409"
---
# <a name="cpospassthruget_stoptime-method"></a>Método CPosPassThru.get \_ StopTime

El método recupera la hora a la que se detendrá `get_StopTime` la reproducción, en relación con la duración de la secuencia. Este método implementa el [**método IMediaPosition::get \_ StopTime.**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntero a una variable que recibe la hora de detenerse, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





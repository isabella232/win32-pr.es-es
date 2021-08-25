---
description: El método get \_ Duration recupera la duración de la secuencia. Este método implementa el método IMediaPosition::get \_ Duration.
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: CPosPassThru.get_Duration método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e39dadd5a652b7b88321f21f1d5312c1ac44a1f1f23e7be75f9aab3460938aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915485"
---
# <a name="cpospassthruget_duration-method"></a>Método CPosPassThru.get \_ Duration

El `get_Duration` método recupera la duración de la secuencia. Este método implementa el [**método IMediaPosition::get \_ Duration.**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plength* 
</dt> <dd>

Puntero a una variable que recibe la longitud total del flujo, en segundos.

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

 

 





---
description: El método CheckTime determina si se debe a una hora especificada.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681198"
---
# <a name="ccmdqueuechecktime-method"></a>CCmdQueue. CheckTime, método

El `CheckTime` método determina si se debe a una hora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*time* 
</dt> <dd>

Tiempo de comprobación.

</dd> <dt>

*bStream* 
</dt> <dd>

**True** si el parámetro *Time* es un valor de tiempo de secuencia; **False** si la *hora* es un valor de tiempo de presentación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si aún no se ha pasado la hora especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 





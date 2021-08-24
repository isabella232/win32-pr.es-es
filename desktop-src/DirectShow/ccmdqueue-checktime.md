---
description: El método CheckTime determina si se debe una hora especificada.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue.CheckTime (Winutil.h)
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
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910435"
---
# <a name="ccmdqueuechecktime-method"></a>Método CCmdQueue.CheckTime

El `CheckTime` método determina si se debe un tiempo especificado.

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

Hora de comprobación.

</dd> <dt>

*bStream* 
</dt> <dd>

**TRUE** si el *parámetro time* es un valor de tiempo de secuencia; **FALSE** si *time* es un valor de tiempo de presentación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si aún no se ha pasado la hora especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 





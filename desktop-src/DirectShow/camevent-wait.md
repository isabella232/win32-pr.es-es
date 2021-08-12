---
description: El método Wait se bloquea hasta que se señala el evento o hasta que se produce un tiempo de espera.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent.Wait (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3875647cb93619e8326066bc9af7a6f99f79a0b0a2df58f668b1e365fd39102b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662516"
---
# <a name="cameventwait-method"></a>Método CAMEvent.Wait

El `Wait` método se bloquea hasta que se señala el evento o hasta que se produce un tiempo de espera.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valor de tiempo de espera opcional, representado en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se señala el evento. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Observaciones

En el caso de los eventos de restablecimiento automático, el evento se restablece a un estado no firmado cuando este método vuelve.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 





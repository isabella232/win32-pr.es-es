---
description: El método Run cambia al modo de ejecución para que se puedan ejecutar los comandos que se aplazan por el tiempo de transmisión.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Método CCmdQueue.Run (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5da70c4ac0c5890e4483f7facdc4d1f5a3d5dd70906c53917bd83029dfaa6c6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757145"
---
# <a name="ccmdqueuerun-method"></a>CCmdQueue.Run (método)

El método cambia al modo de ejecución para que se puedan ejecutar los comandos que se `Run` aplazan por el tiempo de transmisión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Tiempo de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Durante el modo de ejecución, se conoce la asignación en tiempo de transmisión a tiempo de presentación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 





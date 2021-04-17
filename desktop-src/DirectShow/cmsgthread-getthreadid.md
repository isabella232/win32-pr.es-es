---
description: Recupera el identificador del subproceso.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Método CMsgThread. GetThreadID (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670987"
---
# <a name="cmsgthreadgetthreadid-method"></a>CMsgThread. GetThreadID, método

Recupera el identificador del subproceso.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el miembro de datos privado del **\_ ThreadId de m** .

## <a name="remarks"></a>Observaciones

Esta función devuelve el identificador de Microsoft Win32 para el subproceso de trabajo. Puede llamar a esta función miembro en el subproceso de trabajo o en un subproceso de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 





---
description: Se llama al método OnThreadCreate cuando se inicializa el subproceso de streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: CSourceStream. OnThreadCreate (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660902"
---
# <a name="csourcestreamonthreadcreate-method"></a>CSourceStream. OnThreadCreate, método

`OnThreadCreate`Se llama al método cuando se inicializa el subproceso de streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El procedimiento de subproceso, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), llama a este método cuando recibe por primera vez una solicitud [**CSourceStream:: init**](csourcestream-init.md) . El método no hace nada en la clase base. La clase derivada puede invalidar este método para realizar inicializaciones de subprocesos. Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 





---
description: Se llama al método OnThreadCreate cuando se inicializa el subproceso de streaming.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Método CSourceStream.OnThreadCreate (Source.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361351"
---
# <a name="csourcestreamonthreadcreate-method"></a>Método CSourceStream.OnThreadCreate

Se `OnThreadCreate` llama al método cuando se inicializa el subproceso de streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

El procedimiento de subproceso [**CSourceStream::ThreadProc**](csourcestream-threadproc.md)llama a este método cuando recibe por primera vez una [**solicitud CSourceStream::Init.**](csourcestream-init.md) El método no hace nada en la clase base. La clase derivada puede invalidar este método para realizar inicializaciones de subprocesos. Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 





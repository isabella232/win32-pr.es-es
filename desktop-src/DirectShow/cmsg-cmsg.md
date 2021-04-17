---
description: Construye un objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Constructor CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680350"
---
# <a name="cmsgcmsg-constructor"></a>Constructor CMsg. CMsg

Construye un objeto [**CMsg**](cmsg.md) .

## <a name="syntax"></a>Sintaxis


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*u* 
</dt> <dd>

Código de solicitud, definido por el cliente de la clase de subproceso y comprensible por la función de subproceso de trabajo invalidada.

</dd> <dt>

*dw* 
</dt> <dd>

Parámetro de marca para el código de solicitud.

</dd> <dt>

*LP* 
</dt> <dd>

Puntero a los datos requeridos por el subproceso de trabajo como parámetros o valores devueltos. Estos datos no deberían estar basados en la pila, ya que se hará referencia a él después de completar la operación de puesta en cola.

</dd> <dt>

*As* 
</dt> <dd>

Puntero al objeto de evento que un subproceso de trabajo puede señalar para indicar la finalización de la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta función miembro contiene una solicitud para que un subproceso de trabajo de [**CMsgThread**](cmsgthread.md) actúe. Todos los parámetros se pasan a la función de subproceso de trabajo como parámetros cuando se procesa este mensaje. Los significados de los parámetros se definen mediante la función de cliente que llama al subproceso de trabajo y la clase derivada que proporciona la función de ejecución del subproceso de trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 





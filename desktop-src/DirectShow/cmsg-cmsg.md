---
description: Construye un objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Constructor CMsg.CMsg (Msgthrd.h)
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
ms.openlocfilehash: f921c96ae185d8993002c84a09b4efb8bc5977104c274de3a2ffc964a093f1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831905"
---
# <a name="cmsgcmsg-constructor"></a>Constructor CMsg.CMsg

Construye un [**objeto CMsg.**](cmsg.md)

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

Código de solicitud, definido por el cliente de la clase de subproceso y comprendido por la función de subproceso de trabajo invalidada.

</dd> <dt>

*dw* 
</dt> <dd>

Marca el parámetro en el código de solicitud.

</dd> <dt>

*Lp* 
</dt> <dd>

Puntero a los datos requeridos por el subproceso de trabajo como parámetros o valores devueltos. Estos datos no deben basarse en la pila, ya que se hará referencia a estos algún tiempo después de completar la operación de cola.

</dd> <dt>

*pEvent* 
</dt> <dd>

Puntero al objeto de evento que un subproceso de trabajo puede indicar para indicar la finalización de la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta función miembro contiene una solicitud para que actúe un subproceso de [**trabajo CMsgThread.**](cmsgthread.md) Todos los parámetros se pasan a la función del subproceso de trabajo como parámetros cuando se procesa este mensaje. Los significados de los parámetros se definen mediante la función de cliente que llama al subproceso de trabajo y la clase derivada que proporciona la función de ejecución del subproceso de trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 





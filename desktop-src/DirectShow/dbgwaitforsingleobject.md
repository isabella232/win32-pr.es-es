---
description: Espera a que se señale un objeto.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Función DbgWaitForSingleObject (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681160"
---
# <a name="dbgwaitforsingleobject-function"></a>DbgWaitForSingleObject función)

Espera a que se señale un objeto.

En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se Señalice el objeto. Para establecer el intervalo de tiempo de espera, llame a la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

En una compilación comercial, esta función es equivalente a la función **WaitForSingleObject** con un intervalo de tiempo de espera infinito.

## <a name="syntax"></a>Sintaxis


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*h* 
</dt> <dd>

Identificador del objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de espera](wait-debugging-functions.md)
</dt> </dl>

 

 





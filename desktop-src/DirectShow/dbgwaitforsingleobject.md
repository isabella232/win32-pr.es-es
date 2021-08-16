---
description: Espera a que se señale un objeto.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Función DbgWaitForSingleObject (Wxdebug.h)
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
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749355"
---
# <a name="dbgwaitforsingleobject-function"></a>Función DbgWaitForSingleObject

Espera a que se señale un objeto.

En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se señale el objeto. Para establecer el intervalo de tiempo de espera, llame a la [**función DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

En una compilación comercial, esta función es equivalente a la **función WaitForSingleObject** con un intervalo de tiempo de espera infinito.

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
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de depuración de espera](wait-debugging-functions.md)
</dt> </dl>

 

 





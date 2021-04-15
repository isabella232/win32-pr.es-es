---
description: Espera a que se señalen todos los objetos especificados (o todos).
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Función DbgWaitForMultipleObjects (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661309"
---
# <a name="dbgwaitformultipleobjects-function"></a>DbgWaitForMultipleObjects función)

Espera a que se señalen todos los objetos especificados (o todos).

En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se señalen los objetos. Para establecer el intervalo de tiempo de espera, llame a la función [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

En una compilación comercial, esta función es equivalente a la función **WaitForMultipleObjects** con un intervalo de tiempo de espera infinito.

## <a name="syntax"></a>Sintaxis


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nCount* 
</dt> <dd>

Número de objetos.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Matriz de identificadores de objetos, de tamaño *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valor booleano que especifica si se deben esperar todos los objetos. Si **es true**, la función espera a que se señalen todos los objetos. De lo contrario, espera que se señalice al menos un objeto.

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

 

 





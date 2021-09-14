---
description: Espera a que se señale a cualquiera (o a todos) de los objetos especificados.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Función DbgWaitForMultipleObjects (Wxdebug.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062372"
---
# <a name="dbgwaitformultipleobjects-function"></a>Función DbgWaitForMultipleObjects

Espera a que se señale a cualquiera (o a todos) de los objetos especificados.

En una compilación de depuración, esta función desencadena una aserción si el intervalo de tiempo de espera expira antes de que se señalen los objetos. Para establecer el intervalo de tiempo de espera, llame a la [**función DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

En una compilación comercial, esta función es equivalente a la **función WaitForMultipleObjects** con un intervalo de tiempo de espera infinito.

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

Matriz de identificadores para objetos, de tamaño *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valor booleano que especifica si se debe esperar a todos los objetos. Si **es TRUE,** la función espera a que se señalen todos los objetos. De lo contrario, espera a que se señale al menos un objeto.

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

 

 





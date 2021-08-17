---
description: La función DbgDumpObjectRegister muestra información sobre los objetos activos. Se omite en las compilaciones comerciales.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Función DbgDumpObjectRegister (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d82d7b419949210e19460880126a07ad52f63ae59f6055e5a2b968a2dd5c7beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821582"
---
# <a name="dbgdumpobjectregister-function"></a>Función DbgDumpObjectRegister

La `DbgDumpObjectRegister` función muestra información sobre los objetos activos. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

En las compilaciones de depuración, la biblioteca de depuración mantiene una lista de objetos activos. La lista incluye los objetos que derivan de [**CBaseObject**](cbaseobject.md), creados por el módulo actual y no se han destruyedo. Los métodos de constructor y destructor **CBaseObject** actualizan la lista.

Esta función genera varios mensajes LOG \_ MEMORY. En el nivel de registro 1, la función muestra solo el número total de objetos. En el nivel de registro 2 o superior, muestra una lista de los objetos .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





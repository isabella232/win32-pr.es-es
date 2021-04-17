---
description: La función DbgDumpObjectRegister muestra información sobre los objetos activos. Se omite en las compilaciones comerciales.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Función DbgDumpObjectRegister (Wxdebug. h)
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
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660502"
---
# <a name="dbgdumpobjectregister-function"></a>DbgDumpObjectRegister función)

La `DbgDumpObjectRegister` función muestra información sobre los objetos activos. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En las compilaciones de depuración, la biblioteca de depuración mantiene una lista de objetos activos. La lista incluye todos los objetos que se derivan de [**CBaseObject**](cbaseobject.md), creados por el módulo actual y no se han destruido. Los métodos del constructor y el destructor de **CBaseObject** actualizan la lista.

Esta función genera varios mensajes de memoria de registro \_ . En el nivel de registro 1, la función muestra solo el número total de objetos. En el nivel de registro 2 o superior, se muestra una lista de los objetos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





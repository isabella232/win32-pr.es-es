---
description: La función DbgTerminate limpia la biblioteca de depuración. Se omite en las compilaciones comerciales.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Función DbgTerminate (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255266"
---
# <a name="dbgterminate-function"></a>Función DbgTerminate

La **función DbgTerminate** limpia la biblioteca de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a esta función si llama a [**la función DbgInitialise.**](dbginitialise.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





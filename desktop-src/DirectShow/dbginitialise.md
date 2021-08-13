---
description: La función DbgInitialise inicializa la biblioteca de depuración. Se omite en las compilaciones comerciales.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Función DbgInitialise (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13aad8d0214c65c01237c8e74548c3915af9287c935b53e33c6d229b2da5b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654220"
---
# <a name="dbginitialise-function"></a>Función DbgInitialise

La **función DbgInitialise** inicializa la biblioteca de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hInst* 
</dt> <dd>

Identificador de la instancia del módulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En un archivo ejecutable, llame a este método antes de usar las DirectShow de depuración. Antes de que se cierre el ejecutable, llame a la [**función DbgTerminate**](dbgterminate.md) para limpiar la biblioteca de depuración.

En un archivo DLL que se vincula a la biblioteca de clase base (Strmbase.lib), no es necesario llamar a esta función. Se llama automáticamente a la función cuando se carga el archivo DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





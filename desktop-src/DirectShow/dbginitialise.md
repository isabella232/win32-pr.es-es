---
description: La función DbgInitialise inicializa la biblioteca de depuración. Se omite en las compilaciones comerciales.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Función DbgInitialise (Wxdebug. h)
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
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679497"
---
# <a name="dbginitialise-function"></a>DbgInitialise función)

La función **DbgInitialise** inicializa la biblioteca de depuración. Se omite en las compilaciones comerciales.

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

Identificador de la instancia de módulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En un archivo ejecutable, llame a este método antes de usar las funciones de depuración de DirectShow. Antes de que se cierre el archivo ejecutable, llame a la función [**DbgTerminate**](dbgterminate.md) para limpiar la biblioteca de depuración.

En un archivo DLL que se vincula a la biblioteca de clases base (Strmbase. lib), no es necesario llamar a esta función. Se llama a la función automáticamente cuando se carga el archivo DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





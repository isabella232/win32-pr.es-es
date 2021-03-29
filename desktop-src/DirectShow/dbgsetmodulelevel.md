---
description: La función DbgSetModuleLevel establece el nivel de registro para uno o más tipos de mensaje. Se omite en las compilaciones comerciales.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Función DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660499"
---
# <a name="dbgsetmodulelevel-function"></a>DbgSetModuleLevel función)

La función **DbgSetModuleLevel** establece el nivel de registro para uno o más tipos de mensaje. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipos* 
</dt> <dd>

Combinación bit a bit de uno o varios tipos de mensaje.

</dd> <dt>

*Level* 
</dt> <dd>

Nivel de registro de los tipos de mensaje especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





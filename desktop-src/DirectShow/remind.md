---
description: La macro reminds genera un recordatorio en tiempo de compilación. Esta macro genera una cadena que incluye la cadena de parámetro, el nombre del archivo de código fuente y el número de línea.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: RECORDAR (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690460"
---
# <a name="remind"></a>TE

La `REMIND` macro genera un recordatorio en tiempo de compilación. Esta macro genera una cadena que incluye la cadena de parámetro, el nombre del archivo de código fuente y el número de línea.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Cadena de texto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta macro es útil para generar advertencias en tiempo de compilación:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





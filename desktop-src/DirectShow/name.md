---
description: La macro NAME genera una cadena de solo depuración.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NAME (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107694"
---
# <a name="name"></a>NOMBRE

La **macro NAME** genera una cadena de solo depuración.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Cadena de texto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En las compilaciones de depuración, esta macro es equivalente a la **macro TEXT.** En las compilaciones comerciales, se resuelve en (TCHAR \* ) **NULL**. Esta macro es útil al declarar el nombre de un objeto que deriva de la [**clase CBaseObject.**](cbaseobject.md)


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





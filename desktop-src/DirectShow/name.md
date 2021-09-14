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
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254264"
---
# <a name="name"></a>NAME

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

## <a name="remarks"></a>Observaciones

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

 

 





---
description: La macro NOTE envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Nota (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690914"
---
# <a name="note"></a>NOTA

La `NOTE` macro envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*
</dt> <dd>

Una cadena de formato de estilo printf.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*:*arg5*
</dt> <dd>

Argumentos adicionales para la cadena de formato. El número de argumentos debe coincidir con el nombre de la macro. Por ejemplo, **NOTE1** toma un argumento y **NOTE5** toma cinco argumentos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estas macros son variantes de la macro [**DbgLog**](dbglog.md) . Generan mensajes de seguimiento de registro de nivel 5 \_ .

## <a name="example"></a>Ejemplo


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
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

 

 





---
description: GuidNames es una matriz global de la biblioteca de clases base de DirectShow que contiene cadenas que representan los GUID definidos en UUID. h. Esta matriz es útil para generar la salida de depuración.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680200"
---
# <a name="guidnames"></a>GuidNames

`GuidNames` es una matriz global de la biblioteca de clases base de DirectShow que contiene cadenas que representan los GUID definidos en UUID. h. Esta matriz es útil para generar la salida de depuración.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*volumen*
</dt> <dd>

Especifica cualquier valor GUID definido en el archivo de encabezado UUID. h.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use esta matriz global para generar constantes GUID como cadenas. Por ejemplo, el código siguiente imprime la cadena "MEDIATYPE \_ video" en la consola:


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Si no se encuentra ninguna coincidencia con el GUID, se devuelve la cadena "nombre del GUID desconocido". No todos los GUID de DirectShow se definen en UUID. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





---
description: GuidNames es una matriz global de DirectShow biblioteca de clases base que contiene cadenas que representan los GUID definidos en Uuids.h. Esta matriz es útil para generar la salida de depuración.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169962"
---
# <a name="guidnames"></a>GuidNames

`GuidNames`es una matriz global de DirectShow biblioteca de clases base que contiene cadenas que representan los GUID definidos en Uuids.h. Esta matriz es útil para generar la salida de depuración.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*Guid*
</dt> <dd>

Especifica cualquier valor GUID definido en el archivo de encabezado Uuids.h.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use esta matriz global para generar constantes GUID como cadenas. Por ejemplo, el código siguiente imprime la cadena "MEDIATYPE \_ Video" en la consola:


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Si el GUID no coincide, se devuelve la cadena "Unknown GUID Name" (Nombre de GUID desconocido). No todos DirectShow GUID se definen en uuids.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 





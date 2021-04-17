---
description: La función WideStringFromResource carga una cadena de caracteres anchos de un archivo de recursos con el identificador de recursos especificado.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Función WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671066"
---
# <a name="widestringfromresource-function"></a>WideStringFromResource función)

La `WideStringFromResource` función carga una cadena de caracteres anchos de un archivo de recursos con el identificador de recursos especificado.

## <a name="syntax"></a>Sintaxis


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBuffer* 
</dt> <dd>

Puntero a la cadena que corresponde a *iResourceID*.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso de la cadena que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la misma cadena que *pBuffer*. Si la función no es correcta, devuelve una cadena nula.

## <a name="remarks"></a>Observaciones

Normalmente, se llama a las páginas de propiedades a través de sus interfaces COM, que usan cadenas de caracteres anchos independientemente de cómo se compile el binario. Esta función permite convertir una cadena de recursos en una cadena de caracteres anchos. La función convierte el recurso en una cadena de caracteres anchos (si aún no es uno) después de cargarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de páginas de propiedades](property-page-helper-functions.md)
</dt> </dl>

 

 





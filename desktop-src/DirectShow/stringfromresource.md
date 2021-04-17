---
description: La función StringFromResource carga una cadena desde un archivo de recursos con el identificador de recursos especificado.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Función StringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680944"
---
# <a name="stringfromresource-function"></a>StringFromResource función)

La `StringFromResource` función carga una cadena de un archivo de recursos con el identificador de recursos especificado.

## <a name="syntax"></a>Sintaxis


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
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

El búfer *pBuffer* debe ser al menos de \_ bytes de longitud máxima de Str \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de páginas de propiedades](property-page-helper-functions.md)
</dt> </dl>

 

 





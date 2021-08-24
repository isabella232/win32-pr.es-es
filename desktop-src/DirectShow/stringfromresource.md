---
description: La función StringFromResource carga una cadena desde un archivo de recursos con el identificador de recurso especificado.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Función StringFromResource (Wxutil.h)
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
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329656"
---
# <a name="stringfromresource-function"></a>Función StringFromResource

La `StringFromResource` función carga una cadena de un archivo de recursos con el identificador de recurso especificado.

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

Puntero a la cadena correspondiente a *iResourceID.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso de la cadena que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la misma cadena que *pBuffer.* Si la función no se realiza correctamente, devuelve una cadena null.

## <a name="remarks"></a>Comentarios

El *búfer pBuffer* debe ser al menos bytes STR \_ MAX \_ LENGTH.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de página de propiedades](property-page-helper-functions.md)
</dt> </dl>

 

 





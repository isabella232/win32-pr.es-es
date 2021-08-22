---
description: La función WideStringFromResource carga una cadena de caracteres anchos desde un archivo de recursos con el identificador de recurso especificado.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Función WideStringFromResource (Wxutil.h)
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
ms.openlocfilehash: 798f915536c491d32ccab7e7dbdc9b506d8b5df22b4459818472307e62356b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071819"
---
# <a name="widestringfromresource-function"></a>Función WideStringFromResource

La `WideStringFromResource` función carga una cadena de caracteres anchos desde un archivo de recursos con el identificador de recurso especificado.

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

Puntero a la cadena correspondiente a *iResourceID.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso de la cadena que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la misma cadena que *pBuffer.* Si la función no se realiza correctamente, devuelve una cadena null.

## <a name="remarks"></a>Comentarios

Normalmente, se llama a las páginas de propiedades a través de sus interfaces COM, que usan cadenas de caracteres anchos, independientemente de cómo se ha creado el binario. Esta función permite convertir una cadena de recursos en una cadena de caracteres anchos. La función convierte el recurso en una cadena de caracteres anchos (si aún no lo está) después de cargarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de página de propiedades](property-page-helper-functions.md)
</dt> </dl>

 

 





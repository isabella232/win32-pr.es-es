---
description: Recupera los datos de atributo para el archivo especificado.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Función SdbGetFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103655"
---
# <a name="sdbgetfileattributes-function"></a>Función SdbGetFileAttributes

Recupera los datos de atributo para el archivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpwszFileName* \[ En\]
</dt> <dd>

Ruta de acceso al archivo.

</dd> <dt>

*ppAttrInfo* \[ out\]
</dt> <dd>

Matriz de [**estructuras ATTRINFO**](attrinfo.md) que contienen los datos de atributo.

</dd> <dt>

*lpdwAttrCount* \[ out\]
</dt> <dd>

Número de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="remarks"></a>Comentarios

Cuando haya terminado con los datos, cándalo mediante la [**función SdbFreeFileAttributes.**](sdbfreefileattributes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 





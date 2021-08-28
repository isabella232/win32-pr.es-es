---
description: Convierte los datos de atributo especificados al formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Función SdbFormatAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 44303a568a9f7775893033edc512e8a916004c43207277e308e1d4826d9f9537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161565"
---
# <a name="sdbformatattribute-function"></a>Función SdbFormatAttribute

Convierte los datos de atributo especificados al formato XML.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttrInfo* \[ En\]
</dt> <dd>

Estructura [**ATTRINFO.**](attrinfo.md)

</dd> <dt>

*pchBuffer* \[ out\]
</dt> <dd>

Búfer de salida.

</dd> <dt>

*dwBufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer *pchBuffer,* en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta **correctamente** o FALSE si el búfer es demasiado pequeño o no se encuentra el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 





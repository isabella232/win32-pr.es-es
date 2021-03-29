---
description: Convierte los datos de atributos especificados al formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute función)
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
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906908"
---
# <a name="sdbformatattribute-function"></a>SdbFormatAttribute función)

Convierte los datos de atributos especificados al formato XML.

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

*pAttrInfo* \[ de\]
</dt> <dd>

Estructura [**ATTRINFO**](attrinfo.md) .

</dd> <dt>

*pchBuffer* \[ enuncia\]
</dt> <dd>

Búfer de salida.

</dd> <dt>

*dwBufferSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *pchBuffer* , en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si es correcto o **false** si el búfer es demasiado pequeño o no se encuentra el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 





---
description: Libera los datos de atributo de archivo especificados.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Función SdbFreeFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7e99180198f8f23ba6b6872502710b2af28aaff3999a9f315c33ef2d1874d987
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103675"
---
# <a name="sdbfreefileattributes-function"></a>Función SdbFreeFileAttributes

Libera los datos de atributo de archivo especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileAttributes* \[ En\]
</dt> <dd>

Estructura [**ATTRINFO devuelta**](attrinfo.md) por la [**función SdbGetFileAttributes.**](sdbgetfileattributes.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

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

 

 





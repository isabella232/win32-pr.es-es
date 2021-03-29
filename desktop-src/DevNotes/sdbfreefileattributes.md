---
description: Libera los datos de atributo de archivo especificados.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes función)
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
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806914"
---
# <a name="sdbfreefileattributes-function"></a>SdbFreeFileAttributes función)

Libera los datos de atributo de archivo especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileAttributes* \[ de\]
</dt> <dd>

Una estructura [**ATTRINFO**](attrinfo.md) devuelta por la función [**SdbGetFileAttributes**](sdbgetfileattributes.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

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

 

 





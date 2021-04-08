---
description: Crea una nueva base de datos de correcciones de compatibilidad.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000578"
---
# <a name="sdbcreatedatabase-function"></a>SdbCreateDatabase función)

Crea una nueva base de datos de correcciones de compatibilidad.

## <a name="syntax"></a>Sintaxis


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszPath* \[ de\]
</dt> <dd>

La ruta de acceso donde debe guardarse la base de datos. Este parámetro no puede ser **null**.

</dd> <dt>

*ETYPE* \[ de\]
</dt> <dd>

Tipo de ruta de acceso. Consulte [**\_ tipo de ruta de acceso**](path-type.md) para obtener una lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos de correcciones de compatibilidad o **null** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 





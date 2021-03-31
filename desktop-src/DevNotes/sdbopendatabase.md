---
description: Abre la base de datos de Shim especificada.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807040"
---
# <a name="sdbopendatabase-function"></a>SdbOpenDatabase función)

Abre la base de datos de Shim especificada.

## <a name="syntax"></a>Sintaxis


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszPath* \[ de\]
</dt> <dd>

Ruta de acceso de la base de datos. Este parámetro no puede ser **null**.

</dd> <dt>

*ETYPE* \[ de\]
</dt> <dd>

Tipo de ruta de acceso. Consulte [**\_ tipo de ruta de acceso**](path-type.md) para obtener una lista de valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos de correcciones de compatibilidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 





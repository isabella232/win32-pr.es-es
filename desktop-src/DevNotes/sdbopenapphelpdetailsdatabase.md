---
description: Abre la base de datos de detalles de Apphelp especificada.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Función SdbOpenApphelpDetailsDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045165"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>Función SdbOpenApphelpDetailsDatabase

Abre la base de datos de detalles de Apphelp especificada.

## <a name="syntax"></a>Sintaxis


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwsDetailsDatabasePath* \[ en, opcional\]
</dt> <dd>

Ruta de acceso de la base de datos. Si este parámetro es **NULL,** se abre la base de datos del sistema local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos de detalles de Apphelp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





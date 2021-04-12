---
description: Abre la base de datos de detalles de apphelp especificada.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase función)
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
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152703"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>SdbOpenApphelpDetailsDatabase función)

Abre la base de datos de detalles de apphelp especificada.

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

Ruta de acceso de la base de datos. Si este parámetro es **null**, se abre la base de datos del sistema local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador a la base de datos de detalles de apphelp.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





---
description: Crea una clave a partir de una cadena.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998043"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>SdbMakeIndexKeyFromString función)

Crea una clave a partir de una cadena.

## <a name="syntax"></a>Sintaxis


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszKey* \[ de\]
</dt> <dd>

La cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve la clave o 0 si se produce un error.

## <a name="remarks"></a>Observaciones

La clave de índice estándar son los ocho primeros caracteres de la cadena, convertidos en mayúsculas y, después, se convierten en un valor de **ULONGLONG** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





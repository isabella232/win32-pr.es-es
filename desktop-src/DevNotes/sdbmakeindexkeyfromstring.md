---
description: Crea una clave a partir de una cadena.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Función SdbMakeIndexKeyFromString
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
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161228"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Función SdbMakeIndexKeyFromString

Crea una clave a partir de una cadena.

## <a name="syntax"></a>Sintaxis


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszKey* \[ En\]
</dt> <dd>

La cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve la clave o 0 si se produce un error.

## <a name="remarks"></a>Comentarios

La clave de índice estándar es los ocho primeros caracteres de la cadena, convertidos a mayúsculas y luego convertidos en un **valor ULONGLONG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





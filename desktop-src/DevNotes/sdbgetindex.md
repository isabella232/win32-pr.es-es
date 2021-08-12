---
description: Recupera el índice de la etiqueta y el tipo de clave especificados de la base de datos especificada.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Función SdbGetIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 36bfa9df62aba2ce8fb1df637c802369ca35911bd02c9876ea6b649c66698685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666480"
---
# <a name="sdbgetindex-function"></a>Función SdbGetIndex

Recupera el índice de la etiqueta y el tipo de clave especificados de la base de datos especificada.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tWhich* \[ En\]
</dt> <dd>

ETIQUETA.

</dd> <dt>

*tKey* \[ En\]
</dt> <dd>

El tipo de clave.

</dd> <dt>

*lpdwFlags* \[ out, opcional\]
</dt> <dd>

Este parámetro puede ser 0 o **SHIMDB \_ INDEX UNIQUE \_ \_ KEY** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TAGID **del** índice o **TAGID \_ NULL.**

## <a name="remarks"></a>Observaciones

El índice resultante se puede usar para las operaciones de lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





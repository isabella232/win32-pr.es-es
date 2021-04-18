---
description: Recupera el índice de la etiqueta y el tipo de clave especificados de la base de datos especificada.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex función)
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
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496175"
---
# <a name="sdbgetindex-function"></a>SdbGetIndex función)

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tWhich* \[ de\]
</dt> <dd>

ETIQUETA.

</dd> <dt>

*tKey* \[ de\]
</dt> <dd>

El tipo de clave.

</dd> <dt>

*lpdwFlags* \[ out, opcional\]
</dt> <dd>

Este parámetro puede ser 0 o **SHIMDB \_ \_ Unique index \_ key** (0x00000001).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TagID** del índice o **TagID \_ null**.

## <a name="remarks"></a>Observaciones

El índice resultante se puede usar para operaciones de lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





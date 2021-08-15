---
description: Busca el primer registro DWORD en el índice especificado que cumple los criterios especificados.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Función SdbFindFirstDWORDIndexedTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161576"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Función SdbFindFirstDWORDIndexedTag

Busca el primer **registro DWORD** en el índice especificado que cumple los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
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

Tipo de índice. Consulte [**TAG**](tag.md) para obtener una lista de valores.

</dd> <dt>

*tKey* \[ En\]
</dt> <dd>

El tipo de clave.

</dd> <dt>

*dwName* \[ En\]
</dt> <dd>

Nombre de los datos que se va a encontrar. Este valor se convertirá en una clave.

</dd> <dt>

*pFindInfo* \[ out\]
</dt> <dd>

Estructura [**FIND \_ INFO**](find-info.md) que recibe el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TAGID **de la** primera coincidencia o **TAG \_ NULL** si no se encuentra ninguna coincidencia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 





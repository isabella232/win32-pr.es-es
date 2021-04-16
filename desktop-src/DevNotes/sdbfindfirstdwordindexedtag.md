---
description: Busca el primer registro DWORD en el índice especificado que cumpla los criterios especificados.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag función)
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
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538265"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>SdbFindFirstDWORDIndexedTag función)

Busca el primer registro **DWORD** en el índice especificado que cumpla los criterios especificados.

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tWhich* \[ de\]
</dt> <dd>

Tipo de índice. Vea [**etiqueta**](tag.md) para obtener una lista de valores.

</dd> <dt>

*tKey* \[ de\]
</dt> <dd>

El tipo de clave.

</dd> <dt>

*dwName* \[ de\]
</dt> <dd>

Nombre de los datos que se van a buscar. Este valor se convertirá en una clave.

</dd> <dt>

*pFindInfo* \[ enuncia\]
</dt> <dd>

Una estructura de [**\_ información de búsqueda**](find-info.md) que recibe el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TAGID** de la primera coincidencia o **etiqueta \_ null** si no se encuentra ninguna coincidencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 





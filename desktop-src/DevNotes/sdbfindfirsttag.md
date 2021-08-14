---
description: Busca una coincidencia TAG dentro del elemento primario especificado y devuelve el TAGID de la primera coincidencia.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Función SdbFindFirstTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f6562589158e5c3a5e1b65273451f812802c1c73b76f52c47274c06b9639f5ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390235"
---
# <a name="sdbfindfirsttag-function"></a>Función SdbFindFirstTag

Busca una coincidencia TAG dentro del elemento primario especificado y devuelve el **TAGID** de la primera coincidencia.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ En\]
</dt> <dd>

Identificador de la base de datos shim.

</dd> <dt>

*tiParent* \[ En\]
</dt> <dd>

TAGID **del** inicio de búsqueda. Este parámetro puede ser **TAGID \_ ROOT o** **TAG TYPE \_ \_ LIST.**

</dd> <dt>

*tTag* \[ En\]
</dt> <dd>

Etiqueta con la que se va a coincidir. Consulte [TAG](tag.md) para obtener una lista de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TAGID **de** la primera coincidencia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 





---
description: Busca la siguiente coincidencia TAG dentro del elemento primario especificado y devuelve el TAGID de la coincidencia.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Función SdbFindNextTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: fe9b9914ed9126a364fb377adc4afae84784df156a8e75c3d0d2f997f6185811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103705"
---
# <a name="sdbfindnexttag-function"></a>Función SdbFindNextTag

Busca la siguiente coincidencia TAG dentro del elemento primario especificado y devuelve **el TAGID** de la coincidencia.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

*tiPrev* \[ En\]
</dt> <dd>

TAGID **de** la coincidencia anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TAGID **de** la coincidencia.

## <a name="remarks"></a>Comentarios

Antes de llamar a esta función, llame a [**la función SdbFindFirstTag.**](sdbfindfirsttag.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 





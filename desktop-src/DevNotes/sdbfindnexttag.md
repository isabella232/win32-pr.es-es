---
description: Busca la siguiente coincidencia de etiqueta en el elemento primario especificado y devuelve el TAGID de la coincidencia.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag función)
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
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907112"
---
# <a name="sdbfindnexttag-function"></a>SdbFindNextTag función)

Busca la siguiente coincidencia de etiqueta en el elemento primario especificado y devuelve el **TAGID** de la coincidencia.

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tiParent* \[ de\]
</dt> <dd>

El **TAGID** del inicio de la búsqueda. Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.

</dd> <dt>

*tiPrev* \[ de\]
</dt> <dd>

El **TAGID** de la coincidencia anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TAGID** de la coincidencia.

## <a name="remarks"></a>Observaciones

Antes de llamar a esta función, llame a la función [**SdbFindFirstTag**](sdbfindfirsttag.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 





---
description: Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del siguiente elemento secundario.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907190"
---
# <a name="sdbgetnextchild-function"></a>SdbGetNextChild función)

Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del siguiente elemento secundario.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbGetNextChild(
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

**TAGID** del elemento secundario anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TagID** del elemento secundario o **TagID \_ null** si no se encuentra ningún elemento secundario.

## <a name="remarks"></a>Observaciones

Antes de llamar a esta función, llame a la función [**SdbGetFirstChild**](sdbgetfirstchild.md) .

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

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 





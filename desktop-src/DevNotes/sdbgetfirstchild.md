---
description: Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del primer elemento secundario.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538254"
---
# <a name="sdbgetfirstchild-function"></a>SdbGetFirstChild función)

Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del primer elemento secundario.

## <a name="syntax"></a>Sintaxis


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor de **TagID** del primer elemento secundario o **TagID \_ null** no se encuentra.

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

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 





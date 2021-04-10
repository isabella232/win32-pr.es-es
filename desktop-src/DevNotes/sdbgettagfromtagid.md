---
description: Recupera la etiqueta asociada al TAGID especificado.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153070"
---
# <a name="sdbgettagfromtagid-function"></a>SdbGetTagFromTagID función)

Recupera la etiqueta asociada al **TAGID** especificado.

## <a name="syntax"></a>Sintaxis


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tiWhich* \[ de\]
</dt> <dd>

**TAGID** de la etiqueta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve la etiqueta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ETIQUETA**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 





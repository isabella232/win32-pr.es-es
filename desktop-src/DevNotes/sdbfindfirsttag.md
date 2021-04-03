---
description: Busca una coincidencia de etiqueta en el elemento primario especificado y devuelve el TAGID de la primera coincidencia.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag función)
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
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998045"
---
# <a name="sdbfindfirsttag-function"></a>SdbFindFirstTag función)

Busca una coincidencia de etiqueta en el elemento primario especificado y devuelve el **TAGID** de la primera coincidencia.

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

archivo *PDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad.

</dd> <dt>

*tiParent* \[ de\]
</dt> <dd>

El **TAGID** del inicio de la búsqueda. Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.

</dd> <dt>

*tTag* \[ de\]
</dt> <dd>

ETIQUETA que se va a comparar. Vea [etiqueta](tag.md) para obtener una lista de valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TAGID** de la primera coincidencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 





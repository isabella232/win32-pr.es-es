---
description: Recupera el TAGID y un identificador de la base de datos shim para el TAGREF especificado.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Función SdbTagRefToTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: feeb622fd196ed20efb60d866d59b634fdcd9ecd955a97a1d7af0aef1347c8f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815325"
---
# <a name="sdbtagreftotagid-function"></a>Función SdbTagRefToTagID

Recupera el **TAGID y un** identificador de la base de datos shim para el [**TAGREF especificado.**](tagref.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSDB* \[ En\]
</dt> <dd>

Identificador de la base de datos shim devuelta por la [**función SdbInitDatabase.**](sdbinitdatabase.md)

</dd> <dt>

*trWhich* \[ En\]
</dt> <dd>

[**TAGREF**](tagref.md).

</dd> <dt>

*ppdb* \[ out\]
</dt> <dd>

Identificador resultante de la base de datos shim.

</dd> <dt>

*ptiWhich* \[ out\]
</dt> <dd>

TagID **resultante.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **TRUE si** se ejecuta correctamente o **FALSE** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 





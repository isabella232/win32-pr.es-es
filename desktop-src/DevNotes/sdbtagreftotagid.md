---
description: Recupera el TAGID y un identificador de la base de datos de Shim para el TAGREF especificado.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID función)
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
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152958"
---
# <a name="sdbtagreftotagid-function"></a>SdbTagRefToTagID función)

Recupera el **TAGID** y un identificador de la base de datos de Shim para el [**TAGREF**](tagref.md)especificado.

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

*hSDB* \[ de\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*trWhich* \[ de\]
</dt> <dd>

[**TAGREF**](tagref.md).

</dd> <dt>

*ppdb* \[ enuncia\]
</dt> <dd>

El identificador resultante para la base de datos de Shim.

</dd> <dt>

*ptiWhich* \[ enuncia\]
</dt> <dd>

El **TAGID** resultante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 





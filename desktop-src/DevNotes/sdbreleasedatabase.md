---
description: Cierra la base de datos shim inicializada mediante la función SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Función SdbReleaseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 82a7cf785927a5ef14e3e033c29233afcc4a49cf89d610757d110583bce4eff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815335"
---
# <a name="sdbreleasedatabase-function"></a>Función SdbReleaseDatabase

Cierra la base de datos shim inicializada mediante la [**función SdbInitDatabase.**](sdbinitdatabase.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSDB* \[ En\]
</dt> <dd>

Identificador de la base de datos shim devuelta por la [**función SdbInitDatabase.**](sdbinitdatabase.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 





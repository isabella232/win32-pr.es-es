---
description: Cierra la base de datos de correcciones de compatibilidad (shim) especificada.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Función SdbCloseDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 06e7b493d6114b4085dcabcfd5f241413b431daa081c53fd467b100e225f486c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161596"
---
# <a name="sdbclosedatabase-function"></a>Función SdbCloseDatabase

Cierra la base de datos de correcciones de compatibilidad (shim) especificada.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdb* \[ in, out\]
</dt> <dd>

Identificador de la base de datos shim. Este parámetro no puede ser **NULL.**

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

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 





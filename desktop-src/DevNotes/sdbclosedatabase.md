---
description: Cierra la base de datos de Shim especificada.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase función)
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
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080185"
---
# <a name="sdbclosedatabase-function"></a>SdbCloseDatabase función)

Cierra la base de datos de Shim especificada.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

archivo *PDB* \[ in, out\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 





---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Unión de tipos escalares.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418079"
---
# <a name="dml_scalar_union-union-directmlh"></a>DML_SCALAR_UNION union (directml.h)
Unión de tipos escalares.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a>Miembros

`Bytes`

Matriz de 8 bytes.


`Int8`

Entero de 8 bits con signo.


`UInt8`

Entero de 8 bits sin signo.


`Int16`

Entero de 16 bits con signo.


`UInt16`

Entero de 16 bits sin signo.


`Int32`

Entero de 32 bits con signo.


`UInt32`

Entero de 32 bits sin signo.


`Int64`

Entero de 64 bits con signo.


`UInt64`

Entero de 64 bits sin signo.


`Float32`

Número de punto flotante de precisión sencilla.


`Float64`

Número de punto flotante de precisión doble.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
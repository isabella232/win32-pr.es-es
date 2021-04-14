---
description: Contiene una matriz de blobs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Estructura de BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276699"
---
# <a name="blob_table-structure"></a>\_Estructura de tabla BLOB

La estructura de la **\_ tabla BLOB** contiene una matriz de blobs.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indicador que siguen muchos BLOBs.

</dd> <dt>

**hBlobs**
</dt> <dd>

Identificador de la matriz de BLOBs.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





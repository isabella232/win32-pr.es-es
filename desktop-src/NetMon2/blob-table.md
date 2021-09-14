---
description: Contiene una matriz de blobs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: BLOB_TABLE estructura (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161155"
---
# <a name="blob_table-structure"></a>Estructura \_ BLOB TABLE

La **estructura \_ BLOB TABLE** contiene una matriz de blobs.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indicador que siguen muchos blobs.

</dd> <dt>

**hBlobs**
</dt> <dd>

Identificador de la matriz BLOB.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





---
description: Contiene una matriz de BLOB.
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
ms.openlocfilehash: e0615ad9c11657a47d9eaa87035207cb499634cd4ded6ae484d6f5d256c23e15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144348"
---
# <a name="blob_table-structure"></a>Estructura \_ BLOB TABLE

La **estructura BLOB \_ TABLE** contiene una matriz de BLOB.

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

Indicador que siguen muchos BLOB.

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



 

 





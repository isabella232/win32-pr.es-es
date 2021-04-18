---
description: Asocia un nombre de grupo y su identificador.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Estructura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666272"
---
# <a name="groupinfo-structure"></a>Estructura GROUPINFO

La estructura **GROUPINFO** asocia un nombre de grupo y su identificador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szGroupName**
</dt> <dd>

Valor incrementado de una matriz en la estructura **GROUPNAME** .

</dd> <dt>

**hGroup**
</dt> <dd>

Identificador de un grupo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





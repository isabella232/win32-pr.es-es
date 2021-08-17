---
title: MPRESERVED_DATA estructura (MpClient.h)
description: Datos de notificación reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA estructura heredada de Windows environment
- PMPRESERVED_DATA puntero de estructura heredado Windows environment Features
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747659"
---
# <a name="mpreserved_data-structure"></a>Estructura DE DATOS MPRESERVED \_

Datos de notificación reservados.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbReservedData**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos reservados, en bytes.

</dd> <dt>

**pbReservedData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntero a datos reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






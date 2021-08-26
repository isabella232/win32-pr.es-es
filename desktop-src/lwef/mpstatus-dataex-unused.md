---
title: MPSTATUS_DATAEX_UNUSED estructura (MpClient.h)
description: Estructura ficticia para no SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED estructura heredada de Windows environment
- PMPSTATUS_DATAEX_UNUSED puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245315d12b5fbe76ec2f552e510336aa3974753678e04f87c33546737f180c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961095"
---
# <a name="mpstatus_dataex_unused-structure"></a>Estructura NO \_ UTILIZADA DE MPSTATUS DATAEX \_

Estructura ficticia para no SRP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwNone**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






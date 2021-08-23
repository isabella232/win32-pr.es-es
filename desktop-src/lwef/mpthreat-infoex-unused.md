---
title: MPTHREAT_INFOEX_UNUSED estructura (MpClient.h)
description: Estructura ficticia para amenazas de tipos de modificación que no son de comportamiento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED Legacy Windows Environment Features
- PMPTHREAT_INFOEX_UNUSED puntero de estructura heredado de Windows environment
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8def13a6f6aff010b9854055abd4636d19f77ef1f0e9867ec5e4d7562baff4f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601105"
---
# <a name="mpthreat_infoex_unused-structure"></a>Estructura MPTHREAT \_ INFOEX \_ UNUSED

Estructura ficticia para amenazas de tipos de modificación que no son de comportamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwNone**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






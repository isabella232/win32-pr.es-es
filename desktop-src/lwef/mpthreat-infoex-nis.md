---
title: MPTHREAT_INFOEX_NIS estructura (MpClient.h)
description: Contiene información específica de NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS estructura heredada de Windows environment
- PMPTHREAT_INFOEX_NIS puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8320070f80000ec5c2b235a815dc075f96f82ddd3c6d56c4022b9d60759c3e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746904"
---
# <a name="mpthreat_infoex_nis-structure"></a>Estructura NIS de MPTHREAT \_ INFOEX \_

Contiene información específica de NIS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**SourceIP**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd></dd> <dt>

**DestinationIP**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd></dd> <dt>

**dwSourceport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**dwDestinationport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**Protocolo**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd></dd> <dt>

**Vínculo**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






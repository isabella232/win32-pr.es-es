---
title: MPNIS_PRIVATE_DATA estructura (MpClient.h)
description: Notificaciones privadas de NIS.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA estructura heredada de Windows environment
- PMPNIS_PRIVATE_DATA puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50719e4ecc0beff848467023a1c5f941ff06ceb891b05674e199d47a38b8659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556145"
---
# <a name="mpnis_private_data-structure"></a>Estructura DE \_ DATOS PRIVADOS DE MPZON \_

Notificaciones privadas de NIS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de notificación.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de los datos reservados, en bytes.

</dd> <dt>

**pbData**
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



 

 






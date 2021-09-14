---
title: MPHEALTH_DATA estructura (MpClient.h)
description: Datos de notificación de estado.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA estructura heredada de Windows environment
- PMPHEALTH_DATA puntero de estructura heredados Windows environment features
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360086"
---
# <a name="mphealth_data-structure"></a>Estructura DE DATOS \_ MPHEALTH

Datos de notificación de estado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de notificación.

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sin usar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






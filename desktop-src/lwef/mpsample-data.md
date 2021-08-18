---
title: MPSAMPLE_DATA estructura (MpClient.h)
description: Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA estructura heredada de Windows environment
- PMPSAMPLE_DATA puntero de estructura heredado Windows de entorno
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafafd2ff7162dcb50bd5e2ea92cd56ab9f073332238dc0742845f9c48c5a588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747418"
---
# <a name="mpsample_data-structure"></a>Estructura DE \_ DATOS MPSAMPLE

Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSampleIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Índice del elemento de ejemplo para el que se notifica el estado de envío.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






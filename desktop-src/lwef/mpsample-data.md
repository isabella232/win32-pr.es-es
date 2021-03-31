---
title: MPSAMPLE_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSAMPLE_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151158"
---
# <a name="mpsample_data-structure"></a>\_Estructura de datos MPSAMPLE

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

Índice del elemento de ejemplo para el que se registra el estado del envío.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






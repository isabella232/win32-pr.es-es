---
title: MPRESERVED_DATA estructura (MpClient. h)
description: Datos de notificación reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESERVED_DATA características de entorno heredado de Windows
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
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150575"
---
# <a name="mpreserved_data-structure"></a>\_Estructura de datos MPRESERVED

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

Tipo: **byte \***

</dd> <dd>

Puntero a los datos reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






---
title: MPTHREAT_INFOEX_UNUSED estructura (MpClient. h)
description: Estructura ficticia para amenazas de tipo de modificación sin comportamiento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_UNUSED características de entorno heredado de Windows
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
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150571"
---
# <a name="mpthreat_infoex_unused-structure"></a>MPTHREAT \_ INFOEX de la \_ estructura no usada

Estructura ficticia para amenazas de tipo de modificación sin comportamiento.

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






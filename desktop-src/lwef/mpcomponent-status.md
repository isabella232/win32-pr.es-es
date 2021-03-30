---
title: MPCOMPONENT_STATUS estructura (MpClient. h)
description: Información de estado del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCOMPONENT_STATUS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801916"
---
# <a name="mpcomponent_status-structure"></a>Estructura de estado de MPCOMPONENT \_

Información de estado del componente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**fEnable**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

Estado del componente.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de éxito o error asociado al estado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






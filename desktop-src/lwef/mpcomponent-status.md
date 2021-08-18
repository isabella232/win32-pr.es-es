---
title: MPCOMPONENT_STATUS estructura (MpClient.h)
description: Información de estado del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS estructura heredada de Windows environment
- PMPCOMPONENT_STATUS puntero de estructura Legacy Windows Environment Features
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
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747803"
---
# <a name="mpcomponent_status-structure"></a>Estructura MPCOMPONENT \_ STATUS

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

Tipo: **BOOL**

</dd> <dd>

Estado del componente.

</dd> <dt>

**Hresult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código correcto o de error asociado al estado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






---
title: MPCOMPONENT_VERSION estructura (MpClient.h)
description: Versión y hora de actualización de un componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION estructura heredada de Windows environment
- PMPCOMPONENT_VERSION puntero de estructura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976075"
---
# <a name="mpcomponent_version-structure"></a>Estructura DE VERSIÓN DE MPCOMPONENT \_

Versión y hora de actualización de un componente individual.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Campo Versión. Cada **WORD** representa la versión principal, secundaria, de compilación y revisión.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ENTERO \_ ULARGE**

</dd> <dd>

Hora de la última actualización del componente, en **formato FILETIME.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






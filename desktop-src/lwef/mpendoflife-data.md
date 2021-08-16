---
title: MPENDOFLIFE_DATA estructura (MpClient.h)
description: '\ 0034; Fin del ciclo de vida \ 0034; datos de notificación.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA estructura heredada de Windows environment
- PMPENDOFLIFE_DATA puntero de estructura heredado de Windows Environment Features
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476287"
---
# <a name="mpendoflife_data-structure"></a>Estructura DE DATOS MPENDOFLIFE \_

Datos de notificación de "fin de ciclo de vida".

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Hora a la que expira la firma.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Hora a la que expira la plataforma.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True si el administrador controla la directiva para mostrar la notificación. Si se establece, indica a la interfaz de usuario que no muestre la notificación EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True si "Fin de la vida" está pendiente o pasado. Si es false, la interfaz de usuario y los clientes pueden borrar los estados relacionados con EOL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






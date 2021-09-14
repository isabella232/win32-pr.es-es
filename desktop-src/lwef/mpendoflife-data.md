---
title: MPENDOFLIFE_DATA estructura (MpClient.h)
description: '\ 0034; Fin del ciclo de vida \ 0034; datos de notificación.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA estructura heredada de Windows environment
- PMPENDOFLIFE_DATA puntero de estructura Legacy Windows Environment Features
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
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258031"
---
# <a name="mpendoflife_data-structure"></a>Estructura DE DATOS MPENDOFLIFE \_

Datos de notificación de "Fin del ciclo de vida".

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Members

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

True si "Final del ciclo de vida" está pendiente o pasado. Si es false, la interfaz de usuario y los clientes pueden borrar los estados relacionados con EOL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






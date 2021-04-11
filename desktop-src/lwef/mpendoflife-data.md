---
title: MPENDOFLIFE_DATA estructura (MpClient. h)
description: '\ 0034; Final de la vida \ 0034; datos de notificación.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPENDOFLIFE_DATA características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150676"
---
# <a name="mpendoflife_data-structure"></a>\_Estructura de datos MPENDOFLIFE

Datos de notificación de "fin de la vida".

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

Tipo: **bool**

</dd> <dd>

True si el administrador controla la Directiva para mostrar la notificación. Si se establece, indica a la interfaz de usuario que no muestre la notificación EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True si "fin de la vida" está pendiente o pasado. Si es false, la interfaz de usuario y los clientes pueden borrar cualquier estado relacionado con EOL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






---
description: La estructura PROTOCOLINFO describe un protocolo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Estructura PROTOCOLINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d44bf19f651f9391dcfc872798f709c463a74ce22b328c6942a32ca1a98636a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889765"
---
# <a name="protocolinfo-structure"></a>PROTOCOLINFO (estructura)

La **estructura PROTOCOLINFO** describe un protocolo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ProtocolID**
</dt> <dd>

Identificador de protocolo asignado por el sistema de la sesión de ejecución especificada.

</dd> <dt>

**PropertyDatabase**
</dt> <dd>

Base de datos de propiedades del protocolo especificado.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Nombre abreviado del protocolo.

</dd> <dt>

**Helpfile**
</dt> <dd>

Nombre de archivo de Ayuda opcional asociado al protocolo.

</dd> <dt>

**Comment**
</dt> <dd>

Comentario que describe el protocolo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





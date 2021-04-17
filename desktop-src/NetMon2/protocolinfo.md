---
description: La estructura PROTOCOLINFO describe un protocolo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Estructura PROTOCOLINFO (Netmon. h)
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
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678178"
---
# <a name="protocolinfo-structure"></a>Estructura PROTOCOLINFO

La estructura **PROTOCOLINFO** describe un protocolo.

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

Nombre abreviado de protocolo.

</dd> <dt>

**HelpFile**
</dt> <dd>

Nombre de archivo de ayuda opcional asociado al Protocolo.

</dd> <dt>

**Comentario**
</dt> <dd>

Comentario que describe el protocolo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





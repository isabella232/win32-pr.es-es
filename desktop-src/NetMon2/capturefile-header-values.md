---
description: Define la estructura del archivo de encabezado Monitor de red.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Estructura de CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652661"
---
# <a name="capturefile_header_values-structure"></a>CAPTUREFILE \_ estructura de valores de encabezado \_

La estructura de **\_ \_ los valores del encabezado CAPTUREFILE** define la estructura del archivo de encabezado monitor de red.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Signature**
</dt> <dd>

Identificador único: ' GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binario, decimal codificado (secundaria). El valor de este miembro debe ser cero (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Decimal codificado binario (principal). Este valor debe ser 2.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de topología.

</dd> <dt>

**Indicaciones**
</dt> <dd>

Hora de captura.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Tabla de índice de fotogramas.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Tamaño de la tabla de índice de fotogramas.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Desplazamiento de datos del usuario.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Longitud de los datos de usuario.

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

Desplazamiento de datos de comentario.

</dd> <dt>

**CommentDataLength**
</dt> <dd>

Longitud de los datos de comentario.

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

Desplazamiento a la estructura **Statistics** .

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Longitud de la estructura de **estadísticas** .

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Desplazamiento a la estructura **NETWORKINFO** .

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Longitud de la estructura **NETWORKINFO** .

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

Este miembro no se usa.

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

Este miembro no se usa.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





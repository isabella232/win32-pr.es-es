---
description: Define la estructura Monitor de red archivo de encabezado.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: CAPTUREFILE_HEADER_VALUES estructura (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253922"
---
# <a name="capturefile_header_values-structure"></a>Estructura CAPTUREFILE \_ HEADER \_ VALUES

La **estructura CAPTUREFILE \_ HEADER \_ VALUES** define la estructura Monitor de red archivo de encabezado.

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



## <a name="members"></a>Members

<dl> <dt>

**Signature**
</dt> <dd>

Identificador único: 'GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binario, decimal codificado (menor). El valor de este miembro debe ser cero (0).

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Decimal binario codificado (principal). Este valor debe ser 2.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de topología.

</dd> <dt>

**Timestamp**
</dt> <dd>

Tiempo de captura.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Tabla de índice de marco.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Tamaño de tabla de índice de marco.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Desplazamiento de datos del usuario.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Longitud de los datos del usuario.

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

Desplazamiento a la **estructura STATISTICS.**

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Longitud de la **estructura STATISTICS.**

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Desplazamiento a la **estructura NETWORKINFO.**

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Longitud de la **estructura NETWORKINFO.**

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
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





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
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367421"
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



## <a name="members"></a>Miembros

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

Desplazamiento de datos de usuario.

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



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





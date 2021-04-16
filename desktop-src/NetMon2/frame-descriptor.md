---
description: La estructura de descriptores de fotogramas \_ proporciona información descriptiva sobre fotogramas sin formato.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Estructura de FRAME_DESCRIPTOR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677291"
---
# <a name="frame_descriptor-structure"></a>\_Estructura de descriptor de marco

La estructura de **\_ descriptores de fotogramas** proporciona información descriptiva sobre fotogramas sin formato.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FramePointer**
</dt> <dd>

Puntero a los datos del marco.

</dd> <dt>

**Indicaciones**
</dt> <dd>

Hora del sistema, en microsegundos, en que se capturó el fotograma. Este tiempo se usa normalmente para determinar el intervalo entre las veces que se capturaron dos fotogramas.

</dd> <dt>

**FrameLength**
</dt> <dd>

Longitud del marco.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Longitud de fotograma real copiada.

</dd> <dt>

**ETYPE**
</dt> <dd>

ETYPE nombre.

</dd> <dt>

**SAP**
</dt> <dd>

Valor de SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Índice de protocolo encontrado.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Desplazamiento a los datos de protocolo obtenidos de **LowProtocol**.

</dd> <dt>

**HighPort**
</dt> <dd>

Puerto del protocolo alto identificado en **LowProtocol**.

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Desplazamiento a los datos de protocolo obtenidos de **HighPort**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





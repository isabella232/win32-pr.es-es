---
description: La estructura \_ FRAME DESCRIPTOR proporciona información descriptiva sobre los marcos sin procesar.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: FRAME_DESCRIPTOR estructura (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074156"
---
# <a name="frame_descriptor-structure"></a>Estructura \_ DEL DESCRIPTOR DE MARCO

La **estructura \_ FRAME DESCRIPTOR** proporciona información descriptiva sobre los marcos sin procesar.

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



## <a name="members"></a>Members

<dl> <dt>

**FramePointer**
</dt> <dd>

Puntero a los datos de marco.

</dd> <dt>

**Timestamp**
</dt> <dd>

Hora del sistema, en microsegundos, cuando se capturó el fotograma. Esta hora se usa normalmente para determinar el intervalo entre las veces que se capturaron dos fotogramas.

</dd> <dt>

**FrameLength**
</dt> <dd>

Longitud del marco.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Longitud real del fotograma copiada.

</dd> <dt>

**Tipo E**
</dt> <dd>

Nombre del tipo E.

</dd> <dt>

**Sap**
</dt> <dd>

Valor de SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Índice del protocolo encontrado.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Desplazamiento a los datos de protocolo obtenidos **de LowProtocol.**

</dd> <dt>

**HighPort**
</dt> <dd>

Puerto de protocolo alto identificado en **LowProtocol**.

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Desplazamiento a los datos de protocolo obtenidos **de HighPort.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





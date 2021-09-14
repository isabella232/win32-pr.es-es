---
description: Marco real del controlador.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Estructura FRAME (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074155"
---
# <a name="frame-structure"></a>Estructura FRAME

La **estructura FRAME** es un marco real del controlador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Members

<dl> <dt>

**Timestamp**
</dt> <dd>

Tiempo transcurrido, en microsegundos, entre el inicio de la captura y la hora en que se capturó el fotograma.

</dd> <dt>

**FrameLength**
</dt> <dd>

Longitud del marco MAC.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Longitud real del fotograma copiada.

</dd> <dt>

**MacFrame**
</dt> <dd>

Datos de marco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





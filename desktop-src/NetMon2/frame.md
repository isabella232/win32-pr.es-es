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
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910955"
---
# <a name="frame-structure"></a>Estructura FRAME

La **estructura FRAME** es un fotograma real del controlador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Miembros

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



 

 





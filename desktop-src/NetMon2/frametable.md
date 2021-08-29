---
description: La estructura FRAMETABLE, un búfer circular de punteros de marco, se entrega a las aplicaciones conectadas a la interfaz ITRC del NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Estructura FRAMETABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 214a9e947c7aba34f0cc65d1df8d56a57b9d1087e168824494f64e30bd8098e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890745"
---
# <a name="frametable-structure"></a>Estructura FRAMETABLE

La **estructura FRAMETABLE,** un búfer circular de punteros de marco, se entrega a las aplicaciones conectadas a la **interfaz ITRC** del NPP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**FrameTableLength**
</dt> <dd>

Longitud total de la tabla.

</dd> <dt>

**Startindex**
</dt> <dd>

Primer índice de la tabla.

</dd> <dt>

**Endindex**
</dt> <dd>

Último índice de la tabla.

</dd> <dt>

**FrameCount**
</dt> <dd>

Número de fotogramas descritos en esta tabla.

</dd> <dt>

**Marcos**
</dt> <dd>

Matriz real de descriptores de marco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





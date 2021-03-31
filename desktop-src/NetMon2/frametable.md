---
description: La estructura FRAMETABLE, un búfer circular de punteros de Marcos, se reenvía a las aplicaciones adjuntas a la interfaz ITRC de NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: Estructura FRAMETABLE (Netmon. h)
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
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153863"
---
# <a name="frametable-structure"></a>Estructura FRAMETABLE

La estructura **frametable** , un búfer circular de punteros de Marcos, se reenvía a las aplicaciones adjuntas a la interfaz **ITRC** de NPP.

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

La longitud total de la tabla.

</dd> <dt>

**Super**
</dt> <dd>

Primer índice de la tabla.

</dd> <dt>

**EndIndex**
</dt> <dd>

Último índice de la tabla.

</dd> <dt>

**FrameCount**
</dt> <dd>

Número de fotogramas descritos en esta tabla.

</dd> <dt>

**Imágenes**
</dt> <dd>

Matriz real de descriptores de marco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





---
description: La estructura del DESENCADENAdor indica una acción que debe llevar a cabo el controlador en un momento determinado.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Estructura del DESENCADENAdor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678207"
---
# <a name="trigger-structure"></a>Estructura del DESENCADENAdor

La estructura del **desencadenador** indica una acción que debe llevar a cabo el controlador en un momento determinado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TriggerActive**
</dt> <dd>

Valor booleano que determina si el controlador debe prestar atención al desencadenador.

</dd> <dt>

**TriggerType**
</dt> <dd>

Código de operación del desencadenador.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Acción que el desencadenador debe llevar a cabo si se activa.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Marcas de desencadenador.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Coincidencia de patrón de desencadenador.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Tamaño del búfer del desencadenador.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





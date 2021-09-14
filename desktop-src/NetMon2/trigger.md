---
description: La estructura TRIGGER indica una acción que debe realizar el controlador en un momento especificado.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Estructura TRIGGER (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260348"
---
# <a name="trigger-structure"></a>TRIGGER (estructura)

La **estructura TRIGGER** indica una acción que debe realizar el controlador en un momento especificado.

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



## <a name="members"></a>Members

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

Acción que debe realizar el desencadenador si se activa.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Marcas de desencadenador.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Coincidencia del patrón de desencadenador.

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
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





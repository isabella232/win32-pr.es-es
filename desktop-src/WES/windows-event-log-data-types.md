---
title: Windows Tipos de datos del registro de eventos (WinEvt.h)
description: Windows El registro de eventos define los siguientes tipos de datos
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619995"
---
# <a name="windows-event-log-data-types"></a>Windows Tipos de datos del registro de eventos

Windows El registro de eventos define los siguientes tipos de datos:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**CONTROLADOR \_ DE EVT**
</dt> <dd>

Identificador de un objeto Windows registro de eventos.

</dd> <dt>

**IDENTIFICADOR \_ DE PEVT**
</dt> <dd>

Puntero al identificador de un objeto Windows de eventos.

</dd> <dt>

**IDENTIFICADOR DE PROPIEDAD \_ DE \_ MATRIZ \_ DE OBJETOS \_ EVT**
</dt> <dd>

Identificador de una matriz de objetos Windows de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>WinEvt.h</dt> </dl> |



 

 






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
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241526"
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

Identificador de un objeto Windows de eventos.

</dd> <dt>

**IDENTIFICADOR DE \_ PEVT**
</dt> <dd>

Puntero al identificador de un objeto Windows de eventos.

</dd> <dt>

**IDENTIFICADOR DE PROPIEDAD \_ DE \_ MATRIZ \_ DE OBJETOS EVT \_**
</dt> <dd>

Identificador de una matriz de objetos Windows de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WinEvt.h</dt> </dl> |



 

 






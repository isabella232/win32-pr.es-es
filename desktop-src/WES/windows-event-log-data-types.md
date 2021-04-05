---
title: Tipos de datos del registro de eventos de Windows (WinEvt. h)
description: El registro de eventos de Windows define los siguientes tipos de datos
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802191"
---
# <a name="windows-event-log-data-types"></a>Tipos de datos del registro de eventos de Windows

El registro de eventos de Windows define los siguientes tipos de datos:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**identificador de EVT \_**
</dt> <dd>

Identificador de un objeto de registro de eventos de Windows.

</dd> <dt>

**identificador de PEVT \_**
</dt> <dd>

Puntero al identificador de un objeto de registro de eventos de Windows.

</dd> <dt>

**identificador de la propiedad de matriz de \_ objetos evt \_ \_ \_**
</dt> <dd>

Identificador de una matriz de objetos de registro de eventos de Windows.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 






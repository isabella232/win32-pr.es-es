---
description: Esta clase es la clase de tipo de evento para eventos de mensaje de recepción de ALPC. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255074"
---
# <a name="alpc_receive_message-class"></a>Alpc \_ Receive \_ Message (clase)

Esta clase es la clase de tipo de evento para eventos de mensaje de recepción de ALPC.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Members

La **clase ALPC \_ Receive \_ Message** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ALPC \_ Receive \_ Message** tiene estas propiedades.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del mensaje.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





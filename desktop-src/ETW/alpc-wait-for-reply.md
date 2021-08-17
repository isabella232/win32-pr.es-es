---
description: Esta clase es la clase de tipo de evento para esperar eventos de respuesta de ALPC. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: ALPC_Wait_For_Reply clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b2f2e867e3e95e8ba0916ad288363db7ad8b6a7753f956df5415529d8ec5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070315"
---
# <a name="alpc_wait_for_reply-class"></a>ALPC \_ Wait For Reply \_ \_ (Clase)

Esta clase es la clase de tipo de evento para esperar eventos de respuesta de ALPC.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Miembros

La **clase WAIT For Reply \_ \_ \_ de ALPC** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Wait For Reply \_ \_ \_ de ALPC** tiene estas propiedades.

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



 

 





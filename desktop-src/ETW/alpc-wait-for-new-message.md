---
description: Esta clase es la clase de tipo de evento para que ALPC espere nuevos eventos de mensaje. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67b3e52e59345eea95db7485e0764f31f88669241159ffc857d46cf230a5e8b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901555"
---
# <a name="alpc_wait_for_new_message-class"></a>ALPC \_ Wait For New Message \_ \_ \_ (Clase)

Esta clase es la clase de tipo de evento para que ALPC espere nuevos eventos de mensaje.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a>Miembros

La **clase ALPC \_ Wait For \_ New \_ \_ Message** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ALPC \_ Wait For \_ New \_ \_ Message** tiene estas propiedades.

<dl> <dt>

**IsServerPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el puerto es un puerto de servidor.

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que contiene el nombre del puerto en el que ESTÁ ESPERANDO ALPC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





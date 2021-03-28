---
description: Esta clase es la clase de tipo de evento para la espera ALPC para los nuevos eventos de mensaje. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message (clase)
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
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984527"
---
# <a name="alpc_wait_for_new_message-class"></a>ALPC- \_ esperar \_ para la \_ nueva clase de \_ mensaje

Esta clase es la clase de tipo de evento para la espera ALPC para los nuevos eventos de mensaje.

La siguiente sintaxis se simplifica desde el código MOF.

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

La **nueva clase de \_ mensaje ALPC wait \_ for \_ New \_ Message** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ nueva clase \_ de mensaje ALPC wait for \_ New \_ Message** tiene estas propiedades.

<dl> <dt>

**IsServerPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
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

Cadena que contiene el nombre del puerto en el que se está esperando ALPC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





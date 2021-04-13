---
description: La estructura NETWORKSTATUS describe el estado actual del NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Estructura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546995"
---
# <a name="networkstatus-structure"></a>Estructura NETWORKSTATUS

La estructura **NETWORKSTATUS** describe el estado actual del NPP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**State**
</dt> <dd>

Indica el estado actual del NPP.



| Value                                                                                                                                                                                                          | Significado                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS \_ estado \_ void**</dt> </dl>                | NPP no está conectado o está conectado y la captura no se ha iniciado.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**\_captura de estado de NETWORKSTATUS \_**</dt> </dl> | NPP está capturando datos.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**Estado de NETWORKSTATUS en \_ \_ pausa**</dt> </dl>          | El NPP se ha pausado durante la captura de datos.<br/>                                     |



 

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas que describen el estado actual del NPP.



| Value                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**\_desencadenador de marcas de NETWORKSTATUS \_ \_ pendiente**</dt> </dl> | Hay un desencadenador pendiente para el NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al utilizar esta estructura, debe asignar la memoria de la estructura antes de que se pueda utilizar y liberar la memoria cuando la estructura ya no se necesite.

En la lista vea también en la parte inferior de este tema se enumeran todos los métodos que utilizan esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC:: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP:: QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC:: QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStas:: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 





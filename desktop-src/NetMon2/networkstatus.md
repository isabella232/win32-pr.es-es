---
description: La estructura NETWORKSTATUS describe el estado actual del NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Estructura NETWORKSTATUS (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245294"
---
# <a name="networkstatus-structure"></a>Estructura NETWORKSTATUS

La **estructura NETWORKSTATUS** describe el estado actual del NPP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**State**
</dt> <dd>

Indica el estado actual del NPP.



| Value                                                                                                                                                                                                          | Significado                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS \_ STATE \_ VOID**</dt> </dl>                | El NPP no está conectado o está conectado y no se inicia la captura.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**CAPTURA DE ESTADO \_ NETWORKSTATUS \_**</dt> </dl> | El NPP captura datos.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**ESTADO NETWORKSTATUS \_ \_ EN PAUSA**</dt> </dl>          | El NPP se ha detenido al capturar datos.<br/>                                     |



 

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas que describen el estado actual del NPP.



| Value                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**NETWORKSTATUS \_ FLAGS \_ TRIGGER \_ PENDING**</dt> </dl> | Hay un desencadenador pendiente para el NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al usar esta estructura, debe asignar la memoria para la estructura antes de que se pueda usar y liberar la memoria cuando la estructura ya no sea necesaria.

En la lista Ver también de la parte inferior de este tema se enumeran todos los métodos que usan esta estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP::QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC::QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats::QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 





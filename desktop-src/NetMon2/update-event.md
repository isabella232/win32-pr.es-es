---
description: Los eventos de actualización de la \_ estructura de eventos. Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento mediante NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Estructura de UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677670"
---
# <a name="update_event-structure"></a>ACTUALIZAR la \_ estructura de eventos

Los eventos de actualización de la estructura de **\_ eventos** . Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento mediante NPP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Evento**
</dt> <dd>

Evento real que se está registrando.

</dd> <dt>

**Acción**
</dt> <dd>

Acción realizada.

</dd> <dt>

**Estado**
</dt> <dd>

Indicación del estado de la red.

</dd> <dt>

**Valor**
</dt> <dd>

Variable de contador auxiliar.

</dd> <dt>

**Indicaciones**
</dt> <dd>

Los eventos marcados, en microsegundos.

</dd> <dt>

**lpUserContext**
</dt> <dd>

Contexto de usuario proporcionado por la aplicación.

</dd> <dt>

**lpReserved**
</dt> <dd>

Controlador o uso de NAL.

</dd> <dt>

**FramesDropped**
</dt> <dd>

Fotogramas RTF quitados en el búfer especificado.

</dd> <dt>

**Reserved**
</dt> <dd>

No se devuelve ningún dato con esta opción de modificador.

</dd> <dt>

**lpFrameTable**
</dt> <dd>

Solo RTF.

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

Para las retransmisiones.

</dd> <dt>

**SecurityResponse**
</dt> <dd>

Respuesta del monitor de seguridad remota.

</dd> <dt>

**lpFinalStats**
</dt> <dd>

Esto solo se rellena en paradas no relacionadas con la seguridad (por ejemplo, desencadenadores).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los usuarios de C++ deben tener en cuenta que la declaración de esta devolución de llamada debe estar en la parte pública del archivo de encabezado:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

La implementación debe estar en la sección protegida del archivo. cpp:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





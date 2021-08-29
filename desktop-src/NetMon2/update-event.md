---
description: La estructura UPDATE \_ EVENT actualiza los eventos. Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento por parte del NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: UPDATE_EVENT estructura (Netmon.h)
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
ms.openlocfilehash: 51fda96f988a6420acd772182c3259a3de09a10b8a9c2ac8678025e26f5fa15a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962815"
---
# <a name="update_event-structure"></a>UPDATE \_ EVENT (estructura)

La **estructura UPDATE \_ EVENT** actualiza los eventos. Esta estructura se pasa a la aplicación que realiza la llamada a través del procedimiento de devolución de llamada de estado de evento por parte del NPP.

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

Indicación de estado de red.

</dd> <dt>

**Valor**
</dt> <dd>

Variable de contador auxiliar.

</dd> <dt>

**Timestamp**
</dt> <dd>

Eventos marcados, en microsegundos.

</dd> <dt>

**lpUserContext**
</dt> <dd>

Contexto de usuario especificado por la aplicación.

</dd> <dt>

**lpReserved**
</dt> <dd>

Uso del controlador o NAL.

</dd> <dt>

**FramesDropped**
</dt> <dd>

Fotogramas RTF descartados en el búfer especificado.

</dd> <dt>

**Reserved**
</dt> <dd>

No se recupera ningún dato con esta opción de modificador.

</dd> <dt>

**lpFrameTable**
</dt> <dd>

Solo RTF.

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

Para las transmisiónes.

</dd> <dt>

**SecurityResponse**
</dt> <dd>

Respuesta del monitor de seguridad remoto.

</dd> <dt>

**lpFinalStats**
</dt> <dd>

Esto solo se rellena en las paradas no relacionadas con la seguridad (por ejemplo, desencadenadores).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los usuarios de C++ deben tener en cuenta que la declaración de esta devolución de llamada debe estar en la parte pública del archivo de encabezado:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

La implementación debe estar en la sección protegida del archivo .cpp:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





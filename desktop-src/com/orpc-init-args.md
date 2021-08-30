---
title: ORPC_INIT_ARGS estructura
description: La estructura ORPC INIT ARGS contiene información que se usa para inicializar \_ \_ la depuración remota mediante la interfaz IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- ORPC_INIT_ARGS com de estructura
- LPORPC_INIT_ARGS de estructura de datos COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49bca85d44f13f304ad566b2d0ab39cb800abd36af4c922c0ae5619bb2703009
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992315"
---
# <a name="orpc_init_args-structure"></a>Estructura ARGS de ORPC \_ INIT \_

La **estructura ORPC \_ INIT \_ ARGS** contiene información que se usa para inicializar la depuración remota mediante la [**interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**lpIntfOrpcDebug**
</dt> <dd>

Puntero a la [**interfaz IOrpcDebugNotify**](iorpcdebugnotify.md) para que la usen los depuradores en proceso. Si el depurador no está en proceso o es un sistema Macintosh, este campo debe ser **NULL.**

</dd> <dt>

**pvPSN**
</dt> <dd>

Puntero al número de serie del proceso Macintosh del proceso del depurado. Si el depurado no es un sistema Macintosh, este campo debe ser **NULL.**

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reservado. Debe ser 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado. Debe ser 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**BÚFER \_ DE DBG DE ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 






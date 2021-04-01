---
title: Estructura de ORPC_INIT_ARGS
description: La \_ estructura ORPC init \_ args contiene información que se usa para inicializar la depuración remota mediante la interfaz IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- Estructura de ORPC_INIT_ARGS COM
- LPORPC_INIT_ARGS puntero de estructura COM
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
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150081"
---
# <a name="orpc_init_args-structure"></a>ORPC \_ init \_ args (estructura)

La estructura **ORPC \_ init \_ args** contiene información que se usa para inicializar la depuración remota mediante la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

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

Un puntero a la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) para su uso por los depuradores en proceso. Si el depurador no está en proceso o es un sistema Macintosh, este campo debe ser **null**.

</dd> <dt>

**pvPSN**
</dt> <dd>

Puntero al número de serie del proceso de Macintosh del proceso del depurador. Si el código depurado no es un sistema Macintosh, este campo debe ser **null**.

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

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_búfer ORPC dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 






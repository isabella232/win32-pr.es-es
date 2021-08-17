---
description: Contiene el contexto de ejecución del controlador de impresora que llama a GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: PRINT_EXECUTION_DATA estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e67b43089c275baf59295f15e84d9bf38d1a3a5ff6e2adfaf2d270b02e2ad967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447145"
---
# <a name="print_execution_data-structure"></a>Estructura PRINT \_ EXECUTION \_ DATA

Contiene el contexto de ejecución del controlador de impresora que llama a [**GetPrintExecutionData**](getprintexecutiondata.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**contextoo**
</dt> <dd>

Valor [**PRINT EXECUTION CONTEXT \_ \_ que**](print-execution-context.md) representa el contexto de ejecución actual del controlador de impresora.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Si el valor de **context** es **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64**, **clientAppPID** identifica la aplicación cliente en cuyo nombre el proceso de splwow64.exe cargó el controlador de impresora. Si el valor de **context no** es PRINT EXECUTION **CONTEXT \_ \_ \_ WOW64,** **clientAppPID** es cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**CONTEXTO DE \_ EJECUCIÓN DE \_ IMPRESIÓN**](print-execution-context.md)
</dt> </dl>

 

 





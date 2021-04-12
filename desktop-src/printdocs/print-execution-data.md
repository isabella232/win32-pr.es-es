---
description: Contiene el contexto de ejecución del controlador de impresora que llama a GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Estructura de PRINT_EXECUTION_DATA (winspool. h)
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
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278197"
---
# <a name="print_execution_data-structure"></a>Estructura de datos de \_ ejecución de impresión \_

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

Valor [**del \_ \_ contexto de ejecución de impresión**](print-execution-context.md) que representa el contexto de ejecución actual del controlador de impresora.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Si el valor de **Context** es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, **clientAppPID** identifica la aplicación cliente en cuyo nombre el proceso de splwow64.exe cargó el controlador de impresora. Si el valor de **Context** no es el **contexto de ejecución de impresión \_ \_ \_ WOW64**, **clientAppPID** es cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**\_contexto de ejecución de impresión \_**](print-execution-context.md)
</dt> </dl>

 

 





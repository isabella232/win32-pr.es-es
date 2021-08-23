---
description: Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.
title: Función DlpInitializeEnforcementMode (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: be1e71782b258745e31d286a69ae76d3ecbcafb74c170f3b5baf5eb19bcc4b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610445"
---
# <a name="dlpinitializeenforcementmode-function"></a>Función DlpInitializeEnforcementMode

Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Recuento* \[ En\]
</dt> <dd>

DWORD **que** especifica el número de operaciones incluidas en la *matriz OperationEnforcement.*

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[ En\]
</dt> <dd>

Matriz de estructuras [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) que especifican el nivel de cumplimiento de una operación DLP de punto de conexión.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve un HRESULT que incluye, entre otros, los valores siguientes.

| HRESULT | Descripción |
|---------|-------------|
| S_OK | La función se completó correctamente |
| E_INVALIDARG | Uno o varios de los parámetros de función no son válidos. |
| E_OUTOFMEMORY | Error de asignación de memoria para la operación. |



## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |
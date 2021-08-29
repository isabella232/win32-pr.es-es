---
title: Función FreeSystemHealthAgentState (NapUtil.h)
description: Libera una estructura de datos SystemHealthAgentState.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- Función NAP de FreeSystemHealthAgentState
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5161b24f983936b2eb380f1863489ea6c5c927d9b18a278e5942e162f156c6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891655"
---
# <a name="freesystemhealthagentstate-function"></a>Función FreeSystemHealthAgentState

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función FreeSystemHealthAgentState** libera una [**estructura de datos SystemHealthAgentState.**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*state* \[ En\]
</dt> <dd>

Puntero a la [**estructura de datos SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) que se liberará.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   **El** autor de la llamada asigna y libera los parámetros de .
-   **El** destinatario asigna los parámetros out y el autor de la llamada lo libera **mediante CoTaskMem**.
-   **El autor de** la llamada asigna los parámetros de entrada y salida, los libera y reasigna el destinatario y, en última instancia, los libera el autor de la llamada, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






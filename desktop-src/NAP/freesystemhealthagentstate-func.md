---
title: Función FreeSystemHealthAgentState (NapUtil. h)
description: Libera una estructura de datos SystemHealthAgentState.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- FreeSystemHealthAgentState función NAP
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
ms.openlocfilehash: 6ce59135de1c8f47d84a07f01dbb5f2bbe697f9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150104"
---
# <a name="freesystemhealthagentstate-function"></a>FreeSystemHealthAgentState función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **FreeSystemHealthAgentState** libera una estructura de datos [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) .

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ de de\]
</dt> <dd>

Puntero a la estructura de datos [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) que se va a liberar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   El autor de la llamada asigna y libera los parámetros **in** .
-   El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.
-   Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






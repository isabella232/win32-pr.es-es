---
title: Función FreeIsolationInfo (NapUtil. h)
description: Libera una estructura de datos IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- FreeIsolationInfo función NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676889"
---
# <a name="freeisolationinfo-function"></a>FreeIsolationInfo función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **FreeIsolationInfo** libera una estructura de datos [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) .

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ de\]
</dt> <dd>

Puntero a la estructura de datos [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que se va a liberar.

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



 

 






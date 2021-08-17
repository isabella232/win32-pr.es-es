---
title: Función FreeIsolationInfo (NapUtil.h)
description: Libera una estructura de datos IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- Función NAP de FreeIsolationInfo
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
ms.openlocfilehash: 031fd49bbdda7c0b36481776ba3c9dca8ea6d1c236b0010ada319b9a51f989df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940652"
---
# <a name="freeisolationinfo-function"></a>Función FreeIsolationInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función FreeIsolationInfo** libera una estructura [**de datos IsolationInfo.**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isolationInfo* \[ En\]
</dt> <dd>

Puntero a la estructura [**de datos IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que se liberará.

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



 

 






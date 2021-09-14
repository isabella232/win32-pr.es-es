---
description: Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Función NtGetCurrentProcessorNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375019"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Función NtGetCurrentProcessorNumber

\[**NtGetCurrentProcessorNumber** puede modificarse o no estar disponible en versiones futuras de Windows. Las aplicaciones deben usar [**la función GetCurrentProcessorNumber en**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) su lugar.\]

Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.

## <a name="syntax"></a>Sintaxis


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de procesador actual.

## <a name="remarks"></a>Observaciones

Esta función se usa para proporcionar información para calcular el rendimiento del proceso.

Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Varios procesadores](multiple-processors.md)
</dt> <dt>

[Funciones de proceso y subproceso](process-and-thread-functions.md)
</dt> <dt>

[Procesos](child-processes.md)
</dt> </dl>

 

 

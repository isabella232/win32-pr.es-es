---
description: Recupera el número del procesador en el que se estaba ejecutando el subproceso actual durante la llamada a esta función.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber función)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681001"
---
# <a name="ntgetcurrentprocessornumber-function"></a>NtGetCurrentProcessorNumber función)

\[**NtGetCurrentProcessorNumber** puede modificarse o no estar disponible en versiones futuras de Windows. En su lugar, las aplicaciones deben usar la función [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]

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

Esta función se usa para proporcionar información para calcular el rendimiento de los procesos.

Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

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

 

 

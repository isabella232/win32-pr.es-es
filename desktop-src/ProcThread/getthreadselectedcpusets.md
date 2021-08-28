---
description: Devuelve la asignación explícita del conjunto de CPU del subproceso especificado, si se estableció alguna asignación mediante la API SetThreadSelectedCpuSets. Si no se establece ninguna asignación explícita, RequiredIdCount se establece en 0 y la función devuelve TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Función GetThreadSelectedCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978785"
---
# <a name="getthreadselectedcpusets-function"></a>Función GetThreadSelectedCpuSets

Devuelve la asignación explícita del conjunto de CPU del subproceso especificado, si se estableció alguna asignación mediante la API [**SetThreadSelectedCpuSets.**](setthreadselectedcpusets.md) Si no se establece ninguna asignación explícita, **RequiredIdCount** se establece en 0 y la función devuelve TRUE.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Subproceso* \[ En\]
</dt> <dd>

Especifica el subproceso para el que se consultan los conjuntos de CPU seleccionados. Este identificador debe tener el derecho de acceso THREAD \_ QUERY \_ LIMITED \_ INFORMATION. El valor devuelto [**por GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) también se puede especificar aquí.

</dd> <dt>

*CpuSetIds* \[ out, opcional\]
</dt> <dd>

Especifica un búfer opcional para recuperar la lista de identificadores de conjunto de CPU.

</dd> <dt>

*CpuSetIdCount* \[ En\]
</dt> <dd>

Especifica la capacidad del búfer especificado en **CpuSetIds**. Si el búfer es NULL, debe ser 0.

</dd> <dt>

*RequiredIdCount* \[ out\]
</dt> <dd>

Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU seleccionados para subprocesos. Si la devolución es correcta, especifica el número de identificaciónes rellenadas en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta API devuelve TRUE si se ejecuta correctamente. Si el búfer no es lo suficientemente grande, el **valor de GetLastError** es ERROR \_ INSUFFICIENT \_ BUFFER. Esta API no puede producir un error cuando se pasan parámetros válidos y el búfer de retorno es lo suficientemente grande.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


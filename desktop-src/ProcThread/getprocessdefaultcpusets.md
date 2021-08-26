---
description: Recupera la lista de conjuntos de CPU del conjunto predeterminado de procesos establecido por SetProcessDefaultCpuSets. Si no se establece ningún conjunto de CPU predeterminado para un proceso determinado, RequiredIdCount se establece en 0 y la función se realiza correctamente.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Función GetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3c5d71e4811411756719177647fda8dd76224f756629ad01794720d291565b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886705"
---
# <a name="getprocessdefaultcpusets-function"></a>Función GetProcessDefaultCpuSets

Recupera la lista de conjuntos de CPU del conjunto predeterminado de procesos establecido por [**SetProcessDefaultCpuSets.**](setprocessdefaultcpusets.md) Si no se establece ningún conjunto de CPU predeterminado para un proceso determinado, **RequiredIdCount** se establece en 0 y la función se realiza correctamente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Proceso* \[ En\]
</dt> <dd>

Especifica un identificador de proceso para el proceso que se debe consultar. Este identificador debe tener el derecho de \_ acceso PROCESS QUERY LIMITED \_ \_ INFORMATION. El valor devuelto [**por GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

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

Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU predeterminados del proceso. Si la devolución es correcta, especifica el número de identificaciónes rellenadas en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta API devuelve TRUE si se ejecuta correctamente. Si el búfer no es lo suficientemente grande, la API devuelve FALSE y el **valor getLastError** es ERROR \_ INSUFFICIENT \_ BUFFER. Esta API no puede producir un error cuando se pasan parámetros válidos y el búfer devuelto es lo suficientemente grande.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


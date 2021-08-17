---
description: Establece la asignación predeterminada de conjuntos de CPU para subprocesos en el proceso especificado. Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante SetThreadSelectedCpuSets, heredarán automáticamente los conjuntos especificados por SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Función SetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793182"
---
# <a name="setprocessdefaultcpusets-function"></a>Función SetProcessDefaultCpuSets

Establece la asignación predeterminada de conjuntos de CPU para subprocesos en el proceso especificado. Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante [**SetThreadSelectedCpuSets,**](setthreadselectedcpusets.md)heredarán automáticamente los conjuntos especificados por **SetProcessDefaultCpuSets.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Proceso* \[ En\]
</dt> <dd>

Especifica el proceso para el que se establecen los conjuntos de CPU predeterminados. Este identificador debe tener el derecho de \_ acceso PROCESS SET LIMITED \_ \_ INFORMATION. El valor devuelto [**por GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

</dd> <dt>

*CpuSetIds* \[ in, opcional\]
</dt> <dd>

Especifica la lista de los ID de conjunto de CPU que se establecerán como el conjunto de CPU predeterminado del proceso. Si es NULL, **SetProcessDefaultCpuSets** borra cualquier asignación.

</dd> <dt>

*CpuSetIdCound* \[ En\]
</dt> <dd>

Especifica el número de id. de la lista pasada en el **argumento CpuSetIds.** Si ese valor es NULL, debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no puede producir un error cuando se pasan parámetros válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 

---
description: Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se establece una.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Función SetThreadSelectedCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d627c3ae0499cf19ba533c30d1a3fabb05c2dbf5782d99b2f716579f50125b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031735"
---
# <a name="setthreadselectedcpusets-function"></a>Función SetThreadSelectedCpuSets

Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se establece una.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Subproceso* \[ En\]
</dt> <dd>

Especifica el subproceso en el que se va a establecer la asignación del conjunto de CPU. Este identificador debe tener el derecho de \_ acceso THREAD SET LIMITED \_ \_ INFORMATION. También se puede usar el valor devuelto por [**GetCurrentThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)

</dd> <dt>

*CpuSetIds* \[ En\]
</dt> <dd>

Especifica la lista de los ID de conjunto de CPU que se establecerán como el conjunto de CPU seleccionado para subprocesos. Si es NULL, la API borra cualquier asignación y vuelve a procesar la asignación predeterminada si se establece una.

</dd> <dt>

*CpuSetIdCount* \[ En\]
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



 

 

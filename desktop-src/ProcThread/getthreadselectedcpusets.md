---
description: Devuelve la asignación de conjunto de CPU explícita del subproceso especificado, si se ha establecido una asignación mediante la API de SetThreadSelectedCpuSets. Si no se establece ninguna asignación explícita, RequiredIdCount se establece en 0 y la función devuelve TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Función GetThreadSelectedCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082650"
---
# <a name="getthreadselectedcpusets-function"></a>GetThreadSelectedCpuSets función)

Devuelve la asignación de conjunto de CPU explícita del subproceso especificado, si se ha establecido una asignación mediante la API de [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) . Si no se establece ninguna asignación explícita, **RequiredIdCount** se establece en 0 y la función devuelve true.

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

*Subproceso* \[ de\]
</dt> <dd>

Especifica el subproceso para el que se van a consultar los conjuntos de CPU seleccionados. Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de subproceso \_ . El valor devuelto por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) también se puede especificar aquí.

</dd> <dt>

*CpuSetIds* \[ out, opcional\]
</dt> <dd>

Especifica un búfer opcional para recuperar la lista de identificadores de conjuntos de CPU.

</dd> <dt>

*CpuSetIdCount* \[ de\]
</dt> <dd>

Especifica la capacidad del búfer especificado en **CpuSetIds**. Si el búfer es NULL, debe ser 0.

</dd> <dt>

*RequiredIdCount* \[ enuncia\]
</dt> <dd>

Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU seleccionados para el subproceso. Especifica el número de identificadores rellenados en el búfer si la devolución es correcta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta API devuelve TRUE en caso de éxito. Si el búfer no es suficientemente grande, el valor de **GetLastError** es error de \_ búfer insuficiente \_ . No se puede producir un error en esta API cuando se pasan parámetros válidos y el búfer de retorno es suficientemente grande.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


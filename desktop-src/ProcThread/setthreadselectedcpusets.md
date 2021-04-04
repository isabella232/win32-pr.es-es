---
description: Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se ha establecido uno.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Función SetThreadSelectedCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909677"
---
# <a name="setthreadselectedcpusets-function"></a>SetThreadSelectedCpuSets función)

Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se ha establecido uno.

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

*Subproceso* \[ de\]
</dt> <dd>

Especifica el subproceso en el que se va a establecer la asignación de conjunto de CPU. Este identificador debe tener el \_ derecho de \_ acceso de información limitada del subproceso \_ . También se puede usar el valor devuelto por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) .

</dd> <dt>

*CpuSetIds* \[ de\]
</dt> <dd>

Especifica la lista de identificadores de conjuntos de CPU que se establecerá como conjunto de CPU seleccionado de subproceso. Si es NULL, la API borra cualquier asignación y revierte para procesar la asignación predeterminada si se establece una.

</dd> <dt>

*CpuSetIdCount* \[ de\]
</dt> <dd>

Especifica el número de identificadores de la lista que se han pasado en el argumento **CpuSetIds** . Si ese valor es NULL, debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se puede producir un error en esta función cuando se pasan parámetros válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 

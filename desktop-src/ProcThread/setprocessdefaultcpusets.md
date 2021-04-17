---
description: Establece la asignación de conjuntos de CPU predeterminada para los subprocesos en el proceso especificado. Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante SetThreadSelectedCpuSets, heredarán automáticamente los conjuntos especificados por SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Función SetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677831"
---
# <a name="setprocessdefaultcpusets-function"></a>SetProcessDefaultCpuSets función)

Establece la asignación de conjuntos de CPU predeterminada para los subprocesos en el proceso especificado. Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), heredarán automáticamente los conjuntos especificados por **SetProcessDefaultCpuSets** .

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

*Proceso* \[ de de\]
</dt> <dd>

Especifica el proceso para el que se van a establecer los conjuntos de CPU predeterminados. Este identificador debe tener el \_ derecho de \_ acceso de información limitada del proceso \_ . El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

</dd> <dt>

*CpuSetIds* \[ en, opcional\]
</dt> <dd>

Especifica la lista de identificadores de conjuntos de CPU que se establecerá como el conjunto de CPU predeterminado del proceso. Si es NULL, el **SetProcessDefaultCpuSets** borra cualquier asignación.

</dd> <dt>

*CpuSetIdCound* \[ de\]
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



 

 

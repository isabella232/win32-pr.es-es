---
description: Recupera la lista de conjuntos de CPU en el conjunto predeterminado de procesos establecido por SetProcessDefaultCpuSets. Si no se establecen conjuntos de CPU predeterminados para un proceso determinado, el valor de RequiredIdCount se establece en 0 y la función se ejecuta correctamente.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Función GetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677861"
---
# <a name="getprocessdefaultcpusets-function"></a>GetProcessDefaultCpuSets función)

Recupera la lista de conjuntos de CPU en el conjunto predeterminado de procesos establecido por [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md). Si no se establecen conjuntos de CPU predeterminados para un proceso determinado, el valor de **RequiredIdCount** se establece en 0 y la función se ejecuta correctamente.

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

*Proceso* \[ de de\]
</dt> <dd>

Especifica un identificador de proceso para el proceso que se va a consultar. Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de proceso \_ . El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

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

Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU predeterminados del proceso. Especifica el número de identificadores rellenados en el búfer si la devolución es correcta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta API devuelve TRUE en caso de éxito. Si el búfer no es suficientemente grande, la API devuelve FALSE y el valor de **GetLastError** es error de \_ búfer insuficiente \_ . No se puede producir un error en esta API cuando se pasan parámetros válidos y el búfer de retorno es suficientemente grande.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


---
description: Permite a una aplicación consultar los conjuntos de CPU disponibles en el sistema y su estado actual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Función GetSystemCpuSetInformation (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 011a809c78f2e94e6d16bbe5deb716ee7e97db356765bb771709048d3b00d05a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995375"
---
# <a name="getsystemcpusetinformation-function"></a>Función GetSystemCpuSetInformation

Permite a una aplicación consultar los conjuntos de CPU disponibles en el sistema y su estado actual.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Información* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura [**SYSTEM \_ CPU SET \_ \_ INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) que recibe los datos del conjunto de CPU. Pase NULL con una longitud de búfer de 0 para determinar el tamaño de búfer necesario.

</dd> <dt>

*BufferLength* \[ En\]
</dt> <dd>

Longitud, en bytes, del búfer de salida pasado como argumento Information.

</dd> <dt>

*ReturnedLength* \[ out\]
</dt> <dd>

Longitud, en bytes, de los datos válidos en el búfer de salida si el búfer es lo suficientemente grande o el tamaño necesario del búfer de salida. Si no existe ningún conjunto de CPU, este valor será 0.

</dd> <dt>

*Proceso* \[ en, opcional\]
</dt> <dd>

Identificador opcional de un proceso. Este proceso se usa para determinar el valor de la **marca AllocatedToTargetProcess** en la estructura SYSTEM \_ CPU SET \_ \_ INFORMATION. Si se asigna un conjunto de CPU al proceso especificado, se establece la marca . De lo contrario, está claro. Este identificador debe tener el derecho de \_ acceso PROCESS QUERY LIMITED \_ \_ INFORMATION. El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

</dd> <dt>

*Marcas* 
</dt> <dd>

Reservado, debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la API se realiza correctamente, devuelve TRUE. Si se produce un error, el motivo del error está disponible a través **de GetLastError**. Si el búfer de información era NULL o no lo suficientemente grande, se devuelve el código de error ERROR \_ INSUFFICIENT \_ BUFFER. Esta API no puede producir un error cuando se pasan parámetros válidos y un búfer lo suficientemente grande como para contener todos los datos devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


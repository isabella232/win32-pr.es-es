---
description: Permite a una aplicación consultar los conjuntos de CPU disponibles en el sistema y su estado actual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Función GetSystemCpuSetInformation (Processthreadapi. h)
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
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276823"
---
# <a name="getsystemcpusetinformation-function"></a>GetSystemCpuSetInformation función)

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

*Información* \[ de out, opcional\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ \_ información de conjunto de CPU del sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) que recibe los datos del conjunto de CPU. Pase NULL con una longitud de búfer de 0 para determinar el tamaño de búfer necesario.

</dd> <dt>

*BufferLength* \[ de\]
</dt> <dd>

La longitud, en bytes, del búfer de salida pasada como argumento de la información.

</dd> <dt>

*ReturnedLength* \[ enuncia\]
</dt> <dd>

La longitud, en bytes, de los datos válidos en el búfer de salida si el búfer es suficientemente grande o el tamaño necesario del búfer de salida. Si no existe ningún conjunto de CPU, este valor será 0.

</dd> <dt>

*Proceso* \[ de en, opcional\]
</dt> <dd>

Un identificador opcional para un proceso. Este proceso se usa para determinar el valor de la marca **AllocatedToTargetProcess** en la estructura de información de conjunto de CPU del sistema \_ \_ \_ . Si se asigna un conjunto de CPU al proceso especificado, se establece la marca. De lo contrario, está claro. Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de proceso \_ . El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.

</dd> <dt>

*Marcas* 
</dt> <dd>

Reserved, debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la API se ejecuta correctamente, devuelve TRUE. Si se produce un error, la razón del error está disponible a través de **GetLastError**. Si el búfer de información era NULL o no es lo suficientemente grande, se devuelve el búfer de ERROR de código \_ insuficiente \_ . No se puede producir un error en esta API cuando se pasan parámetros válidos y un búfer lo suficientemente grande como para contener todos los datos devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 


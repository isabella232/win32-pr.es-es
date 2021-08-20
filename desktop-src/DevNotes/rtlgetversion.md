---
description: Obtiene información de versión sobre el sistema operativo que se está ejecutando actualmente.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Función RtlGetVersion (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161687"
---
# <a name="rtlgetversion-function"></a>Función RtlGetVersion

Obtiene información de versión sobre el sistema operativo que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpVersionInformation* \[ out\]
</dt> <dd>

Puntero a una estructura [**\_ RTL OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una estructura [**\_ RTL OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) que contiene la información de versión sobre el sistema operativo que se está ejecutando actualmente. Un llamador especifica qué estructura de entrada se usa estableciendo el **miembro dwOSVersionInfoSize** de la estructura en el tamaño en bytes de la estructura que se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve STATUS \_ SUCCESS.

## <a name="remarks"></a>Comentarios

**RtlGetVersion es** el equivalente de la [**función GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) en Windows SDK. Vea el ejemplo en el SDK Windows que muestra cómo obtener la versión del sistema.

Cuando se **usa RtlGetVersion** para determinar si se está ejecutando una versión determinada del sistema operativo, un autor de la llamada debe comprobar los números de versión que sean mayores o iguales que el número de versión necesario. Esto garantiza que una prueba de versión se realiza correctamente para versiones posteriores de Windows.

Dado que las características del sistema operativo se pueden agregar en un archivo DLL redistribuible, comprobar solo los números de versión principal y secundaria no es la manera más confiable de comprobar la presencia de una característica específica del sistema. Un controlador debe usar [**RtlVerifyVersionInfo para**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) comprobar la presencia de una característica específica del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Header<br/>                   | <dl> <dt>Ntddk.h (incluir Ntddk.h)</dt> </dl>                                                     |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 

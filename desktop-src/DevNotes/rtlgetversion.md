---
description: Obtiene la información de versión del sistema operativo que se está ejecutando actualmente.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Función RtlGetVersion (Ntddk. h)
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
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152964"
---
# <a name="rtlgetversion-function"></a>RtlGetVersion función)

Obtiene la información de versión del sistema operativo que se está ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpVersionInformation* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una [**estructura \_ RTL OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) que contiene la información de versión del sistema operativo que se está ejecutando actualmente. Un llamador especifica la estructura de entrada que se utiliza estableciendo el miembro **dwOSVersionInfoSize** de la estructura en el tamaño en bytes de la estructura que se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado \_ correcto.

## <a name="remarks"></a>Observaciones

**RtlGetVersion** es el equivalente de la función [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) en el Windows SDK. Vea el ejemplo del Windows SDK que muestra cómo obtener la versión del sistema.

Al usar **RtlGetVersion** para determinar si se está ejecutando una versión determinada del sistema operativo, el autor de la llamada debe comprobar si los números de versión son mayores o iguales que el número de versión requerido. Esto garantiza que una prueba de versión se realiza correctamente para las versiones posteriores de Windows.

Dado que las características del sistema operativo se pueden agregar en un archivo DLL redistribuible, comprobar solo los números de versión principal y secundaria no es la forma más confiable de comprobar la presencia de una característica específica del sistema. Un controlador debe usar [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) para comprobar la presencia de una característica específica del sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Plataforma de destino<br/>          | <dl> <dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Encabezado<br/>                   | <dl> <dt>Ntddk. h (incluye Ntddk. h)</dt> </dl>                                                     |
| Biblioteca<br/>                  | <dl> <dt>Ntdll. lib; </dt> <dt>NtosKrnl. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 

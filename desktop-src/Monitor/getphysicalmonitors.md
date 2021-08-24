---
title: Función GetPhysicalMonitors
description: Obtiene los monitores físicos asociados a un dispositivo de visualización.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configuración del monitor de la función GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94cef0352aae75f95b1ff7ee9e65937f82c7b598a19cdce768028173dc97331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146158"
---
# <a name="getphysicalmonitors-function"></a>Función GetPhysicalMonitors

> [!IMPORTANT]
> La API de configuración de monitor usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene los monitores físicos asociados a un dispositivo de visualización.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrDeviceName* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ STRING UNICODE**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función [**GetMonitorInfo.**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*dwPhysicalMonitorArraySize* \[ En\]
</dt> <dd>

Número de elementos de la matriz *pdwNumPhysicalMonitorHandlesInArray.* Para obtener el tamaño necesario de la matriz, llame a [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[ out\]
</dt> <dd>

Recibe el número de elementos que la función copia en la *matriz phPhysicalMonitorArray.*

</dd> <dt>

*phPhysicalMonitorArray* \[ out\]
</dt> <dd>

Matriz que recibe identificadores para los monitores físicos. Cada identificador debe liberarse mediante una llamada [**a DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Supervisar funciones de configuración](monitor-configuration-functions.md)
</dt> </dl>

 


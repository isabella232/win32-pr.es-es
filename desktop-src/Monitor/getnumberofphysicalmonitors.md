---
title: GetNumberOfPhysicalMonitors función)
description: Obtiene el número de monitores físicos asociados a un dispositivo de pantalla.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Configuración del monitor de función GetNumberOfPhysicalMonitors
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905220"
---
# <a name="getnumberofphysicalmonitors-function"></a>GetNumberOfPhysicalMonitors función)

> [!IMPORTANT]
> La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene el número de monitores físicos asociados a un dispositivo de pantalla.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pstrDeviceName* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ cadena Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*pdwNumberOfPhysicalMonitors* \[ enuncia\]
</dt> <dd>

Recibe el número de monitores físicos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**. De lo contrario, devuelve un código de error **NTSTATUS** .

## <a name="remarks"></a>Observaciones

En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:

-   [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Supervisar funciones de configuración](monitor-configuration-functions.md)
</dt> </dl>

 


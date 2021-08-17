---
title: Función DDCCIGetCapabilitiesStringLength
description: Obtiene la longitud de una cadena de funcionalidades para un monitor.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configuración del monitor de la función DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd30aeb1e71d88b649478d0ecd1c3052dbbe32372909882f73ae77db6e4dbc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066615"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a>Función DDCCIGetCapabilitiesStringLength

> [!IMPORTANT]
> La API de configuración de monitor usa esta función para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene la longitud de una cadena de funcionalidades para un monitor.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMonitor* \[ En\]
</dt> <dd>

Identificador de un monitor físico.

</dd> <dt>

*pdwLength* \[ out\]
</dt> <dd>

Recibe la longitud de la cadena de funcionalidades, en caracteres, incluido el carácter nulo de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

Las aplicaciones deben [**llamar a GetCapabilitiesStringLength en**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) lugar de llamar a esta función.

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

 


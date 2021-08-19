---
title: Función DDCCISetVCPFeature
description: Establece el valor de un código Panel de control virtual (VCP) para un monitor.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Configuración del monitor de la función DDCCISetVCPFeature
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecbfb6172ffd61dd7882895c0db15baddf28986493b202e2fd873135cee41d76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806153"
---
# <a name="ddccisetvcpfeature-function"></a>Función DDCCISetVCPFeature

> [!IMPORTANT]
> Esta función la usa la API de configuración de monitor para acceder a la funcionalidad en el controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Establece el valor de un código Panel de control virtual (VCP) para un monitor.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMonitor* \[ En\]
</dt> <dd>

Identificador de un monitor físico.

</dd> <dt>

*dwVCPCode* \[ En\]
</dt> <dd>

Código de VCP que se establece.

</dd> <dt>

*dwNewValue* \[ En\]
</dt> <dd>

Valor del código VCP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Comentarios

Las aplicaciones deben llamar [**a SetVCPFeature en**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) lugar de llamar a esta función.

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Supervisar funciones de configuración](monitor-configuration-functions.md)
</dt> </dl>

 


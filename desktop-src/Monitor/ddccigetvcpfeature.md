---
title: Función DDCCIGetVCPFeature
description: Obtiene el valor actual, el valor máximo y el tipo de código de un Panel de control virtual (VCP) para un monitor.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuración del monitor de la función DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641003"
---
# <a name="ddccigetvcpfeature-function"></a>Función DDCCIGetVCPFeature

> [!IMPORTANT]
> Esta función la usa la API de configuración de monitor para acceder a la funcionalidad en el controlador de pantalla. Las aplicaciones no deben llamar a esta función.

 

Obtiene el valor actual, el valor máximo y el tipo de código de un Panel de control virtual (VCP) para un monitor.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
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

Código de VCP que se consulta.

</dd> <dt>

*pvct* \[ out, opcional\]
</dt> <dd>

Recibe el tipo de código VCP, como miembro de la [**enumeración MC \_ VCP \_ CODE \_ TYPE.**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type)

</dd> <dt>

*pdwCurrentValue* \[ out\]
</dt> <dd>

Recibe el valor actual del código VCP.

</dd> <dt>

*pdwMaximumValue* \[ out, opcional\]
</dt> <dd>

Recibe el valor máximo del código VCP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **STATUS \_ SUCCESS**. De lo contrario, devuelve un código de error **NTSTATUS.**

## <a name="remarks"></a>Observaciones

Las aplicaciones deben [**llamar a GetVCPFeatureAndVCPFeatureReply en**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) lugar de llamar a esta función.

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

 


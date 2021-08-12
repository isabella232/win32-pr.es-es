---
title: Método SetDeviceRedirectionType de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece la propiedad DeviceRedirectionType, que controla qué dispositivos se redirigirán.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Método SetDeviceRedirectionType Servicios de Escritorio remoto
- Método SetDeviceRedirectionType Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd3ccbe06acbc75e8c7c29632d7fd83dc0af222eb004c6b83976e3f6478f705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604664"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetDeviceRedirectionType de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece la **propiedad DeviceRedirectionType,** que controla qué dispositivos se redirigirán.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DeviceRedirectionType* \[ En\]
</dt> <dd>

Tipo de redireccionamiento del dispositivo.

<dt>

0
</dt> <dd>

Se redirigirán todos los dispositivos.

</dd> <dt>

1
</dt> <dd>

No se redirigirá ningún dispositivo.

</dd> <dt>

2
</dt> <dd>

Los dispositivos especificados no se redirigirán. Las **propiedades DiskDrivesDisabled**, **PrintersDisabled,** **SerialPortsDisabled,** **ClipboardDisabled** y **PlugAndPlayDevicesDisabled** controlan qué dispositivos no se redirigirán.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


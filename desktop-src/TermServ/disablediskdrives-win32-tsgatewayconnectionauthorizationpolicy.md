---
title: Método DisableDiskDrives de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece la propiedad DiskDrivesDisabled.
ms.assetid: bdc4a923-bda7-464a-95eb-95231374ac93
ms.tgt_platform: multiple
keywords:
- Método DisableDiskDrives Servicios de Escritorio remoto
- Método DisableDiskDrives Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , DisableDiskDrives
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableDiskDrives
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4ddcac0641139cd6b88a9cffd783ee1ca2eef7b53b08f0f6df1b6eeb54fa97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574805"
---
# <a name="disablediskdrives-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableDiskDrives de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece la **propiedad DiskDrivesDisabled.** Si la propiedad **DeviceRedirectionType** tiene un valor de "2", la propiedad **DiskDrivesDisabled** controla el redireccionamiento de las unidades de disco cliente para las sesiones que se establecen a través del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableDiskDrives(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Deshabilitado* \[ En\]
</dt> <dd>

Nuevo valor para **la propiedad DiskDrivesDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


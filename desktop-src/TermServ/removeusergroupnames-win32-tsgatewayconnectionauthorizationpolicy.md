---
title: Método RemoveUserGroupNames de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Quita los nombres de grupo de usuarios especificados de los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 4ddbac15-7054-482a-8b5c-49551561673e
ms.tgt_platform: multiple
keywords:
- Método RemoveUserGroupNames Servicios de Escritorio remoto
- Método RemoveUserGroupNames Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a695aa0d6abd9bf4e27bd37f54a71ff8ea0c01f588de4733d5ee082503970991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058563"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método RemoveUserGroupNames de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Quita los nombres de grupo de usuarios especificados de los grupos de usuarios existentes en **la propiedad UserGroupNames.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Nombres de grupo de usuarios que se quitarán. Los nombres de grupo de usuarios deben tener el formato *Dominio \\ UserGroupName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Si hay varios nombres de grupo de usuarios en el parámetro *UserGroupNames* y no se puede procesar uno de los nombres, no se procesará ninguno de los nombres.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 


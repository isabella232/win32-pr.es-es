---
title: Método AddUserGroupNames de la Win32_TSGatewayResourceAuthorizationPolicy clase
description: Agrega la lista de nombres de grupos de usuarios separados por punto y coma especificada a los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Método AddUserGroupNames Servicios de Escritorio remoto
- Método AddUserGroupNames Servicios de Escritorio remoto , Win32_TSGatewayResourceAuthorizationPolicy clase
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto método , AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be87eb72790d5852861fe0066bc32e319f0a74ba00af3d0ea38dc0ebcbee9850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610179"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método AddUserGroupNames de la clase \_ TSGatewayResourceAuthorizationPolicy de Win32

Agrega la lista de nombres de grupos de usuarios separados por punto y coma especificada a los grupos de usuarios existentes en **la propiedad UserGroupNames.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Lista separada por punto y coma de nombres de grupo de usuarios que se agregarán a **la propiedad UserGroupNames.** Los nombres de grupo de usuarios deben tener el formato *Dominio \\ UserGroupName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Si hay varios nombres de grupo de usuarios en el parámetro *UserGroupNames* y no se puede procesar uno de ellos, no se procesará ninguno de los nombres.

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


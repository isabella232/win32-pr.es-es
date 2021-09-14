---
title: Método AddUserGroupNames de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Agrega los nombres de grupo de usuarios especificados a la propiedad UserGroupNames.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- Método AddUserGroupNames Servicios de Escritorio remoto
- Método AddUserGroupNames Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891332"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método AddUserGroupNames de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Agrega los nombres de grupo de usuarios especificados a **la propiedad UserGroupNames.**

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


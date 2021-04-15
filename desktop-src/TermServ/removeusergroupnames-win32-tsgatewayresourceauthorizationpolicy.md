---
title: Método RemoveUserGroupNames de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Método RemoveUserGroupNames Servicios de Escritorio remoto
- Método RemoveUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676752"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método RemoveUserGroupNames de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32

Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad **UserGroupNames** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserGroupNames* \[ de\]
</dt> <dd>

Lista separada por puntos y comas de nombres de grupos de usuarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


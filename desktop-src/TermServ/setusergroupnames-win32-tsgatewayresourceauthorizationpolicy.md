---
title: Método SetUserGroupNames de la Win32_TSGatewayResourceAuthorizationPolicy clase
description: Establece la propiedad UserGroupNames para la directiva Escritorio remoto autorización de recursos de escritorio remoto (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Método SetUserGroupNames Servicios de Escritorio remoto
- Método SetUserGroupNames Servicios de Escritorio remoto , Win32_TSGatewayResourceAuthorizationPolicy clase
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto método , SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d4a54f042ebf99ff5a3b1bf16081ce0719578ef7fc2fd272e9ccc07a832822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008575"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método SetUserGroupNames de la clase \_ TSGatewayResourceAuthorizationPolicy de Win32

Establece la **propiedad UserGroupNames para** la directiva Escritorio remoto autorización de recursos de escritorio remoto (RD RAP).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Lista separada por punto y coma de nombres de grupo de usuarios. Los nombres tienen el formato *Dominio \\ UserGroupName*. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se permitirá el acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


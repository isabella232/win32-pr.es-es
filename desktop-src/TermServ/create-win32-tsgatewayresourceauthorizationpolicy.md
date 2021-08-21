---
title: Método Create de la Win32_TSGatewayResourceAuthorizationPolicy clase
description: Crea una directiva Escritorio remoto autorización de recursos de escritorio remoto (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create method Servicios de Escritorio remoto , Win32_TSGatewayResourceAuthorizationPolicy class
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto , Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a85055ed9c8930a47e9a9949693457456fd8f261e1cb458e1092eb570532231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131189"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método Create de la clase \_ TSGatewayResourceAuthorizationPolicy de Win32

Crea una directiva Escritorio remoto autorización de recursos de escritorio remoto (RD RAP).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre de RD RAP.

</dd> <dt>

*Descripción* \[ En\]
</dt> <dd>

Descripción del RD RAP.

</dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Indica si el RAP de Escritorio remoto se va a habilitar.

</dd> <dt>

*ResourceGroupType* \[ En\]
</dt> <dd>

Tipo de grupo de recursos.

<dt>

"RG"
</dt> <dd>

Un grupo de recursos

</dd> <dt>

"CG"
</dt> <dd>

Grupo de equipos, tal como se almacena en Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Todos los recursos.

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ En\]
</dt> <dd>

Nombre del grupo de recursos.

</dd> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Lista de nombres de grupos de usuarios separados por punto y coma. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se permitirá el acceso. Los nombres de grupo de usuarios deben tener el formato *Dominio \\ UserGroupName*.

</dd> <dt>

*ProtocolNames* \[ En\]
</dt> <dd>

Lista separada por punto y coma de los nombres de protocolo que están habilitados para esta directiva. Los nombres deben coincidir con la devolución del [**método GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32.**](win32-tsgatewayserversettings.md)

</dd> <dt>

*PortNumbers* \[ En\]
</dt> <dd>

Lista separada por punto y coma de números de puerto que están habilitados para esta directiva. Para permitir cualquier número de puerto, establezca " \* ".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


---
title: Método Update de la Win32_TSGatewayResourceAuthorizationPolicy clase
description: Actualiza la directiva Escritorio remoto autorización de recursos de escritorio remoto \160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Actualización del método Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto , Win32_TSGatewayResourceAuthorizationPolicy clase
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto método , Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330bf14759f7cdef129a4c34b32acde1d610619c7f54f7d6ec95789e6bec390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868925"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método Update de la clase \_ TSGatewayResourceAuthorizationPolicy de Win32

Actualiza la directiva de Escritorio remoto autorización de recursos de escritorio remoto (RD RAP).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del ARCHIVO DE ESCRITORIO REMOTO.

</dd> <dt>

*Descripción* \[ En\]
</dt> <dd>

Descripción del RD RAP.

</dd> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Indica si el RD RAP debe estar habilitado.

</dd> <dt>

*ResourceGroupName* \[ En\]
</dt> <dd>

Nombre del grupo de recursos asociado a este RAP de Escritorio remoto.

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

Grupo de equipos, tal como se almacena Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Todos los recursos.

</dd> </dl> </dd> <dt>

*UserGroupNames* \[ En\]
</dt> <dd>

Lista separada por punto y coma de nombres de grupo de usuarios. Los nombres tienen el formato *Dominio \\ UserGroupName*. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se permitirá el acceso.

</dd> <dt>

*ProtocolNames* \[ En\]
</dt> <dd>

Lista separada por punto y coma de nombres de protocolo que están habilitados para esta directiva. Los nombres deben coincidir con la devolución del [**método GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32.**](win32-tsgatewayserversettings.md)

</dd> <dt>

*PortNumbers* \[ En\]
</dt> <dd>

Lista separada por punto y coma de números de puerto que están habilitados para esta directiva. Para permitir cualquier número de puerto, establezca " \* ".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

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

 


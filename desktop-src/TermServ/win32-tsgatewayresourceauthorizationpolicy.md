---
title: Win32_TSGatewayResourceAuthorizationPolicy clase
description: Describe una directiva Escritorio remoto autorización de recursos de escritorio remoto \160; RAP). Un escritorio remoto \ 160; RAP se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890617"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Clase \_ TSGatewayResourceAuthorizationPolicy de Win32

Describe una directiva Escritorio remoto autorización de recursos de escritorio remoto (RD RAP). Un RAP de Escritorio remoto se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Members

La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Agrega los nombres de grupo de usuarios especificados a los grupos de usuarios existentes en **la propiedad UserGroupNames.**<br/>      |
| [**Crear**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Crea un RAP de Escritorio remoto.<br/>                                                                                       |
| [**Eliminar**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Elimina el RAP de Escritorio remoto actual.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Quita los nombres de grupo de usuarios especificados de los grupos de usuarios existentes en **la propiedad UserGroupNames.**<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Establece la **propiedad Description** para RD RAP.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Habilita o deshabilita el RAP de Escritorio remoto estableciendo la **propiedad Enabled.**<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Establece la **propiedad Name** para RD RAP.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Establece la **propiedad PortNumbers** para RD RAP.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Establece las **propiedades ResourceGroupType** **y ResourceGroupName.**<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Establece la **propiedad UserGroupNames** para RD RAP.<br/>                                                     |
| [**Actualizar**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Actualiza el RAP de Escritorio remoto actual.<br/>                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del RD RAP. Esta propiedad se cambia con el [**método SetDescription.**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si este RD RAP está habilitado. Esta propiedad se cambia con el [**método SetEnabled.**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre de RD RAP. Esta propiedad se cambia con el [**método SetName.**](setname-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de números de puerto separados por punto y coma que se permiten para esta directiva. Para permitir cualquier número de puerto, establezca " \* ".

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de protocolo separados por punto y coma que están habilitados para esta directiva. Los nombres deben coincidir con la devolución del [**método GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32.**](win32-tsgatewayserversettings.md)

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del grupo de recursos. Esta propiedad se cambia con el [**método SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el tipo del grupo de recursos. Esta propiedad se cambia con el [**método SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

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

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de grupos de usuarios separados por punto y coma. Si el usuario pertenece a cualquiera de estos grupos de usuarios, se permitirá el acceso. Esta propiedad se cambia con los [**métodos SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)y [**RemoveUserGroupNames.**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**TSGatewayRADIUSServer de Win32 \_**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


---
title: Win32_TSGatewayResourceAuthorizationPolicy (clase)
description: Describe una Escritorio remoto Directiva de autorización de recursos (RD \ 160; RAP). Un RD \ 160; RAP se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto puerta de enlace de escritorio remoto.
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayResourceAuthorizationPolicy de clase, se describe
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079294"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>\_Clase Win32 TSGatewayResourceAuthorizationPolicy

Describe una Escritorio remoto Directiva de autorización de recursos (RAP de RD). Una RAP de RD se usa para decidir si un usuario está autorizado para conectarse a un recurso especificado a través de Escritorio remoto puerta de enlace de escritorio remoto.

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

## <a name="members"></a>Miembros

La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSGatewayResourceAuthorizationPolicy** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Agrega los nombres de grupos de usuarios especificados a los grupos de usuarios existentes en la propiedad **UserGroupNames** .<br/>      |
| [**A**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Crea una RAP de RD.<br/>                                                                                       |
| [**Elimínelos**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Elimina la RAP de RD actual.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Quita los nombres de grupos de usuarios especificados de los grupos de usuarios existentes en la propiedad **UserGroupNames** .<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Establece la propiedad **Description** para la rap de Rd.<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Habilita o deshabilita la RAP de RD estableciendo la propiedad **Enabled** .<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Establece la propiedad de **nombre** para la rap de Rd.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Establece la propiedad **PortNumbers** para la rap de Rd.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Establece las propiedades **ResourceGroupType** y **ResourceGroupName** .<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Establece la propiedad **UserGroupNames** para la rap de Rd.<br/>                                                     |
| [**Update**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Actualiza la RAP de RD actual.<br/>                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayResourceAuthorizationPolicy de Win32** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción de la RAP de RD. Esta propiedad se cambia con el método [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si esta RAP de RD está habilitada. Esta propiedad se cambia con el método [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre de la RAP de RD. Esta propiedad se cambia con el método [**setName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de números de Puerto separados por punto y coma que se permiten para esta Directiva. Para permitir cualquier número de puerto, establezca " \* ".

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de nombres de protocolos separados por punto y coma que están habilitados para esta Directiva. Los nombres deben coincidir con el valor devuelto del método [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32**](win32-tsgatewayserversettings.md) .

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del grupo de recursos. Esta propiedad se cambia con el método [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el tipo del grupo de recursos. Esta propiedad se cambia con el método [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

<dt>

RG
</dt> <dd>

Un grupo de recursos

</dd> <dt>

CG
</dt> <dd>

Grupo de equipos, tal como se almacena en Active Directory Domain Services.

</dd> <dt>

TODOS
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

Lista separada por puntos y comas de nombres de grupos de usuarios. Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso. Esta propiedad se cambia con los métodos [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)y [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar esta clase, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


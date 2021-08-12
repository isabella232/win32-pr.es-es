---
title: Win32_TSGatewayResourceGroup clase
description: Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ba4ec4545502d82a3449cee39954deb9b5b2e68bf7c657423e673c582d1c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603895"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Clase \_ TSGatewayResourceGroup de Win32

Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayResourceGroup de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayResourceGroup de Win32** tiene estos métodos.



| Método                                                                  | Descripción                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Agrega recursos a la **propiedad Recursos** para este grupo de recursos.<br/>      |
| [**Crear**](create-win32-tsgatewayresourcegroup.md)                   | Crea un grupo de recursos.<br/>                                                  |
| [**Eliminar**](delete-win32-tsgatewayresourcegroup.md)                   | Elimina este grupo de recursos.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Elimina los recursos de la **propiedad Recursos** de este grupo de recursos.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Establece la **propiedad Description** para este grupo de recursos.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Establece la **propiedad Name** para este grupo de recursos.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Establece la **propiedad Resources** para este grupo de recursos.<br/>                   |
| [**actualizar**](update-win32-tsgatewayresourcegroup.md)                   | Actualiza este grupo de recursos.<br/>                                               |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayResourceGroup de Win32** tiene estas propiedades.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista separada por punto y coma de Servicios de Escritorio remoto de autorización de recursos (RAP de Escritorio remoto) asociadas a este grupo de recursos.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del grupo de recursos. Esta propiedad se puede cambiar con el [**método SetDescription.**](setdescription-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del grupo de recursos. Esta propiedad se puede cambiar con el [**método SetName.**](setname-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Recursos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de recursos separados por punto y coma de este grupo de recursos. "" \* significa todos los recursos. Esta propiedad se puede cambiar con los [**métodos SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources,**](addresources-win32-tsgatewayresourcegroup.md) [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) [**y Update.**](update-win32-tsgatewayresourcegroup.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


---
title: Win32_TSGatewayResourceGroup (clase)
description: Describe un grupo de recursos, que asigna un conjunto de recursos (nombres de equipo) a una sola entidad.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayResourceGroup de clase, se describe
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
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685959"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>\_Clase Win32 TSGatewayResourceGroup

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

La clase **Win32 \_ TSGatewayResourceGroup** tiene estos métodos.



| Método                                                                  | Descripción                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Agrega recursos a la propiedad **Resources** para este grupo de recursos.<br/>      |
| [**A**](create-win32-tsgatewayresourcegroup.md)                   | Crea un grupo de recursos.<br/>                                                  |
| [**Elimínelos**](delete-win32-tsgatewayresourcegroup.md)                   | Elimina este grupo de recursos.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Elimina recursos de la propiedad **Resources** para este grupo de recursos.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Establece la propiedad **Description** para este grupo de recursos.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Establece la propiedad de **nombre** para este grupo de recursos.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Establece la propiedad **Resources** para este grupo de recursos.<br/>                   |
| [**Update**](update-win32-tsgatewayresourcegroup.md)                   | Actualiza este grupo de recursos.<br/>                                               |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayResourceGroup de Win32** tiene estas propiedades.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista separada por punto y coma de Servicios de Escritorio remoto directivas de autorización de recursos (RAP de RD) que están asociadas a este grupo de recursos.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del grupo de recursos. Esta propiedad se puede cambiar con el método [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del grupo de recursos. Esta propiedad se puede cambiar con el método [**setName**](setname-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Recursos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de recursos separados por punto y coma en este grupo de recursos. Un " \* " hace referencia a todos los recursos. Esta propiedad se puede cambiar con los métodos [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)y [**Update**](update-win32-tsgatewayresourcegroup.md) .

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


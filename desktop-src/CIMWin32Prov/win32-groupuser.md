---
description: La \_ clase WMI GroupUser Association de Win32 relaciona un grupo y una cuenta que es miembro de ese grupo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Win32_GroupUser (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496528"
---
# <a name="win32_groupuser-class"></a>\_Clase Win32 GroupUser

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ GroupUser** Association de Win32 relaciona un grupo y una cuenta que es miembro de ese grupo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ GroupUser de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ GroupUser de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ Grupo Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| Grupo Win32 de WMI \_ ")
</dt> </dl>

Referencia a la instancia de que representa el grupo del que la cuenta es miembro.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ cuenta de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| cuenta de Win32 de WMI \_ ")
</dt> </dl>

Referencia a la instancia de que representa la cuenta de usuario o del sistema que forma parte de un grupo de cuentas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ GroupUser de Win32** se deriva [**del \_ componente CIM**](cim-component.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de PowerShell sobre \_ Cómo usar Win32 GroupUser para recuperar una lista de miembros del grupo local, consulte el ejemplo de la [lista de miembros del grupo local en un equipo remoto mediante WMI y PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) en la galería de TechNet.

El ejemplo de código VBScript del administrador de [información de WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet usa la clase **Win32 \_ GroupUser** para recuperar información de usuario de varios equipos remotos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


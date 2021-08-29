---
description: La clase WMI de asociación GroupUser de Win32 relaciona un grupo y una cuenta \_ que es miembro de ese grupo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Win32_GroupUser clase
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
ms.openlocfilehash: b71b3d183833ff822b40ff8e44e322b1d0e75880481d2e1f2d0f5825c002b24f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878655"
---
# <a name="win32_groupuser-class"></a>Clase GroupUser de Win32 \_

La clase WMI **de asociación \_ GroupUser** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona un grupo y una cuenta que es miembro de ese grupo.

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

Tipo de datos: **Grupo Win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Group")
</dt> </dl>

Referencia a la instancia de que representa el grupo del que es miembro la cuenta.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cuenta win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Account")
</dt> </dl>

Referencia a la instancia de que representa la cuenta de usuario o del sistema que forma parte de un grupo de cuentas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ GroupUser de Win32** se deriva del [**componente CIM \_**](cim-component.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de PowerShell sobre el uso de GroupUser de Win32 para recuperar una lista de miembros del grupo local, vea el ejemplo Enumerar miembros del grupo local en un equipo remoto mediante WMI y PowerShell en la Galería de \_ TechNet. [](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5)

En el ejemplo de código VBScript de WMI [Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la Galería de TechNet se usa la clase **\_ GroupUser de Win32** para recuperar información de usuario de varios equipos remotos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


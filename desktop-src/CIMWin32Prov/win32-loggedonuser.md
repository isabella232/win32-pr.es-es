---
description: La \_ clase WMI LoggedOnUser Association de Win32 relaciona una sesión y una cuenta de usuario.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907461"
---
# <a name="win32_loggedonuser-class"></a>\_Clase Win32 LoggedOnUser

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoggedOnUser** Association de Win32 relaciona una sesión y una cuenta de usuario.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ LoggedOnUser de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LoggedOnUser de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ cuenta de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (antecedente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**\_ Cuenta de Win32**](win32-account.md) que describe la cuenta utilizada en el inicio de esta sesión. La cuenta puede ser una cuenta de usuario o una cuenta del sistema.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogonSession**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (dependiente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**\_ LogonSession de Win32**](win32-logonsessionmappeddisk.md) que describe la sesión que la cuenta está usando actualmente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ LoggedOnUser de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).

## <a name="examples"></a>Ejemplos

El ejemplo de PowerShell de la [función get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) obtiene los usuarios que han iniciado sesión en un equipo local o remoto, con información de la sesión.

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

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


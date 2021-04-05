---
description: Win32 \_ LogicalProgramGroup&\# 8194; La clase WMI representa un grupo de programas en un equipo que ejecuta Windows. Por ejemplo, accesorios o inicio.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907416"
---
# <a name="win32_logicalprogramgroup-class"></a>\_Clase Win32 LogicalProgramGroup

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroup de Win32** representa un grupo de programas en un equipo con Windows. Por ejemplo, accesorios o inicio.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a>Miembros

La **clase \_ LogicalProgramGroup de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogicalProgramGroup de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")
</dt> </dl>

Una descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**GroupName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue métodos de clase \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")
</dt> </dl>

Nombre del grupo de programas de Windows. Los grupos de programas se implementan como carpetas de archivos en Win32.

Ejemplo: " \\ herramientas del sistema de accesorios"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")
</dt> </dl>

Nombre asignado por el usuario seguido del nombre del grupo. Los grupos de programas se implementan como carpetas de archivos en Win32.

Ejemplo: "todos los usuarios: accesorios \\ herramientas del sistema"

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir un estado operativo y no operativo. El estado operativo puede ser "correcto", "degradado" y "Pred FAIL". "Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio". "Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** ("Aceptar")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred FAIL** ("Pred FAIL")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detener** ("detener")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

Con **estrés** ("acentuado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Recover** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicación perdida** ("pérdida de comunicación")


</dt> <dd></dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| CWbemProviderGlue métodos de clase \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")
</dt> </dl>

Usuarios que pueden tener acceso al grupo de programas de Windows. Los grupos de programas se implementan como carpetas de archivos en Win32.

Ejemplo: "todos los usuarios"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ LogicalProgramGroup de Win32** se deriva de [**\_ ProgramGroupOrItem de Win32**](win32-programgrouporitem.md).

El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


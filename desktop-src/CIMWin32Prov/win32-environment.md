---
description: Representa un entorno o una configuración de entorno del sistema en un equipo Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907523"
---
# <a name="win32_environment-class"></a>\_Clase de entorno Win32

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ entorno Win32** representa un entorno o una configuración de entorno del sistema en un equipo Windows. Al consultar esta clase se devuelven las variables de entorno que se encuentran en:

**HKEY \_ Entorno de \_ equipo local** \\  \\ **CurrentControlSet** \\ **control** \\ **SessionManager** \\ **Environment**

y

**HKEY \_** \\ Entorno de **< usuario >** de usuarios \\ 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a>Miembros

La clase de **\_ entorno Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ entorno Win32** tiene estas propiedades.

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

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")
</dt> </dl>

Cadena de caracteres que especifica el nombre de una variable de entorno basada en Windows. Al especificar el nombre de una variable que aún no existe, una aplicación crea una nueva variable de entorno.

Ejemplo: "path"

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

**SystemVariable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")
</dt> </dl>

Indica si la variable es una variable del sistema. El sistema operativo establece una variable del sistema y es independiente de la configuración del entorno del usuario.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")
</dt> </dl>

Nombre del propietario de la configuración del entorno. Se establece en <SYSTEM> para la configuración específica del sistema basado en Windows (en oposición a un usuario específico) y <DEFAULT> para la configuración de usuario predeterminada.

Ejemplo: "JSmith"

</dd> <dt>

**VariableValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")
</dt> </dl>

Variable de marcador de posición de una variable de entorno basada en Windows. La información como el directorio del sistema de archivos puede cambiar de equipo a equipo. El sistema operativo sustituye los marcadores de posición por estos.

Ejemplo: "% SystemRoot%"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ entorno de Win32** se deriva de [**\_ SystemResource CIM**](cim-systemresource.md). Puede usar esta clase para buscar las rutas de acceso de carpetas especiales, como la carpeta del sistema o los archivos de programa en un equipo remoto. Algunos ejemplos son: WINDIR, raízDelSistema, ProgramFiles y userprofile. **Win32 \_** Básicamente, el entorno devuelve lo que se puede encontrar en:

**HKEY \_ Entorno de \_ equipo local** \\  \\ **CurrentControlSet** \\ **control** \\ **SessionManager** \\ **Environment**

y

**HKEY \_** \\ Entorno de **< usuario >** de usuarios \\ 

El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Ejemplos

La [lista de variables de entorno en un equipo Perl de](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) ejemplo usa WMI para devolver información acerca de todas las variables de entorno de un equipo.

En el siguiente ejemplo de código de VBScript se enumeran las variables de entorno en el equipo local.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



El siguiente ejemplo de código de VBScript cambia una variable de entorno denominada \_ tipo de compilación a una entrada de valor por el usuario. El script supone que la variable de tipo de compilación \_ ya existe. Si no existe, el script finaliza. Se comprueba el valor de entrada: debe ser "Build1", "Build2" o "Build3" y no se acepta ningún otro valor. La función [UCase](https://msdn.microsoft.com/library/aa902519.aspx) de VBScript hace que la entrada no distinga mayúsculas de minúsculas. Si lo que se escribe no es uno de los tres valores aceptables, el script finaliza.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



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

[**\_SYSTEMRESOURCE CIM**](cim-systemresource.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 


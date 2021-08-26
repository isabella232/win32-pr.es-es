---
title: Win32_Terminal clase
description: Representa un terminal.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal clase Servicios de Escritorio remoto
- Win32_Terminal clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43f3998e1b8f9e7d252a8a4c949d7d083c763a8759d7c9df6aa60c21618e217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867965"
---
# <a name="win32_terminal-class"></a>Clase Terminal win32 \_

La **clase WMI de \_ terminal Win32** representa un terminal.

La sintaxis siguiente se simplifica a partir del código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a>Miembros

La **clase \_ Terminal win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Terminal win32** tiene estos métodos.



| Método                                  | Descripción                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Crear**](create-win32-terminal.md) | Crea un terminal con la configuración predeterminada que se puede personalizar mediante las propiedades y los métodos de las clases [**\_ TerminalSetting de Win32.**](win32-terminalsetting.md)<br/> |
| [**Eliminar**](delete-win32-terminal.md) | Elimina el terminal especificado.<br/>                                                                                                                                              |
| [**Habilitar**](win32-terminal-enable.md) | Deshabilita o habilita el terminal.<br/>                                                                                                                                            |
| [**Renombrar**](win32-terminal-rename.md) | Cambia el nombre del terminal.<br/>                                                                                                                                                        |



 

### <a name="properties"></a>Propiedades

La **clase \_ Terminal win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**fEnableTerminal**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el terminal especificado está deshabilitado o habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

El terminal está deshabilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

El terminal está habilitado.

</dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LoggedOnUsers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de sesiones iniciadas para el terminal.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Entre los estados no operativo se incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los otros estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("Ok")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Error previo")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Deteniendo")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre único que identifica la instancia del terminal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**Win32 \_ Terminal** está asociado a [**\_ TerminalSetting de Win32**](win32-terminalsetting.md) como la **propiedad Element** de la asociación [**\_ TerminalTerminalSetting de Win32.**](win32-terminalterminalsetting.md)

Las siguientes clases son subclases de la clase **\_ Terminal Win32: Win32** [**\_ TSGeneralSetting,**](win32-tsgeneralsetting.md) [**Win32 \_ TSLogonSetting,**](win32-tslogonsetting.md) [**Win32 \_ TSSessionSetting,**](win32-tssessionsetting.md) [**Win32 \_ TSEnvironmentSetting,**](win32-tsenvironmentsetting.md) [**Win3 2 \_ TSRemoteControlSetting,**](win32-tsremotecontrolsetting.md) [**Win32 \_ TSClientSetting,**](win32-tsclientsetting.md) [**Win32 \_ TSNetworkAdapterSetting,**](win32-tsnetworkadaptersetting.md) [**Win32 \_ TSNetworkAdapterListSetting,**](win32-tsnetworkadapterlistsetting.md) [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)y [**Win32 \_ TSAccount**](win32-tsaccount.md).

Tenga en cuenta que las winstations asociadas a la sesión de consola no pueden tener acceso a los métodos y propiedades de esta clase. Si se intenta hacerlo especificando "Console" como valor de la propiedad **TerminalName,** los métodos de este objeto **devuelven WBEM \_ E NOT \_ \_ SUPPORTED**. Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.

Para conectarse al espacio \\ de nombres Raíz de \\ TerminalServices CIMV2, el nivel de \\ autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN LEVEL \_ \_ PKT \_ PRIVACY**. Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación **de WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el Visual Basic ejemplo de Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> <dt>

[**Terminal \_ Win32TerminalSetting**](win32-terminalterminalsetting.md)
</dt> </dl>

 


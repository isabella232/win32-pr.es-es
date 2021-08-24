---
title: Win32_TSEnvironmentSetting clase
description: Define los valores de configuración de la clase Terminal Win32, \_ incluida la directiva de programa inicial.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting clase Servicios de Escritorio remoto
- Win32_TSEnvironmentSetting clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ede3347581267d9fcec00a82c016c273c239c9673b536843753e6b59ec2341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514325"
---
# <a name="win32_tsenvironmentsetting-class"></a>Clase \_ TSEnvironmentSetting de Win32

La clase WMI **Win32 \_ TSEnvironmentSetting** define los valores de configuración de la clase [**\_ Terminal Win32,**](win32-terminal.md) incluida la directiva de programa inicial.

La sintaxis siguiente se simplifica a partir del código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSEnvironmentSetting de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSEnvironmentSetting de Win32** tiene estos métodos.



| Método                                                                      | Descripción                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**InitialProgram**](win32-tsenvironmentsetting-initialprogram.md)         | Establece las propiedades del programa de inicio incluidas en esta clase.<br/> |
| [**SetClientWallPaper**](win32-tsenvironmentsetting-setclientwallpaper.md) | Establece la **propiedad ClientWallPaper.**<br/>                      |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSEnvironmentSetting de Win32** tiene estas propiedades.

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

**ClientWallPaper**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si la imagen de fondo de pantalla se muestra en el cliente. No mostrar la imagen de papel tapiz puede ahorrar recursos del sistema al reducir el tiempo necesario para volver a dibujar la pantalla.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

La imagen de fondo de pantalla no se muestra en el cliente.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

La imagen de fondo de pantalla se muestra en el cliente.

</dd> </dl>

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

**InitialProgramPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre y la ruta de acceso del programa que el usuario ejecutará inmediatamente después de iniciar sesión en el servidor host de sesión de Escritorio remoto.

</dd> <dt>

**InitialProgramPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Directiva que usa el servidor para determinar la ruta de acceso del programa de inicio y el nombre de archivo, así como el nombre de la carpeta en la que se encuentra.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)


</dt> <dd>

La configuración del programa de inicio del usuario está en vigor.

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de** servidor (1)


</dt> <dd>

El servidor reemplaza la configuración del programa de inicio del usuario.

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Modo de aplicación única** (2)


</dt> <dd>

Solo se ejecutará una aplicación en esta sesión. Se omite la información del programa de inicio.

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PolicySourceClientWallPaper**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la **propiedad ClientWallPaper** está configurada por el servidor, la directiva de grupo o de forma predeterminada.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> <dt>

2
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceInitialProgramPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la **propiedad InitialProgramPath** está configurada por el servidor, la directiva de grupo o de forma predeterminada.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> <dt>

2
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceStartIn**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la **propiedad StartIn** está configurada por el servidor, la directiva de grupo o de forma predeterminada.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Directiva de grupo

</dd> <dt>

2
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**Inicio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso del directorio de trabajo del programa que el usuario ejecutará inmediatamente después de iniciar sesión en el servidor host de sesión de Escritorio remoto.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

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
</dt> </dl>

Nombre del terminal.

Esta propiedad se hereda de [**\_ TerminalSetting de Win32.**](win32-terminalsetting.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que las winstations asociadas a la sesión de consola no pueden tener acceso a los métodos y propiedades de esta clase. Si se intenta hacerlo especificando "Console" como valor de la propiedad **TerminalName,** los métodos de este objeto **devuelven WBEM \_ E NOT \_ \_ SUPPORTED**. Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.

Para conectarse al espacio \\ de nombres raíz de \\ TerminalServices cimv2, el nivel de \\ autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN LEVEL \_ \_ PKT \_ PRIVACY**. Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el ejemplo Visual Basic Scripting Edition (VBScript) siguiente se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Terminal \_ Win32Setting**](win32-terminalsetting.md)
</dt> </dl>

 


---
description: El PUASample.msi de ejemplo es un ejemplo de un paquete de Windows Installer 5,0 dual que es capaz de instalarse en el contexto de instalación por usuario o por equipo en Windows Server 2008 R2 y Windows 7.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Ejemplo de creación de un solo paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652851"
---
# <a name="single-package-authoring-example"></a>Ejemplo de creación de un solo paquete

El PUASample.msi de ejemplo es un ejemplo de un paquete de Windows Installer 5,0 dual que es capaz de instalarse en el [contexto de instalación](installation-context.md) por usuario o por equipo en windows Server 2008 R2 y Windows 7. Este paquete de ejemplo sigue las instrucciones de desarrollo descritas en [creación de un solo paquete](single-package-authoring.md).

## <a name="obtaining-a-copy-of-the-sample"></a>Obtener una copia del ejemplo

Una copia de este ejemplo y un editor de tablas de Windows Installer Database, Orca.exe, se encuentran en los [componentes Windows SDK para los programadores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). El ejemplo y el editor de tablas se proporcionan con el kit de desarrollo de software de Windows para Windows Server 2008 R2 y Windows 7, ya que los archivos de instalación de Windows Installer PUASample1.msi y Orca.msi.

## <a name="system-requirements"></a>Requisitos del sistema

El editor de base de datos, [Orca.exe](orca-exe.md), requiere windows Server 2008 R2 y versiones anteriores, y Windows 7 y versiones anteriores. El paquete de doble propósito, PUASample1.msi, puede instalarse en el [contexto de instalación](installation-context.md) por equipo o por usuario en windows Server 2008 R2 y Windows 7. PUASample1.msi solo se puede instalar en el contexto por equipo en Windows Server 2008 y versiones anteriores, y en Windows Vista y versiones anteriores. Puede instalar el editor de base de datos para examinar el contenido de PUASample1.msi sin instalar el ejemplo. Para instalar los paquetes del editor o del ejemplo, asegúrese de que la directiva [DisableMSI](disablemsi.md) no esté establecida en un valor que bloquee las instalaciones de aplicaciones.

## <a name="identifying-a-dual-purpose-package"></a>Identificar un paquete de Dual-Purpose

Los paquetes de doble propósito deben inicializar el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) en 1. Esto identifica el paquete como capaz de instalarse en el contexto por equipo o por usuario en Windows Server 2008 R2 y Windows 7. Establezca la propiedad **MSIINSTALLPERUSER** en el paquete solo si se ha escrito siguiendo las instrucciones de desarrollo descritas en [creación de paquetes única](single-package-authoring.md) y si desea proporcionar a los usuarios la opción de instalar el paquete en el contexto por usuario o por equipo. Un paquete de uso doble también debe inicializar el valor de la propiedad [**AllUsers**](allusers.md) en 2. Esto especifica por usuario como el contexto de instalación predeterminado de la aplicación. Si el valor de la propiedad **AllUsers** es cualquier valor distinto de 2, Windows Installer omite la propiedad **MSIINSTALLPERUSER** .

Use un editor de base de datos de Windows Installer, como [Orca.exe](orca-exe.md), para examinar el contenido de PUASample1.msi. La tabla de [propiedades](property-table.md) del paquete de ejemplo contiene las dos entradas siguientes.

[Propiedad](property-table.md) Tabla (parcial)

| Propiedad          | Value |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Cuadro de diálogo personalizado para el contexto de instalación

La [interfaz de usuario](user-interface.md) del paquete de ejemplo incluye un ejemplo de un cuadro de diálogo personalizado, VerifyReadyDialog, que permite a los usuarios seleccionar el contexto de instalación por usuario o por equipo en el momento de la instalación. La tabla de cuadro de [diálogo](dialog-table.md) contiene un registro que describe el cuadro de diálogo VerifyReadyDialog. El valor especificado en el campo atributos es 39 porque este cuadro de diálogo usa los [bits de estilo](dialog-style-bits.md)de cuadro de diálogo msidbDialogAttributesVisible (1), msidbDialogAttributesModal (2), msidbDialogAttributesMinimize (4) y msidbDialogAttributesTrackDiskSpace (32). La barra de título del cuadro de diálogo muestra un título dado por el valor de la propiedad [**ProductName**](productname.md) .

[Cuadro de diálogo](dialog-table.md) Tabla (parcial) 

| Diálogo            | HCentering | VCentering | Ancho | Alto | Atributos | Title           | Controlar \_ primero | \_Valor predeterminado del control | \_Cancelar control |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | Siguientes             | Cancelar          |



 

La tabla de [control](control-table.md) contiene entradas para los [controles](controls.md) que se muestran en el cuadro de diálogo VerifyReadyDialog. En el cuadro de diálogo se muestran controles [Pushbutton](pushbutton-control.md) y un control de [texto](text-control.md) . Todos los controles usan los [atributos de control](control-attributes.md)msidbControlAttributesEnabled (2) y msidbControlAttributesVisible (1). El control InstallPerMachine también usa el atributo de control [ElevationShield](elevationshield-attribute.md) , msidbControlAttributesElevationShield (8388608). Este atributo de control agrega el icono de elevación de [*control de cuentas de usuario*](u-gly.md) (UAC) al control InstallPerMachine e informa al usuario de que las credenciales de UAC son necesarias para instalar la aplicación en el contexto por equipo. El valor del campo de texto de la tabla de control es el estilo de texto y el texto que muestra el control. Vea la descripción del campo de texto en el tema de la tabla de control para obtener más información sobre cómo agregar texto a un control mediante estilos predefinidos.

[Control](control-table.md) de Tabla (parcial)

| Diálogo\_          | Control           | Tipo       | Atributo | Texto                                                   | Control \_ siguiente     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | Cancelar            | Botones | 3         | { \\ Tahoma10} &cancelar                                    | Siguientes              |
| VerifyReadyDialog | Anterior          | Botones | 3         | { \\ Tahoma10} <<&anterior                          | Cancelar            |
| VerifyReadyDialog | Siguientes              | Botones | 3         | { \\ Tahoma10} &siguiente >>                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Texto       | 3         | ¿Está listo para completar la instalación suspendida? |                   |
| VerifyReadyDialog | InstallPerUser    | Botones | 3         | { \\ Tahoma10} instalación solo para &me                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | Botones | 8388611   | { \\ Tahoma10} instalación para &todos                      | Anterior          |
| VerifyReadyDialog | Cancelar            | Botones | 3         | { \\ Tahoma10} &cancelar                                    | Siguientes              |



 

La tabla [ControlEvent,](controlevent-table.md) especifica el [ControlEvents](control-events.md), o las acciones que realiza el instalador cuando el usuario interactúa con un control. Cuando un usuario activa el Pushbutton de InstallPerUser, la interfaz de usuario muestra un cuadro de diálogo de OutOfDisk si la propiedad [**OutOfDiskSpace**](outofdiskspace.md) es 1, establece el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) en 1, establece el valor de la propiedad [**AllUsers**](allusers.md) en 2, establece la propiedad [**MSIFASTINSTALL**](msifastinstall.md) en 1 y devuelve. Dado que la propiedad **MSIFASTINSTALL** está establecida, no se genera ningún punto de restauración del sistema para la instalación. Cuando un usuario activa el pulsador InstallPerMachine, la interfaz de usuario muestra un cuadro de diálogo OutOfDisk si la propiedad **OutOfDiskSpace** es 1, establece el valor de la propiedad **AllUsers** en 1 y devuelve.

[ControlEvent,](controlevent-table.md) Tabla (parcial) 

| Diálogo\_          | control\_         | Evento                 | Argumento  | Condición                 | Pedido |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| VerifyReadyDialog | InstallPerUser    | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerUser    | EndDialog             | Valor devuelto    | OutOfDiskSpace <> 1 | 5     |
| VerifyReadyDialog | InstallPerUser    | \[MSIINSTALLPERUSER\] | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| VerifyReadyDialog | InstallPerMachine | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerMachine | EndDialog             | Valor devuelto    | OutOfDiskSpace <> 1 | 3     |
| VerifyReadyDialog | InstallPerMachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[MSIFASTINSTALL\]    | 1         | 1                         | 4     |



 

El control InstallPerUser se debe quitar de la interfaz de usuario de cualquier instalación con una versión de Windows Installer anterior a Windows Installer Windows Installer 5,0. La tabla [ControlCondition](controlcondition-table.md) del paquete de ejemplo contiene cuatro entradas que deshabilitan y ocultan el control InstallPerUser si la versión actual es inferior a Windows Installer 5,0. La tabla usa el valor de la propiedad [**VersionMsi**](versionmsi.md) y la [Sintaxis de la instrucción condicional](conditional-statement-syntax.md) para definir esta condición. La acción especificada en el campo acción solo se realiza si la instrucción del campo condición es true.

[ControlCondition](controlcondition-table.md) Tabla (parcial)

| Diálogo\_          | control\_      | Acción  | Condición               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | Habilitar  | VersionMsi >= "5,00" |
| VerifyReadyDialog | InstallPerUser | Disable | VersionMsi < "5,00"  |
| VerifyReadyDialog | InstallPerUser | Mostrar    | VersionMsi >= "5,00" |
| VerifyReadyDialog | InstallPerUser | Ocultar    | VersionMsi < "5,00"  |



 

## <a name="specifying-directory-structure"></a>Especificar la estructura de directorios

Utilice el editor de base de datos para examinar la tabla de [directorios](directory-table.md) de PUASample1.msi. El registro de la tabla de directorio que tiene una cadena vacía en su \_ campo principal de directorio representa el directorio raíz de los árboles de directorio de origen y de destino. Si la propiedad [**targetDir**](targetdir.md) es undefined, el instalador establece su valor en el momento de la instalación en el valor de la propiedad [**ROOTDRIVE**](rootdrive.md) . Si la propiedad [**SourceDir**](sourcedir.md) no está definida, el instalador establece su valor en la ubicación del directorio que contiene el paquete de Windows Installer (archivo. msi). Los nombres de directorio se especifican con el \| formato largo corto.

[Directorio](directory-table.md) de Tabla (parcial)

| Directorio          | Directorio \_ primario  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | Mi proveedor           | Sample1 \| MSDN-PUASample1 |
| Mi proveedor           | ProgramFilesFolder | Msft \| Microsoft          |



 

En el origen, esta tabla de [directorio](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio.

<dl> \[SourceDir \] \\ msft \\ Sample1  
\[SourceDir\]  
</dl>

En el destino, la tabla de [directorio](directory-table.md) se resuelve en las rutas de acceso de la tabla siguiente. El instalador establece los valores de las propiedades [**ProgramFilesFolder**](programfilesfolder.md) y [**ProgramMenuFolder**](programmenufolder.md) en ubicaciones que dependen del [contexto de instalación](installation-context.md) y de si el sistema es la versión de 32 bits o de 64 bits de Windows Server 2008 R2 y Windows 7. Las rutas de acceso a las carpetas de destino dependen de si el usuario selecciona una instalación por usuario o por equipo.

| Contexto de instalación | System                                                                              | Rutas de acceso de ejemplo                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> versión de 32 bits<br/>           | % ProgramFiles% \\ msft \\ Sample1<br/> % ALLUSERSPROFILE% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\<br/>                  |
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> versión de 64 bits<br/>           | % ProgramFiles (x86)% \\ msft \\ Sample1<br/> % ALLUSERSPROFILE% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\<br/>             |
| Per-User             | Windows Server 2008 R2 y Windows 7<br/> versión de 32 bits o de 64 bits<br/> | % USERPROFILE% \\ AppData \\ \\ programas locales \\ msft \\ Sample1<br/> % APPDATA% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\<br/> |



 

Las aplicaciones por usuario deben almacenarse en subcarpetas en la carpeta programas especificada por el valor de la propiedad [**ProgramFilesFolder**](programfilesfolder.md) . Normalmente, la ruta de acceso a la aplicación tiene el formato siguiente.

% LOCALAPPDATA% \\ Programs \\ *ISV Name* \\ *appname*.

Los datos de configuración por usuario deben almacenarse en la carpeta programas especificada por el valor de la propiedad [**ProgramMenuFolder**](programmenufolder.md) . Normalmente, esta carpeta se encuentra en la siguiente ruta de acceso.

% APPDATA% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\

Si instala componentes de [paquete de Windows Installer de 32 bits](32-bit-windows-installer-packages.md) , utilice la propiedad [**ProgramFilesFolder**](programfilesfolder.md) y [**CommonFilesFolder**](commonfilesfolder.md) en la tabla de [directorio](directory-table.md) . Si instala componentes [de paquete de Windows Installer de 64 bits](64-bit-windows-installer-packages.md) , use las propiedades [**ProgramFiles64Folder**](programfiles64folder.md) y [**CommonFiles64Folder**](commonfiles64folder.md) . Si la aplicación contiene versiones de 32 bits y de 64 bits del mismo componente, con el mismo nombre, asegúrese de que estas versiones se guardan en directorios diferentes o asígneles nombres diferentes.

La siguiente tabla de [directorio](directory-table.md) proporciona un ejemplo de un diseño de directorio compatible con un paquete que incluye componentes de 32 y 64 bits e incluye algunos componentes que se comparten entre las aplicaciones.

| Directorio            | Directorio \_ primario    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | .: Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | Mi proveedor             | Sample1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATION       | ShVendor             | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| MSDN-PUASample1          |
| Mi proveedor             | ProgramFilesFolder   | Msft \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | Msft \| Microsoft                   |
| ShVendor             | CommonFilesFolder    | Msft \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | Msft \| Microsoft                   |
| Shrx86               | SHAREDLOCATION       | \|componentes x32 32 bits            |
| Shrx64               | SHAREDLOCATIONX64    | \|componentes de 64 bits de 64            |
| Binx86               | INSTALLLOCATION      | \|componentes x32 32 bits            |
| Binx64               | INSTALLLOCATIONX64   | \|componentes de 64 bits de 64            |
| App32                | Binx86               | MyApp \| unshared 32 componentes de bits |
| App64                | Binx64               | MyApp \| unshared 64 componentes de bits |
| Share32              | Shrx86               | componentes compartidos compartidos \| de 32 bits  |
| Share64              | Shrx64               | componentes compartidos compartidos \| de 64 bits  |



 

En el origen, esta tabla de [directorio](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio.

<dl> \[SourceDir \] Prog32 \\ msft \\ Sample1 \\ x32 \\ MyApp  
\[\]Archivos comunes de SourceDir Share32 \\ \\ msft \\ Sample1 \\ x32 \\ compartidos  
\[SourceDir \] Prog64 \\ msft \\ Sample1 \\ x64 \\  
\[\]Archivos comunes de SourceDir Share64 \\ \\ msft \\ Sample1 \\ x64 \\ compartidos  
\[SourceDir \] Sample1  
</dl>

En el destino, esta tabla de [directorio](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio. Las rutas de acceso de destino dependen del [contexto de instalación](installation-context.md) y del sistema.

| Contexto de instalación | System                                                                              | Rutas de acceso de ejemplo                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> versión de 32 bits<br/>           | % ProgramFiles% \\ msft \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles% \\ archivos comunes \\ msft \\ Sample1 \\ x32 \\ compartidos<br/> % ProgramFiles (x86)% \\ msft \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles (x86)% \\ archivos comunes \\ msft \\ Sample1 \\ x64 \\ compartidos<br/> % ProgramData% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\ \\ Sample1<br/>               |
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> versión de 64 bits<br/>           | % ProgramFiles (x86)% \\ msft \\ Sample1 \\ x32 \\ MyApp<br/> % ProgramFiles (x86)% \\ archivos comunes \\ msft \\ Sample1 \\ x32 \\ compartidos<br/> % ProgramFiles% \\ msft \\ Sample1 \\ x64 \\ MyApp<br/> % ProgramFiles% \\ archivos comunes \\ msft \\ Sample1 \\ x64 \\ compartidos<br/> % ProgramData% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\ \\ Sample1<br/>               |
| Per-User             | Windows Server 2008 R2 y Windows 7<br/> versión de 32 bits o de 64 bits<br/> | % LOCALAPPDATA% \\ Programs \\ msft \\ Sample1 \\ x32 \\ MyApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ msft \\ Sample1 \\ x32 \\ Shared<br/> % LOCALAPPDATA% \\ programas \\ msft \\ Sample1 \\ x64 \\ MyApp<br/> % LOCALAPPDATA% \\ Programs \\ Common \\ msft \\ Sample1 \\ x64 \\ compartidos<br/> % APPDATA% \\ \\ programas del \\ menú Inicio de Microsoft Windows \\ \\ Sample1<br/> |



 

## <a name="application-registration"></a>Registro de la aplicación

El PUASample.msi agrega una subclave a la clave del registro de las rutas de acceso de la aplicación y realiza registros que permiten guardar la información de la aplicación en el registro bajo esta clave. Para obtener más información sobre las rutas de acceso de la aplicación y el registro de aplicaciones, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) en la sección [extensibilidad de Shell](https://msdn.microsoft.com/library/bb762762.aspx) de la [Guía del desarrollador de Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). En el momento de la instalación, el usuario toma la decisión de instalar la aplicación en el contexto de instalación por usuario o por equipo. En el momento en que se crea el paquete de doble propósito, el desarrollador de paquetes no puede saber si los registros deben realizarse en las claves de usuario de la \_ máquina local HKEY \_ o HKEY \_ actual \_ .

El desarrollador de paquetes define el identificador de archivo del archivo ejecutable de la aplicación en el campo de archivo de la tabla de [archivos](file-table.md) .

[Archivo](file-table.md) de Tabla (parcial) 

| Archivo      | Componente\_      | FileName                     | FileSize | Versión | Idioma | Atributos | Secuencia |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppFile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

Los valores que se van a guardar en el registro se pueden especificar en el campo de valor de la tabla [del registro](registry-table.md) como una cadena [con formato](formatted.md) . Use el identificador de archivo definido en el campo de archivo de la tabla de [archivos](file-table.md) y la \[ \#  \] Convención filekey del tipo con formato para especificar el valor predeterminado de la clave del registro de rutas de acceso de la aplicación. La acción de [instalación](install-action.md) de nivel superior realiza las acciones en la tabla [InstallExecuteSequence](installexecutesequence-table.md) . Una vez completadas las acciones [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)y [InstallFinalize](installfinalize-action.md) en esta tabla, la Windows Installer reemplaza la subcadena con formato \[ \# MyAppFile \] en la tabla del registro con la ruta de acceso completa al archivo de la aplicación.

El ejemplo define una propiedad personalizada, RegRoot, para que contenga la ubicación de la clave raíz y utiliza una acción personalizada para restablecer el valor de la propiedad si el usuario elige una instalación por equipo. Use la propiedad personalizada RegRoot en cualquier valor de cadena con formato que haga referencia a la ubicación raíz. En la tabla de [propiedades](property-table.md) , el paquete de PUASample.msi define la propiedad personalizada y establece el valor de REGROOT en HKCU. Esto inicializa el valor de la propiedad para el contexto de instalación por usuario, el contexto predeterminado recomendado para los paquetes de doble finalidad.

[Propiedad](property-table.md) Tabla (parcial)

| Propiedad | Value |
|----------|-------|
| RegRoot  | HKCU  |



 

En la tabla [CustomAction](customaction-table.md) , el paquete define una acción personalizada denominada set \_ RegRoot \_ HKLM. El valor del campo tipo lo identifica como una acción personalizada 51 estándar de [tipo acción personalizada](custom-action-type-51.md) . El significado de los campos de origen y de destino de la tabla CustomAction depende del tipo de acción personalizada. Para obtener más información sobre los tipos estándar de acciones personalizadas, consulte [tipos de acción personalizados](summary-list-of-all-custom-action-types.md). El campo de origen de la \_ \_ acción personalizada Set RegRoot HKLM especifica que el valor de la propiedad RegRoot. Si el instalador realiza la \_ \_ acción personalizada Set RegRoot HKLM, se restablece el valor de la propiedad REGROOT en HKLM.

[CustomAction](customaction-table.md) Tabla (parcial)

| Acción             | Tipo | Source      | Destino |
|--------------------|------|-------------|--------|
| Establecer \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

La acción de [instalación](install-action.md) de nivel superior realiza las acciones de la tabla [InstallExecuteSequence](installexecutesequence-table.md) , en la secuencia especificada en el campo secuencia de esa tabla. El valor creado en el campo Sequence de la \_ \_ acción personalizada Set RegRoot HKLM (1501) especifica que esta acción personalizada se realizará después de la acción [InstallInitialize](installinitialize-action.md) (1500) y antes de la acción [ProcessComponents](processcomponents-action.md) (1600). Esta secuencia garantiza que el registro de la \_ \_ acción personalizada Set RegRoot HKLM se evalúe en el momento de la instalación. Para obtener más información sobre la secuencia recomendada de acciones en la tabla InstallExecuteSequence, consulte el tema [InstallExecuteSequence sugerido](suggested-installexecutesequence.md) . La [Sintaxis de la instrucción condicional](conditional-statement-syntax.md) creada en el campo condición especifica que la \_ acción Set RegRoot \_ HKLM se realice solo si el valor de la propiedad [**AllUsers**](allusers.md) se evalúa como 1 en el momento de la instalación. El valor 1 de la propiedad **AllUsers** especifica una instalación por equipo.

[InstallExecuteSequence](installexecutesequence-table.md) Tabla (parcial)

| Acción             | Condición  | Secuencia |
|--------------------|------------|----------|
| Establecer \_ RegRoot \_ HKLM | ALLUSERS = 1 | 1501     |



 

Los registros siguientes de la tabla [del registro](registry-table.md) realizan los registros si el componente ProductComponent está instalado. El valor-1 en el campo raíz es necesario para realizar el registro en HKEY \_ local \_ Machine para una instalación por usuario y en HKEY \_ Current \_ User para una instalación por usuario. El registro con una cadena vacía en el campo registro agrega una subclave para la aplicación en la clave del registro AppPaths y establece el valor "(default)" en la ruta de acceso completa del archivo ejecutable de la aplicación. El registro MyAppPathAlias asigna el archivo ejecutable a un alias de aplicación y permite que se inicie la aplicación si el usuario escribe el alias "puapct" en un símbolo del sistema. El registro MyAppPathRegistration asigna el nombre del archivo ejecutable a la ruta de acceso completa del archivo.



| Registro              | Root | Clave                                                                     | Nombre | Value                                                                            | Componente        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Software \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[RegRoot \] \\ software \\ Microsoft \\ Windows \\ CurrentVersion apps \\ paths \\PUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion apps \\ paths \\PUAPCT.exe     |      | \[\#MyAppFile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion apps \\ paths \\PUASample1.exe |      | \[\#MyAppFile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>Cancelación del registro de reproducción automática

El PUASample.msi realiza registros que permiten al usuario de la aplicación impedir que se inicie la [reproducción automática de hardware](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) para los dispositivos seleccionados. Para obtener información sobre cómo registrar un controlador para cancelar la reproducción automática en respuesta a un evento, consulte el tema [preparación del hardware y el software para su uso con reproducción automática](/previous-versions//cc144208(v=vs.85)) en la sección [extensibilidad de Shell](https://msdn.microsoft.com/library/bb762762.aspx) de la [Guía del desarrollador de Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). El Registro siguiente registra el controlador especificado en el campo nombre cuando se instala el componente ProductComponent. El valor-1 en el campo raíz es necesario para especificar el Windows Installer que el registro se debe redirigir a una ubicación que depende del contexto de instalación.

[Registro](registry-table.md) de Cuadro 

| Registro                     | Root | Clave                                                                                             | Nombre                                 | Value | Componente        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ CancelAutoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>Registro del controlador de vista previa

El PUASample.msi realiza registros necesarios para instalar un [controlador de vista previa](../shell/preview-handlers.md) que habilita una vista previa de solo lectura de archivos. PUA sin iniciar la aplicación. Para obtener información sobre el registro de controladores de vista previa, consulte el tema [registrar controladores de vista previa](../shell/how-to-register-a-preview-handler.md) en la sección [extensibilidad de Shell](https://msdn.microsoft.com/library/bb762762.aspx) de la [Guía del desarrollador de Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Los registros siguientes de la tabla [del registro](registry-table.md) registran el controlador cuando se instala el componente ProductComponent. El valor-1 en el campo raíz es necesario para especificar el Windows Installer que el registro se debe redirigir a una ubicación que depende del contexto de instalación.

[Registro](registry-table.md) de Cuadro

| Registro                       | Root | Clave                                                                              | Nombre                                   | Value                                        | Componente        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | Clases de software \\ \\ . PUA                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Controlador de vista previa de pruebas de Microsoft Windows PUA   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | Clases de software \\ \\ puafile \\ ShellEx \\ {8895b1c6-b41f-4c1c-a562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Per-User el controlador de vista previa de la presentación del ejemplo 1 | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32,-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | Icono                                   | notepad.exe, 2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ThreadingModel                         | Procesamiento                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 |                                        | \#%% SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 

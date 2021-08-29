---
description: El ejemplo PUASample.msi es un ejemplo de un paquete de Windows Installer 5.0 de uso dual que es capaz de instalarse en el contexto de instalación por usuario o por equipo en Windows Server 2008 R2 y Windows 7.
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: Ejemplo de creación de paquete único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331ab64623a894082c06613db625c6fb568faf9eb16d67af995b89aee9bdfbff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628245"
---
# <a name="single-package-authoring-example"></a>Ejemplo de creación de paquete único

El ejemplo PUASample.msi es un ejemplo de un paquete de Windows Installer 5.0 de doble propósito que es capaz [](installation-context.md) de instalarse en el contexto de instalación por usuario o por máquina en Windows Server 2008 R2 y Windows 7. Este paquete de ejemplo sigue las directrices de desarrollo descritas en [Creación de paquete único.](single-package-authoring.md)

## <a name="obtaining-a-copy-of-the-sample"></a>Obtención de una copia del ejemplo

Una copia de este ejemplo y un editor de tablas de base de datos Windows Installer, Orca.exe, se encuentran en los componentes del SDK de Windows para desarrolladores [Windows Installer](platform-sdk-components-for-windows-installer-developers.md). El ejemplo y el editor de tablas se proporcionan con el Kit de desarrollo de software de Windows para Windows Server 2008 R2 y Windows 7 como archivos de instalación del instalador de Windows PUASample1.msi y Orca.msi.

## <a name="system-requirements"></a>Requisitos del sistema

El editor de bases de datos, [Orca.exe](orca-exe.md), requiere Windows Server 2008 R2 y versiones anteriores y Windows 7 y versiones anteriores. El paquete de doble propósito, PUASample1.msi, se puede instalar en el [](installation-context.md) contexto de instalación por equipo o por usuario en Windows Server 2008 R2 y Windows 7. PUASample1.msi se puede instalar solo en el contexto por equipo en Windows Server 2008 y versiones anteriores y Windows Vista y versiones anteriores. Puede instalar el editor de bases de datos para examinar el contenido de PUASample1.msi sin instalar el ejemplo. Para instalar los paquetes de ejemplo o editor, asegúrese de que la directiva [DisableMSI](disablemsi.md) no esté establecida en un valor que bloquee las instalaciones de aplicaciones.

## <a name="identifying-a-dual-purpose-package"></a>Identificación de un Dual-Purpose paquete

Los paquetes de doble propósito deben inicializar el valor de la [**propiedad MSIINSTALLPERUSER**](msiinstallperuser.md) en 1. Esto identifica el paquete como capaz de instalarse en el contexto por equipo o por usuario en Windows Server 2008 R2 y Windows 7. Establezca la propiedad **MSIINSTALLPERUSER** en el paquete solo si se [](single-package-authoring.md) ha escrito siguiendo las instrucciones de desarrollo descritas en Creación de paquete único y si piensa proporcionar a los usuarios la opción de instalar el paquete en el contexto por usuario o por equipo. Un paquete de doble propósito también debe inicializar el valor de la [**propiedad ALLUSERS**](allusers.md) en 2. Esto especifica por usuario como contexto de instalación predeterminado para la aplicación. Si el valor de la **propiedad ALLUSERS** es cualquier valor distinto de 2, Windows Installer omite la **propiedad MSIINSTALLPERUSER.**

Use un editor Windows base de datos del instalador de archivos, [comoOrca.exe](orca-exe.md), para examinar el contenido de PUASample1.msi. La [tabla Property](property-table.md) del paquete de ejemplo contiene las dos entradas siguientes.

[Propiedad](property-table.md) Tabla (parcial)

| Propiedad          | Value |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>Cuadro de diálogo personalizado para el contexto de instalación

La [](user-interface.md) interfaz de usuario del paquete de ejemplo incluye un ejemplo de un cuadro de diálogo personalizado, VerifyReadyDialog, que permite a los usuarios seleccionar el contexto de instalación por usuario o por equipo en el momento de la instalación. La [tabla Dialog](dialog-table.md) contiene un registro que describe el cuadro de diálogo VerifyReadyDialog. El valor especificado en el campo Atributos es 39 porque este cuadro de diálogo usa los bits de estilo de diálogo msidbDialogAttributesVisible (1), msidbDialogAttributesModal [](dialog-style-bits.md)(2), msidbDialogAttributesMinimize (4) y msidbDialogAttributesTrackDiskSpace (32). La barra de título del cuadro de diálogo muestra un título dado por el valor de la [**propiedad ProductName.**](productname.md)

[Cuadro de diálogo](dialog-table.md) Tabla (parcial) 

| Diálogo            | HCentering | VCentering | Ancho | Alto | Atributos | Título           | Control \_ First | Control \_ predeterminado | Cancelar \_ control |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | Siguientes             | Cancelar          |



 

La [tabla Control](control-table.md) contiene entradas para los [controles](controls.md) mostrados por el cuadro de diálogo VerifyReadyDialog . El cuadro de diálogo muestra [controles PushButton](pushbutton-control.md) y un [control Text.](text-control.md) Todos los controles usan los atributos de [control](control-attributes.md)msidbControlAttributesEnabled (2) y msidbControlAttributesVisible (1). El control InstallPerMachine también usa el atributo de control [ElevationShield,](elevationshield-attribute.md) msidbControlAttributesExiaShield (8388608). Este atributo de [](u-gly.md) control agrega el icono de elevación control de cuentas de usuario (UAC) (icono de escudo) al control InstallPerMachine e informa al usuario de que se necesitan credenciales de UAC para instalar la aplicación en el contexto por equipo. El valor del campo Texto de la tabla Control es el estilo de texto y el texto que muestra el control. Vea la descripción del campo Texto del tema Tabla de control para obtener más información sobre cómo agregar texto a un control mediante estilos predefinidos.

[Control](control-table.md) Tabla (parcial)

| Diálogo\_          | Control           | Tipo       | Atributo | Texto                                                   | Control \_ Siguiente     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | Cancelar            | Pulsador | 3         | { \\ Canceloma10}&Cancel                                    | Siguientes              |
| VerifyReadyDialog | Anterior          | Pulsador | 3         | { \\ Taoma10}<<&Anterior                          | Cancelar            |
| VerifyReadyDialog | Siguientes              | Pulsador | 3         | { \\ Perooma10}&Siguiente >>                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Texto       | 3         | ¿Está listo para completar la instalación suspendida? |                   |
| VerifyReadyDialog | InstallPerUser    | Pulsador | 3         | { \\ Taoma10}Instalar solo para &Me                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | Pulsador | 8388611   | \\{Menteoma10}Instalar para &todos                      | Anterior          |
| VerifyReadyDialog | Cancelar            | Pulsador | 3         | { \\ Canceloma10}&Cancel                                    | Siguientes              |



 

La [tabla ControlEvent](controlevent-table.md) especifica las acciones [ControlEvents](control-events.md)o , que el instalador realiza cuando el usuario interactúa con un control . Cuando un usuario activa el botón de inserción InstallPerUser, la interfaz de usuario muestra un cuadro de diálogo OutOfDisk si la propiedad [**OutOfDiskSpace**](outofdiskspace.md) es 1, establece el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) en 1, establece el valor de la propiedad [**ALLUSERS**](allusers.md) en 2, establece la propiedad [**MSIFASTINSTALL**](msifastinstall.md) en 1 y devuelve . Dado que se establece la propiedad **MSIFASTINSTALL,** no Restaurar sistema punto de conexión para la instalación. Cuando un usuario activa el botón de inserción InstallPerMachine, la interfaz de usuario muestra un cuadro de diálogo OutOfDisk si la propiedad **OutOfDiskSpace** es 1, establece el valor de la propiedad **ALLUSERS** en 1 y devuelve.

[ControlEvent](controlevent-table.md) Tabla (parcial) 

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



 

El control InstallPerUser debe quitarse de la interfaz de usuario de cualquier instalación mediante una versión del instalador de Windows anterior a Windows Installer Windows Installer 5.0. La [tabla ControlCondition](controlcondition-table.md) del paquete de ejemplo contiene cuatro entradas que deshabilitan y ocultan el control InstallPerUser si la versión actual es menor que Windows Installer 5.0. La tabla usa el valor de la [**propiedad VersionMsi**](versionmsi.md) y la sintaxis [de la instrucción condicional](conditional-statement-syntax.md) para definir esta condición. La acción especificada en el campo Acción solo se realiza si la instrucción del campo Condición es true.

[ControlCondition](controlcondition-table.md) Tabla (parcial)

| Diálogo\_          | control\_      | Acción  | Condición               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | Habilitar  | VersionMsi >= "5.00" |
| VerifyReadyDialog | InstallPerUser | Deshabilitar | VersionMsi < "5.00"  |
| VerifyReadyDialog | InstallPerUser | Mostrar    | VersionMsi >= "5.00" |
| VerifyReadyDialog | InstallPerUser | Ocultar    | VersionMsi < "5.00"  |



 

## <a name="specifying-directory-structure"></a>Especificar la estructura de directorios

Use el editor de bases de datos para examinar la [tabla Directory](directory-table.md) de PUASample1.msi. El registro de la tabla de directorios que tiene una cadena vacía en su campo Primario de directorio representa el directorio raíz de los árboles de directorio de origen \_ y de destino. Si la [**propiedad TARGETDIR**](targetdir.md) no está definida, el instalador establece su valor en el momento de la instalación en el valor de la [**propiedad ROOTDRIVE.**](rootdrive.md) Si la [**propiedad SourceDir**](sourcedir.md) no está definida, el instalador establece su valor en la ubicación del directorio que contiene el paquete Windows Installer (.msi archivo). Los nombres de directorio se especifican con el formato \| largo corto.

[Directorio](directory-table.md) Tabla (parcial)

| Directorio          | Elemento primario \_ del directorio  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | MyVendor           | Ejemplo1 \| MSDN-PUASample1 |
| MyVendor           | ProgramFilesFolder | Msft \| Microsoft          |



 

En el origen, esta tabla [Directory](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio.

<dl> \[SourceDir \] \\ Msft \\ Sample1  
\[SourceDir\]  
</dl>

En el destino, la [tabla Directory](directory-table.md) se resuelve en las rutas de acceso de la tabla siguiente. El instalador establece los valores de las propiedades [**ProgramFilesFolder**](programfilesfolder.md) y [](installation-context.md) [**ProgramMenuFolder**](programmenufolder.md) en ubicaciones que dependen del contexto de instalación y si el sistema es las versiones de 32 o 64 bits de Windows Server 2008 R2 y Windows 7. Las rutas de acceso a las carpetas de destino dependen de si el usuario selecciona una instalación por usuario o por equipo.

| Contexto de instalación | Sistema                                                                              | Rutas de acceso de ejemplo                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> Versión de 32 bits<br/>           | %ProgramFiles% \\ Msft \\ Sample1<br/> %ALLUSERSPROFILE% \\ Programas de menú Inicio Windows \\ \\ Microsoft \\<br/>                  |
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> Versión de 64 bits<br/>           | %ProgramFiles(x86)% \\ Msft \\ Sample1<br/> %ALLUSERSPROFILE% \\ Programas de menú Inicio Windows \\ \\ Microsoft \\<br/>             |
| Per-User             | Windows Server 2008 R2 y Windows 7<br/> Versión de 32 o 64 bits<br/> | %USERPROFILE% \\ AppData \\ Local Programs \\ \\ Msft \\ Sample1<br/> %APPDATA% \\ Programas del menú Inicio Windows \\ \\ Microsoft \\<br/> |



 

Las aplicaciones por usuario deben almacenarse en subcarpetas en la carpeta Programas especificada por el valor de [**la propiedad ProgramFilesFolder.**](programfilesfolder.md) Normalmente, la ruta de acceso a la aplicación tiene la forma siguiente.

%LOCALAPPDATA% \\ Programas Nombre de \\ *ISV* \\ *AppName*.

Los datos de configuración por usuario deben almacenarse en la carpeta Programas especificada por el valor de la [**propiedad ProgramMenuFolder.**](programmenufolder.md) Normalmente, esta carpeta se encuentra en la ruta de acceso siguiente.

%APPDATA% \\ Programas del menú Inicio Windows \\ \\ Microsoft \\

Si instala componentes de paquete de Windows instalador de [32](32-bit-windows-installer-packages.md) bits, use la propiedad [**ProgramFilesFolder**](programfilesfolder.md) y [**CommonFilesFolder**](commonfilesfolder.md) en la [tabla Directory.](directory-table.md) Si instala componentes de paquete Windows instalador de [64](64-bit-windows-installer-packages.md) bits, use las propiedades [**ProgramFiles64Folder**](programfiles64folder.md) y [**CommonFiles64Folder.**](commonfiles64folder.md) Si la aplicación contiene versiones de 32 y 64 bits del mismo componente, con el mismo nombre, asegúrese de que estas versiones se guardan en directorios diferentes o de darles nombres diferentes.

En la [tabla Directorio](directory-table.md) siguiente se proporciona un ejemplo de un diseño de directorio compatible con un paquete que incluye componentes de 32 y 64 bits e incluye algunos componentes que se comparten entre aplicaciones.

| Directorio            | Elemento primario \_ del directorio    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | .:Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | MyVendor             | Ejemplo1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Ejemplo1 \| MSDN-PUASample1          |
| SHAREDLOCATION       | ShVendor             | Ejemplo1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Ejemplo1 \| MSDN-PUASample1          |
| MyVendor             | ProgramFilesFolder   | Msft \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | Msft \| Microsoft                   |
| ShVendor             | CommonFilesFolder    | Msft \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | Msft \| Microsoft                   |
| Shrx86               | SHAREDLOCATION       | Componentes x32 \| de 32 bits            |
| Shrx64               | SHAREDLOCATIONX64    | Componentes x64 \| de 64 bits            |
| Binx86               | INSTALLLOCATION      | Componentes x32 \| de 32 bits            |
| Binx64               | INSTALLLOCATIONX64   | Componentes x64 \| de 64 bits            |
| App32                | Binx86               | componentes \| de 32 bits no compartidos de myapp |
| App64                | Binx64               | componentes de 64 bits no compartidos de \| myapp |
| Share32              | Shrx86               | componentes \| compartidos de 32 bits compartidos  |
| Share64              | Shrx64               | componentes \| compartidos de 64 bits compartidos  |



 

En el origen, esta tabla [Directory](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio.

<dl> \[SourceDir \] Prog32 \\ Msft \\ Sample1 \\ x32 \\ myapp  
\[SourceDir \] Share32 \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared  
\[SourceDir \] Prog64 \\ Msft \\ Sample1 \\ x64 \\ myapp  
\[SourceDir \] Share64 \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared  
\[SourceDir \] Sample1  
</dl>

En el destino, esta [tabla Directory](directory-table.md) se resuelve en las siguientes rutas de acceso de directorio. Las rutas de acceso de destino dependen del [sistema y el contexto](installation-context.md) de instalación.

| Contexto de instalación | Sistema                                                                              | Rutas de acceso de ejemplo                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> Versión de 32 bits<br/>           | %ProgramFiles% \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> %ProgramFiles% \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared<br/> %ProgramFiles(x86)% \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> %ProgramFiles(x86)% \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared<br/> %ProgramData% \\ Microsoft Windows Ejemplo de programas del menú \\ \\ \\ \\ Inicio1<br/>               |
| Per-Machine          | Windows Server 2008 R2 y Windows 7<br/> Versión de 64 bits<br/>           | %ProgramFiles(x86)% \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> %ProgramFiles(x86)% \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared<br/> %ProgramFiles% \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> %ProgramFiles% \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared<br/> %ProgramData% \\ Microsoft Windows Ejemplo de programas del menú \\ \\ \\ \\ Inicio1<br/>               |
| Per-User             | Windows Server 2008 R2 y Windows 7<br/> Versión de 32 o 64 bits<br/> | %LOCALAPPDATA% \\ Programas \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> %LOCALAPPDATA% \\ Programas comunes \\ \\ msft \\ sample1 \\ x32 \\ compartidos<br/> %LOCALAPPDATA% \\ Programas \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> %LOCALAPPDATA% \\ Programas \\ comunes \\ Msft \\ Sample1 \\ x64 \\ compartidos<br/> %APPDATA% \\ Microsoft Windows Ejemplo de programas de menú \\ \\ \\ \\ Inicio1<br/> |



 

## <a name="application-registration"></a>Registro de la aplicación

El PUASample.msi agrega una subclave a la clave del Registro rutas de acceso de la aplicación para la aplicación y realiza registros que permiten guardar la información de la aplicación en el Registro bajo esta clave. Para obtener más información sobre las rutas de acceso de la aplicación y el registro de aplicaciones, vea [PerceivedTypes, SystemFileAssociations](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)) y Application Registration en la sección [extensibilidad](https://msdn.microsoft.com/library/bb762762.aspx) del shell de la Guía del desarrollador [de Shell.](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) En el momento de la instalación, el usuario toma la decisión de instalar la aplicación en el contexto de instalación por usuario o por equipo. En el momento de crear el paquete de doble propósito, el desarrollador del paquete no puede saber si los registros deben realizarse en las claves HKEY LOCAL MACHINE o \_ \_ HKEY \_ CURRENT \_ USER.

El desarrollador del paquete define el identificador de archivo para el archivo ejecutable de la aplicación en el campo Archivo de la [tabla de](file-table.md) archivos.

[Archivo](file-table.md) Tabla (parcial) 

| Archivo      | Componente\_      | FileName                     | FileSize | Versión | Lenguaje | Atributos | Secuencia |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppFile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

Los valores que se guardarán en el Registro se pueden especificar en el campo Valor de la tabla [Registro](registry-table.md) como [una cadena con](formatted.md) formato. Use el identificador de archivo definido [](file-table.md) en el campo Archivo de la tabla Archivo y la convención filekey del tipo Formatted para especificar el valor predeterminado de la clave del Registro \[ \#  \] rutas de acceso de aplicación. La acción [INSTALL de nivel](install-action.md) superior realiza las acciones de la [tabla InstallExecuteSequence.](installexecutesequence-table.md) Una vez completadas las acciones [CostInitialize,](costinitialize-action.md) [FileCost](filecost-action.md)e [InstallFinalize](installfinalize-action.md) de esta tabla, el instalador de Windows reemplaza la subcadena con formato \[ \# MyAppFile de la tabla del Registro por la ruta de acceso completa al archivo de \] aplicación.

El ejemplo define una propiedad personalizada, RegRoot, para contener la ubicación de la clave raíz y usa una acción personalizada para restablecer el valor de propiedad si el usuario elige una instalación por equipo. Use la propiedad personalizada RegRoot en cualquier valor de cadena con formato que haga referencia a la ubicación raíz. En la [tabla Property](property-table.md) , PUASample.msi paquete define la propiedad personalizada y establece el valor de RegRoot en HKCU. Esto inicializa el valor de la propiedad para el contexto de instalación por usuario, el contexto predeterminado recomendado para paquetes de doble propósito.

[Propiedad](property-table.md) Tabla (parcial)

| Propiedad | Value |
|----------|-------|
| RegRoot  | HKCU  |



 

En la [tabla CustomAction,](customaction-table.md) el paquete define una acción personalizada denominada Set \_ RegRoot \_ HKLM. El valor del campo Tipo lo identifica como una acción personalizada estándar de tipo de acción [personalizada 51.](custom-action-type-51.md) El significado de los campos Origen y Destino de la tabla CustomAction depende del tipo de acción personalizada. Para obtener más información sobre los tipos estándar de acciones personalizadas, vea [Custom Action Types](summary-list-of-all-custom-action-types.md). El campo Source de la \_ acción personalizada Set RegRoot \_ HKLM especifica que el valor de la propiedad RegRoot. Si el instalador realiza la acción personalizada Set RegRoot HKLM, se restablece el valor de la \_ \_ propiedad RegRoot a HKLM.

[CustomAction](customaction-table.md) Tabla (parcial)

| Acción             | Tipo | Source      | Destino |
|--------------------|------|-------------|--------|
| Establecer \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

La acción [INSTALL](install-action.md) de nivel superior realiza las acciones de la tabla [InstallExecuteSequence,](installexecutesequence-table.md) en la secuencia especificada en el campo Secuencia de esa tabla. El valor que se crea en el campo Secuencia para la acción personalizada Set RegRoot HKLM (1501) especifica que esta acción personalizada se realice después de la acción \_ \_ [InstallInitialize](installinitialize-action.md) (1500) y antes de la acción [ProcessComponents](processcomponents-action.md) (1600). Esta secuencia garantiza que el registro de la acción personalizada Set \_ RegRoot \_ HKLM se evalúa en el momento de la instalación. Para obtener más información sobre la secuencia recomendada de acciones en la tabla InstallExecuteSequence, vea el tema [Suggested InstallExecuteSequence](suggested-installexecutesequence.md) . La [](conditional-statement-syntax.md) sintaxis de instrucción condicional que se ha escrito en el campo Condición especifica que la acción Set RegRoot HKLM solo se realice si el valor de la propiedad \_ \_ [**ALLUSERS**](allusers.md) se evalúa como 1 en el momento de la instalación. Un **valor de propiedad ALLUSERS** de 1 especifica una instalación por máquina.

[InstallExecuteSequence](installexecutesequence-table.md) Tabla (parcial)

| Acción             | Condición  | Secuencia |
|--------------------|------------|----------|
| Establecer \_ RegRoot \_ HKLM | ALLUSERS=1 | 1501     |



 

Los siguientes registros de la [tabla Registro](registry-table.md) realizan los registros si está instalado el componente ProductComponent. El valor -1 del campo Raíz es necesario para realizar el registro en HKEY LOCAL MACHINE para una instalación por usuario y en HKEY CURRENT USER para una instalación por \_ \_ \_ \_ usuario. El registro con una cadena vacía en el campo Registro agrega una subclave para la aplicación en la clave del Registro AppPaths y establece el valor "(Default)" en la ruta de acceso completa del archivo ejecutable de la aplicación. El registro MyAppPathAlias asigna el archivo ejecutable a un alias de aplicación y permite iniciar la aplicación si el usuario le asigna el alias "puapct" en un símbolo del sistema. El registro MyAppPathRegistration asigna el nombre del archivo ejecutable a la ruta de acceso completa del archivo.



| Registro              | Root | Clave                                                                     | Nombre | Value                                                                            | Componente        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | Software \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[Rutas de acceso de \] \\ la aplicación \\ \\ \\ CurrentVersion de Microsoft Windows \\ \\ RegRoot SoftwarePUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | Software \\ Microsoft Windows \\ \\ rutas de acceso de la aplicación CurrentVersion \\ \\PUAPCT.exe     |      | \[\#MyAppFile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | Software \\ Microsoft Windows \\ \\ rutas de acceso de la aplicación CurrentVersion \\ \\PUASample1.exe |      | \[\#MyAppFile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>Cancelación del registro de reproducción automática

El PUASample.msi realiza registros que permiten al usuario de la aplicación impedir que la reproducción automática de [hardware](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) se inicie para los dispositivos seleccionados. Para obtener información sobre cómo registrar un controlador para cancelar la reproducción automática en respuesta a un evento, vea el tema [Preparing Hardware and Software for Use with AutoPlay](/previous-versions//cc144208(v=vs.85)) (Preparar hardware y software para su uso con Reproducción automática) en la sección [extensibilidad](https://msdn.microsoft.com/library/bb762762.aspx) del shell de la Guía del desarrollador de [Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). El registro siguiente registra el controlador especificado en el campo Nombre cuando se instala el componente ProductComponent. El valor -1 del campo Raíz es necesario para especificar al instalador de Windows que el registro se debe redirigir a una ubicación que dependa del contexto de instalación.

[Registro](registry-table.md) Mesa 

| Registro                     | Root | Clave                                                                                             | Nombre                                 | Value | Componente        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ CancelAutoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>Registro del controlador de vista previa

El PUASample.msi realiza los registros necesarios para instalar [](../shell/preview-handlers.md) un controlador de versión preliminar que permite una vista previa de solo lectura de archivos .pua sin iniciar la aplicación. Para obtener información sobre el registro de controladores de versión preliminar, vea el tema [Registro](../shell/how-to-register-a-preview-handler.md) de controladores de vista previa en la sección [extensibilidad](https://msdn.microsoft.com/library/bb762762.aspx) del shell de la Guía del desarrollador [de Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)). Los registros siguientes de la [tabla Registro](registry-table.md) registran el controlador cuando se instala el componente ProductComponent. El valor -1 del campo Raíz es necesario para especificar al instalador de Windows que el registro se debe redirigir a una ubicación que dependa del contexto de instalación.

[Registro](registry-table.md) Mesa

| Registro                       | Root | Clave                                                                              | Nombre                                   | Value                                        | Componente        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | Clases de software \\ \\ .pua                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ \\ PreviewHandlers de CurrentVersion                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Controlador de versión preliminar Windows PRUEBA PUA de Microsoft   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | Clases \\ de \\ software puafile \\ ShellEx \\ {8895b1c6-b41f-4c1c-a562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Per-User controlador de vista previa del ejemplo 1 de Applicaton | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32,-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | Icono                                   | notepad.exe,2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ThreadingModel                         | Apartamento                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 |                                        | \#%%SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | Clases de software \\ \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 

---
description: Un objeto de controlador de extensión de Shell debe registrarse antes de que el shell pueda usarlo. Este tema es una discusión general sobre cómo registrar un controlador de extensión de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrando controladores de extensión de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985762"
---
# <a name="registering-shell-extension-handlers"></a>Registrando controladores de extensión de Shell

Un objeto de controlador de extensión de Shell debe registrarse antes de que el shell pueda usarlo. Este tema es una discusión general sobre cómo registrar un controlador de extensión de Shell.

Cada vez que crea o cambia un controlador de extensión de Shell, es importante notificar al sistema que ha realizado un cambio. Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el evento **\_ ASSOCCHANGED de SHCNE** . Si no llama a **SHChangeNotify**, es posible que no se reconozca el cambio hasta que se reinicie el sistema.

Hay algunos factores adicionales que se aplican a los sistemas 2000 de Windows. Para obtener más información, consulte la sección [registro de controladores de extensión de Shell en Windows 2000 Systems](#registering-shell-extension-handlers) .

Al igual que con todos los objetos del modelo de objetos componentes (COM), debe crear un GUID para el controlador mediante una herramienta como Guidgen.exe, que se proporciona con el kit de desarrollo de software (SDK) de Windows. Cree una subclave en **HKEY \_ classes \_ raíz** \\ **CLSID** cuyo nombre es la forma de cadena de ese GUID. Dado que los controladores de la extensión de Shell son servidores en proceso, también debe crear una subclave **InProcServer32** en esa subclave GUID con el valor (predeterminado) establecido en la ruta de acceso de la dll del controlador. Use el modelo de subprocesos de apartamento. A continuación, se muestra un ejemplo:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Cada vez que el shell realiza una acción que puede incluir un controlador de extensión de Shell, comprueba la subclave del registro adecuada. La subclave bajo la que un controlador de extensión registra los controles cuando se llama. Por ejemplo, es una práctica común tener un controlador de menú contextual llamado cuando el shell muestra un menú contextual para un miembro de un [tipo de archivo](fa-file-types.md). En este caso, el controlador se debe registrar en la subclave **ProgID** del tipo de archivo.

En este tema se tratan los siguientes temas:

-   [Nombres de controlador](#handler-names)
-   [Objetos de Shell predefinidos](#predefined-shell-objects)
-   [Ejemplo de registro de un controlador de extensión](#example-of-an-extension-handler-registration)
    -   [Registrando controladores de extensión de Shell](#registering-shell-extension-handlers)
-   [Temas relacionados](#related-topics)

## <a name="handler-names"></a>Nombres de controlador

Para habilitar un controlador de extensión de Shell, cree una subclave con el nombre de la subclave del controlador (consulte a continuación) en la subclave **ShellEx** del **ProgID** (para tipos de archivo) o el nombre del tipo de objeto de Shell (para [ \_ \_ objetos de Shell predefinidos](handlers.md)).

Por ejemplo, si desea registrar un controlador de extensión de menú contextual para el programa. 1, empiece por crear la siguiente subclave:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

En el caso de los siguientes controladores, cree una subclave debajo de la subclave "Handlet subclave name" denominada como la versión de cadena del identificador de clase (CLSID) de la extensión de Shell. Se pueden registrar varias extensiones en el nombre de la subclave del controlador mediante la creación de varias subclaves.



| Controlador                 | Interfaz          | Nombre de la subclave del controlador       |
|-------------------------|--------------------|---------------------------|
| Controlador de proveedor de columnas | IColumnProvider    | **ColumnHandlers**        |
| Controlador del menú contextual   | IContextMenu       | **ContextMenuHandlers**   |
| Controlador Copyhook        | ICopyHook          | **CopyHookHandlers**      |
| Controlador de arrastrar y colocar   | IContextMenu       | **DragDropHandlers**      |
| Controlador de la hoja de propiedades  | IShellPropSheetExt | **PropertySheetHandlers** |



 

En el caso de los siguientes controladores, el valor predeterminado de la clave "nombre de subclave de controlador" es la versión de cadena del CLSID de la extensión de Shell. Solo se puede registrar una extensión para estos controladores.



| Controlador                 | Interfaz            | Nombre de la subclave del controlador                        |
|-------------------------|----------------------|--------------------------------------------|
| Controlador de datos            | IDataObject          | **DataHandler**                            |
| Quitar controlador            | IDropTarget          | **DropHandler**                            |
| Controlador de iconos            | IExtractIconA/W      | **IconHandler**                            |
| Controlador de imagen en miniatura | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Controlador de recuadro informativo         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
| Vínculo de Shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Vínculo de Shell (Unicode)    | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| Almacenamiento estructurado      | IStorage             | **{0000000B-0000-0000-C000-000000000046}** |
| Metadatos                | IPropertySetStorage  | **PropertyHandler**                        |
| Anclar al menú Inicio       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Anclar a la barra de tareas          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Las subclaves especificadas para agregar **anclar al menú Inicio** y **anclar a la barra de tareas** al menú contextual de un elemento solo son necesarias para los tipos de archivo que incluyen la entrada [IsShortCut](./links.md) .

## <a name="predefined-shell-objects"></a>Objetos de Shell predefinidos

El shell define objetos adicionales en **la \_ \_ raíz de las clases HKEY** que se pueden extender de la misma manera que los tipos de archivo. Por ejemplo, para agregar un controlador de hoja de propiedades para todos los archivos, puede registrarse en la subclave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

En la tabla siguiente se proporcionan las diversas subclaves de **\_ las clases HKEY \_ raíz** en las que se pueden registrar controladores de extensión. Tenga en cuenta que muchos controladores de extensión no se pueden registrar en todas las subclaves de la lista. Para obtener más información, vea la documentación del controlador específico.



| Subclave                    | Descripción                                                          | Controladores posibles                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\** _                    | Todos los archivos                                                            | Menú contextual, hoja de propiedades, verbos (ver más abajo) |
| _ *AllFileSystemObjects**  | Todos los archivos y carpetas de archivos                                           | Menú contextual, hoja de propiedades, verbos             |
| **Carpeta**                | Todas las carpetas                                                          | Menú contextual, hoja de propiedades, verbos             |
| **Directorio**             | Carpetas de archivos                                                         | Menú contextual, hoja de propiedades, verbos             |
| **Fondo de directorio \\** | Fondo de carpeta de archivos                                               | Solo el menú contextual                               |
| **DesktopBackground**     | Fondo de escritorio (Windows 7 y versiones posteriores)                            | Menú contextual, verbos                             |
| **Unidad**                 | Todas las unidades de mi PC, como "C: \\ "                             | Menú contextual, hoja de propiedades, verbos             |
| **Network**               | Red completa (en mis sitios de red)                             | Menú contextual, hoja de propiedades, verbos             |
| **Tipo de red \\\\\#**     | Todos los objetos de tipo \# (ver más abajo)                                   | Menú contextual, hoja de propiedades, verbos             |
| **NetShare**              | Todos los recursos compartidos de red                                                   | Menú contextual, hoja de propiedades, verbos             |
| **NetServer**             | Todos los servidores de red                                                  | Menú contextual, hoja de propiedades, verbos             |
| *\_nombre del proveedor de red \_* | Todos los objetos proporcionados por el proveedor de red "*\_ \_ nombre de proveedor de red*" | Menú contextual, hoja de propiedades, verbos             |
| **Impresoras**              | Todas las impresoras                                                         | Menú contextual, hoja de propiedades                    |
| **Audio**               | CD de audio en la unidad de CD                                                 | Solo verbos                                       |
| **DISCOS**                   | Unidad de DVD (Windows 2000)                                             | Menú contextual, hoja de propiedades, verbos             |



 

### <a name="notes"></a>Notas

-   Para acceder al menú contextual de fondo de la carpeta de archivos, haga clic con el botón secundario en una carpeta de archivos, pero no en el contenido de la carpeta.
-   Los "verbos" son comandos especiales registrados en el verbo de Shell de la subclave **\_ \_ raíz de las clases HKEY** \\  \\  \\ .
-   Para el tipo de **red** \\  \\ **\#** , " \# " es un código de tipo de proveedor de red en formato decimal. El código de tipo de proveedor de red es la palabra alta de un tipo de red. La lista de tipos de red se proporciona en el archivo de encabezado Winnetwk. h ( \_ valores de net WNNC \_ \* ). Por ejemplo, WNNC \_ net \_ Shiva es 0x00330000, por lo que la subclave de tipo correspondiente sería **HKEY \_ classes \_ root** \\ **Network** \\ **Type** \\ **51**.
-   "*\_ \_ nombre de proveedor de red*" es un nombre de proveedor de red tal y como lo especifica [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con los espacios convertidos en guiones bajos. Por ejemplo, si se instala el proveedor de red de redes de Microsoft, su nombre de proveedor es "red de Microsoft Windows" y el *\_ \_ nombre de proveedor de red* correspondiente es **\_ \_ red de Microsoft Windows**.

## <a name="example-of-an-extension-handler-registration"></a>Ejemplo de registro de un controlador de extensión

Para habilitar un controlador determinado, cree una subclave en la subclave de tipo de controlador de extensión con el nombre del controlador. El shell no utiliza el nombre del controlador, pero debe ser diferente de todos los demás nombres bajo esa subclave de tipo. Establezca el valor predeterminado de la subclave Name en la forma de cadena del GUID del controlador.

En el ejemplo siguiente se muestran las entradas del registro que habilitan los controladores de extensiones de menús contextuales y hojas de propiedades mediante un tipo de archivo. MYP de ejemplo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>Registrando controladores de extensión de Shell

El procedimiento de registro descrito en esta sección debe seguirse para todos los sistemas de Windows. Sin embargo, con los sistemas posteriores, podría ser necesario un paso adicional. Dado que estas versiones posteriores de Windows están diseñadas para usarse en un entorno administrado, el acceso al registro se puede restringir administrativamente, lo que requiere un enfoque algo diferente de la instalación que se describe en la sección anterior.

> [!Note]  
> Los programas de instalación no suelen escribir directamente en el registro. En su lugar, el programa de instalación debe realizarse con Windows Installer paquetes. Estas herramientas garantizan que el software se ejecute correctamente y proporcione acceso a funcionalidades como el registro de clases por usuario.

 

Los controladores de extensión de Shell se ejecutan en el proceso de Shell. Dado que se trata de un proceso del sistema, el administrador de un sistema puede limitar los controladores de extensión de Shell a los de una lista aprobada estableciendo el valor de EnforceShellExtensionSecurity de la clave del **Explorador** en 1, como se muestra aquí:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

Para colocar un controlador de extensión de Shell en la lista aprobada, cree un valor de **reg \_ SZ** cuyo nombre sea la forma de cadena del GUID del controlador en la subclave **aprobada** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Por ejemplo, en el ejemplo siguiente se agregan los controladores de *comandos* y *MyPropSheet* a la lista aprobada.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

El shell no utiliza el valor asignado al GUID, pero debe establecerse para facilitar la inspección del registro.

La aplicación de instalación puede agregar valores a la subclave **aprobada** solo si la persona que instala la aplicación tiene privilegios suficientes. Si se produce un error al intentar agregar un controlador de extensión, debe informar al usuario de que se necesitan privilegios administrativos para instalar completamente la aplicación. Si el controlador es esencial para la aplicación, se debe producir un error en la instalación y notificar al usuario que se ponga en contacto con un administrador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicializar controladores de extensión de Shell](int-shell-exts.md)
</dt> </dl>

 

 

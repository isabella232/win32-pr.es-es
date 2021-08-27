---
description: Se debe registrar un objeto de controlador de extensión de Shell para poder usarlo. Este tema es una explicación general de cómo registrar un controlador de extensión de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registro de controladores de extensión de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111215"
---
# <a name="registering-shell-extension-handlers"></a>Registro de controladores de extensión de shell

Se debe registrar un objeto de controlador de extensión de Shell para poder usarlo. Este tema es una explicación general de cómo registrar un controlador de extensión de Shell.

Cada vez que cree o cambie un controlador de extensión de Shell, es importante notificar al sistema que ha realizado un cambio. Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)y especifique el evento **\_ ASSOCCHANGED de SHCNE.** Si no llama a **SHChangeNotify,** es posible que el cambio no se reconozca hasta que se reinicie el sistema.

Hay algunos factores adicionales que se aplican a Windows 2000 sistemas. Para obtener más información, vea [la sección Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) (Registro de controladores de extensión de shell Windows 2000 Systems).

Al igual que con todos los objetos del modelo de objetos componentes (COM), debe crear un GUID para el controlador mediante una herramienta como Guidgen.exe, que se proporciona con el Kit de desarrollo de software (SDK) de Windows. Cree una subclave en **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** cuyo nombre es la forma de cadena de ese GUID. Dado que los controladores de extensión de Shell son servidores en proceso, también debe crear una subclave **InprocServer32** en esa subclave GUID con el valor (Predeterminado) establecido en la ruta de acceso del archivo DLL del controlador. Use el modelo de subprocesamiento de apartamento. A continuación, se muestra un ejemplo:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Cada vez que el Shell realiza una acción que puede implicar un controlador de extensión de Shell, comprueba la subclave del Registro adecuada. La subclave con la que se registra un controlador de extensión controla cuándo se llamará. Por ejemplo, es una práctica habitual que se llame a un controlador de menú contextual cuando el Shell muestra un menú contextual para un miembro de un [tipo de archivo](fa-file-types.md). En este caso, el controlador debe registrarse en la subclave **ProgID** del tipo de archivo.

En este tema se de abordan los siguientes temas:

-   [Nombres de controlador](#handler-names)
-   [Objetos de shell predefinidos](#predefined-shell-objects)
-   [Ejemplo de un registro de controlador de extensión](#example-of-an-extension-handler-registration)
    -   [Registro de controladores de extensión de shell](#registering-shell-extension-handlers)
-   [Temas relacionados](#related-topics)

## <a name="handler-names"></a>Nombres de controlador

Para habilitar un controlador de extensión de Shell, cree una subclave con el nombre de subclave del controlador (consulte a continuación) en la subclave **ShellEx** de **ProgID** (para tipos de archivo) o el nombre del tipo de objeto shell (para objetos de [shell \_ predefinidos). \_](handlers.md)

Por ejemplo, si desea registrar un controlador de extensión de menú contextual para MyProgram.1, empiece por crear la subclave siguiente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Para los siguientes controladores, cree una subclave debajo de la subclave "Nombre de subclave del controlador" denominada como la versión de cadena del identificador de clase (CLSID) de la extensión shell. Se pueden registrar varias extensiones con el nombre de subclave del controlador mediante la creación de varias subclaves.



| Controlador                 | Interfaz          | Nombre de subclave del controlador       |
|-------------------------|--------------------|---------------------------|
| Controlador de proveedor de columnas | IColumnProvider    | **ColumnHandlers**        |
| Controlador de menú contextual   | IContextMenu       | **ContextMenuHandlers**   |
| Controlador de copyhook        | ICopyHook          | **CopyHookHandlers**      |
| Controlador de arrastrar y colocar   | IContextMenu       | **DragDropHandlers**      |
| Controlador de la hoja de propiedades  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Para los siguientes controladores, el valor predeterminado de la clave "Nombre de subclave del controlador" es la versión de cadena del CLSID de la extensión de Shell. Solo se puede registrar una extensión para estos controladores.



| Controlador                 | Interfaz            | Nombre de subclave del controlador                        |
|-------------------------|----------------------|--------------------------------------------|
| Controlador de datos            | IDataObject          | **Datahandler**                            |
| Controlador de colocación            | IDropTarget          | **DropHandler**                            |
| Controlador de iconos            | IExtractIconA/W      | **IconHandler**                            |
| Controlador de imágenes en miniatura | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Controlador de recuadro informativo         | IQueryInfo           | **{00021500-0000-0000-C000-00000000046}** |
| Vínculo de shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-00000000046}** |
| Vínculo de shell (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-00000000046}** |
| Almacenamiento estructurado      | IStorage             | **{0000000B-0000-0000-C000-00000000046}** |
| Metadatos                | IPropertySetStorage  | **PropertyHandler**                        |
| Anclar al menú Inicio       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Anclar a la barra de tareas          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Las subclaves especificadas  para agregar  Anclar al menú Inicio y Anclar a la barra de tareas al menú contextual de un elemento solo son necesarias para los tipos de archivo que incluyen la [entrada IsShortCut.](./links.md)

## <a name="predefined-shell-objects"></a>Objetos de shell predefinidos

El shell define objetos adicionales en **HKEY \_ CLASSES \_ ROOT** que se pueden extender de la misma manera que los tipos de archivo. Por ejemplo, para agregar un controlador de hoja de propiedades para todos los archivos, puede registrarse en la subclave **PropertySheetHandlers.**

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

En la tabla siguiente se ofrecen las distintas subclaves **de HKEY \_ CLASSES \_ ROOT** en las que se pueden registrar controladores de extensión. Tenga en cuenta que muchos controladores de extensión no se pueden registrar en todas las subclaves enumeradas. Para más información, consulte la documentación del controlador específico.



| Subclave                    | Descripción                                                          | Posibles controladores                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | Todos los archivos                                                            | Menú contextual, hoja de propiedades, verbos (vea a continuación) |
| **AllFileSystemObjects**  | Todos los archivos y carpetas de archivos                                           | Menú contextual, hoja de propiedades, verbos             |
| **Carpeta**                | Todas las carpetas                                                          | Menú contextual, hoja de propiedades, verbos             |
| **Directorio**             | Carpetas de archivos                                                         | Menú contextual, hoja de propiedades, verbos             |
| **Fondo del \\ directorio** | Fondo de la carpeta de archivos                                               | Solo menú contextual                               |
| **DesktopBackground**     | Fondo de escritorio (Windows 7 y posteriores)                            | Menú contextual, verbos                             |
| **Unidad**                 | Todas las unidades de MyComputer, como "C: \\ "                             | Menú contextual, hoja de propiedades, verbos             |
| **Red**               | Toda la red (en Mis lugares de red)                             | Menú contextual, hoja de propiedades, verbos             |
| **Tipo de \\ red\\\#**     | Todos los objetos de tipo \# (consulte a continuación)                                   | Menú contextual, hoja de propiedades, verbos             |
| **NetShare**              | Todos los recursos compartidos de red                                                   | Menú contextual, hoja de propiedades, verbos             |
| **Netserver**             | Todos los servidores de red                                                  | Menú contextual, hoja de propiedades, verbos             |
| *nombre \_ del proveedor de \_ red* | Todos los objetos proporcionados por el proveedor de red "*nombre del proveedor de \_ \_ red*" | Menú contextual, hoja de propiedades, verbos             |
| **Impresoras**              | Todas las impresoras                                                         | Menú contextual, Hoja de propiedades                    |
| **AudioCD**               | CD de audio en la unidad de CD                                                 | Solo verbos                                       |
| **Dvd**                   | Unidad de DVD (Windows 2000)                                             | Menú contextual, hoja de propiedades, verbos             |



 

### <a name="notes"></a>Notas

-   Para acceder al menú contextual de fondo de la carpeta de archivos, haga clic con el botón derecho en una carpeta de archivos, pero no sobre el contenido de la carpeta.
-   "Verbos" son comandos especiales registrados en el verbo de shell de subclave **\_ \_ ROOT HKEY CLASSES** \\  \\  \\ .
-   Para **tipo** \\ **de** \\ **\#** red , " " es un código \# de tipo de proveedor de red en decimal. El código de tipo de proveedor de red es la palabra alta de un tipo de red. La lista de tipos de red se muestra en el archivo de encabezado Winnetwk.h (valores de WNNC \_ \_ \* NET). Por ejemplo, WNNC NET 0X00330000, por lo que la subclave de tipo correspondiente sería \_ \_ **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51**.
-   "*network \_ provider \_ name*" es un nombre de proveedor de red especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con los espacios convertidos en caracteres de subrayado. Por ejemplo, si está instalado el proveedor de redes de Microsoft, su nombre de proveedor es "Microsoft Windows Network" y el nombre del proveedor de red correspondiente es **Microsoft \_ Windows \_ Network**. *\_ \_*

## <a name="example-of-an-extension-handler-registration"></a>Ejemplo de un registro de controlador de extensión

Para habilitar un controlador determinado, cree una subclave en el tipo de controlador de extensión subclave con el nombre del controlador. El Shell no usa el nombre del controlador, pero debe ser diferente de todos los demás nombres de esa subclave de tipo. Establezca el valor predeterminado de la subclave name en el formato de cadena del GUID del controlador.

En el ejemplo siguiente se muestran las entradas del Registro que habilitan el menú contextual y los controladores de extensión de la hoja de propiedades, con un tipo de archivo .myp de ejemplo.

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

### <a name="registering-shell-extension-handlers"></a>Registro de controladores de extensión de Shell

El procedimiento de registro descrito en esta sección debe seguirse para todos Windows sistemas. Sin embargo, con sistemas posteriores, podría ser necesario realizar un paso adicional. Dado que estas versiones posteriores de Windows están diseñadas para usarse en un entorno administrado, el acceso al registro podría estar restringido administrativamente, lo que requiere un enfoque ligeramente diferente a la instalación descrito en la sección anterior.

> [!Note]  
> Por lo general, los programas de instalación no deben escribir directamente en el Registro. En su lugar, el programa de instalación debe realizarse Windows paquetes del instalador. Estas herramientas garantizan que el software se ejecuta bien y proporciona acceso a funcionalidades como el registro de clases por usuario.

 

Los controladores de extensión de Shell se ejecutan en el proceso de Shell. Dado que se trata de un proceso del sistema, el administrador de un sistema puede limitar los  controladores de extensión de Shell a los de una lista aprobada estableciendo el valor EnforceShellExtensionSecurity de la clave del explorador en 1 como se muestra aquí:

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

Para colocar un controlador de extensión de Shell en la lista aprobada, cree un valor **REG \_ SZ** cuyo nombre sea el formato de cadena del GUID del controlador en la **subclave Aprobado.**

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Por ejemplo, en el ejemplo siguiente se agregan los controladores *MyCommand* y *MyPropSheet* a la lista aprobada.

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

El Shell no usa el valor asignado al GUID, pero debe establecerse para facilitar la inspección del registro.

La aplicación de instalación puede agregar valores a la subclave **Aprobado** solo si la persona que instala la aplicación tiene privilegios suficientes. Si se produce un error al intentar agregar un controlador de extensión, debe informar al usuario de que se necesitan privilegios administrativos para instalar completamente la aplicación. Si el controlador es esencial para la aplicación, debe producir un error en la instalación y notificar al usuario que se pondrá en contacto con un administrador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicialización de controladores de extensión de Shell](int-shell-exts.md)
</dt> </dl>

 

 

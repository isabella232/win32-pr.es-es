---
description: En este tema se describen algunos de los aspectos que se deben tener en cuenta al usar bibliotecas en el programa.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Uso de bibliotecas en el programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2c76c4ce8bf9114d7294b257c03bcc62adecc947a3d7e651d6f94fa8876d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821115"
---
# <a name="using-libraries-in-your-program"></a>Uso de bibliotecas en el programa

En este tema se describen algunos de los aspectos que se deben tener en cuenta al usar bibliotecas en el programa.

En este tema:

-   [Introducción a la programación de bibliotecas](#library-programming-overview)
-   [Programación con bibliotecas](#programming-with-libraries)
    -   [Traslado de carpetas conocidas a bibliotecas](#moving-from-known-folders-to-libraries)
    -   [HomeGroup y bibliotecas compartidas](#homegroup-and-shared-libraries)
-   [Uso de un cuadro de diálogo de archivo común con bibliotecas](#using-a-common-file-dialog-box-with-libraries)
-   [Habilitación de la selección de biblioteca desde la interfaz de usuario](#enabling-library-selection-from-the-user-interface)
-   [Acceso al contenido de la biblioteca en un programa](#accessing-library-content-in-a-program)
    -   [Acceso al contenido de la biblioteca con la interfaz IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Acceso al contenido de la biblioteca con las API de Shell](#accessing-library-content-with-the-shell-apis)
-   [Guardar contenido de usuario en una biblioteca](#saving-user-content-in-a-library)
-   [Compatibilidad con operaciones de arrastrar y colocar en una biblioteca](#supporting-drag-and-drop-operations-in-a-library)
-   [Mantener la sincronización con una biblioteca](#keeping-in-sync-with-a-library)
    -   [Actualización masiva](#bulk-update)
    -   [Notificación de API de Shell](#shell-api-notification)
    -   [Notificación de API del sistema de archivos](#file-system-api-notification)
-   [Temas relacionados](#related-topics)

## <a name="library-programming-overview"></a>Introducción a la programación de bibliotecas

Las bibliotecas permiten a los usuarios organizar su contenido basado en archivos de una manera significativa para ellos y no limitada por la organización del sistema de archivos. Cuando el programa admite bibliotecas, permite al usuario encontrar su contenido de una manera que tenga sentido para ellas al presentar una interfaz de usuario coherente con la experiencia del usuario Windows 7. Las bibliotecas también facilitan al programa la búsqueda de contenido basado en archivos que se almacena en carpetas diferentes o en equipos diferentes.

En los temas de esta sección se describe cómo puede agregar compatibilidad con bibliotecas al programa y aprovechar las nuevas funcionalidades que ofrecen las bibliotecas. Windows 7 proporciona parte de esta compatibilidad de forma predeterminada. Si el programa no modifica los cuadros de diálogo de archivos comunes que usa actualmente, puede requerir muy poca programación adicional para admitir bibliotecas.

En esta sección se describen algunas de las características clave que proporcionan las bibliotecas y cómo admitirlas en el programa. Con esta información, puede decidir qué características proporcionarán la mejor experiencia de usuario del programa. Si el programa personaliza los cuadros de diálogo de archivos comunes, la información de esta sección puede ayudarle a determinar cómo usar los nuevos cuadros de diálogo de archivos comunes para usar bibliotecas y proporcionar funcionalidad equivalente en Windows 7.

## <a name="programming-with-libraries"></a>Programación con bibliotecas

El Windows de programación de Shell describe cómo interactúa un programa con Windows de programación de Shell. Aunque los objetos del sistema de archivos, como archivos y directorios, se representan mediante objetos de shell de Windows, no todos los objetos de Shell de Windows están representados por el sistema de archivos. Las bibliotecas, por ejemplo, Windows shell que no tienen un sistema de archivos equivalente. El Windows Shell en el programa permite que el programa acceda a todos los objetos de Shell y no solo a los objetos del sistema de archivos.

Para obtener los mejores resultados, el programa usaría la API de biblioteca de [**Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para interactuar con las bibliotecas y acceder a su contenido. Aunque las bibliotecas contienen elementos del sistema de archivos, como carpetas y archivos, las bibliotecas no son elementos del sistema de archivos. Por lo tanto, las API del sistema de archivos no se pueden usar para acceder a las características de la biblioteca ni al contenido de la biblioteca.

Si tiene un programa existente que actualmente usa muchas API del sistema de archivos, el programa todavía puede aprovechar las características de la biblioteca. La API de biblioteca de [**Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) puede proporcionar referencias del sistema de archivos a los elementos que se encuentran en una biblioteca y estas referencias del sistema de archivos, como el nombre de archivo y la ruta de acceso, se pueden pasar a las API del sistema de archivos existentes que se encuentran en el programa existente.

### <a name="moving-from-known-folders-to-libraries"></a>Traslado de carpetas conocidas a bibliotecas

Antes Windows 7 era habitual usar una carpeta conocida, como la carpeta Mis documentos, como carpeta predeterminada en las operaciones de guardado de archivos o de apertura de archivos. En Windows 7, se debe usar la biblioteca correspondiente para que el usuario tenga la misma experiencia en el programa que con otros programas de Windows 7, como Windows Explorer.

Si actualmente usa la API Windows Shell en el programa, agregar compatibilidad con bibliotecas es sencillo. Por ejemplo, si actualmente llama a la función [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) para obtener la ubicación de la carpeta Mis documentos, puede reemplazar el valor [**KNOWNFOLDERID**](knownfolderid.md) de la carpeta conocida Mis documentos por el valor **KNOWNFOLDERID** de la biblioteca correspondiente.

En la tabla siguiente se muestra la relación entre los [**valores KNOWNFOLDERID**](knownfolderid.md) de las carpetas conocidas y el **valor KNOWNFOLDERID** de la biblioteca correspondiente en Windows 7. 

| Valores known folder KNOWNFOLDERID | Valores KNOWNFOLDERID de la biblioteca |
|-----------------------------------|------------------------------|
| Documentos \_ FOLDERID               | FOLDERID \_ DocumentsLibrary   |
| IMÁGENES \_ DE FOLDERID                | FOLDERID \_ PicturesLibrary    |
| FolderID \_ Música                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>HomeGroup y bibliotecas compartidas

Al agregar compatibilidad con bibliotecas al programa, se habilitará la compatibilidad con las bibliotecas compartidas en un grupo de inicio. HomeGroup se identifica mediante su [**valor KNOWNFOLDERID**](knownfolderid.md) [**de FOLDERID \_ HomeGroup.**](knownfolderid.md) El programa puede encontrar la ubicación de guardado predeterminada privada o compartida del usuario estableciendo el valor [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) en la llamada al método [**IShellLibrary::GetDefaultSaveFolder.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder)

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Uso de un cuadro de diálogo de archivo común con bibliotecas

Uso de un cuadro de diálogo de archivo común con bibliotecas El cuadro de diálogo Archivo común se ha actualizado para admitir bibliotecas en Windows 7. En la ilustración siguiente se muestra cómo aparece el cuadro de diálogo de archivo común a un usuario Windows 7.

![captura de pantalla del cuadro de diálogo de archivo común que muestra las bibliotecas](images/libraries-commonfiledialog.png)

En Windows 7, si el programa muestra actualmente un cuadro de diálogo de archivo común y no cambia la plantilla de cuadro de diálogo ni enlazar ninguno de sus eventos, mostrará automáticamente la nueva versión Windows 7 del cuadro de diálogo. En concreto, en la llamada a la función de cuadro de diálogo de archivo común, los miembros **lpfnHook**, **hInstance**, **lpTemplatename** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deben ser **NULL** y las marcas **OFN \_ ENABLEHOOK** y **OFN \_ ENABLETEMPLATE** deben estar claras.

En Windows 7, las interfaces relacionadas con [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)reemplazan las funciones comunes del cuadro de diálogo de archivo que se usaban en versiones anteriores de Windows. Las funciones de cuadro de diálogo de archivos comunes anteriores todavía se admiten en Windows 7, pero no proporcionan la experiencia de usuario de Windows 7 completa y no admiten bibliotecas. Algunas de las nuevas características admitidas por las interfaces relacionadas con **IFileDialog** incluyen:

-   El usuario puede acceder a las propiedades de archivo admitidas por Windows 7 Windows Explorer para buscar y seleccionar los archivos.
-   El programa puede usar interfaces y métodos de la API de espacio de nombres de Shell para trabajar con los elementos.
-   El programa puede usar un modelo de personalización controlado por datos en lugar de un modelo de personalización controlado por archivos de recursos para agregar nuevos controles a los cuadros de diálogo de archivos comunes.

Debe usar las interfaces [**relacionadas con IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)cuando:

-   debe personalizar el cuadro de diálogo de archivo común para el programa en Windows 7. Esto permitirá que el programa funcione con bibliotecas y admita la personalización del cuadro de diálogo.
-   quiere que el usuario pueda seleccionar varios archivos de un cuadro de diálogo de archivo común. Esto garantizará que obtiene las rutas de acceso correctas al objeto seleccionado porque una biblioteca puede tener contenido almacenado en carpetas diferentes.

Para obtener más información sobre las interfaces relacionadas con [**IFileDialog,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)vea:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Habilitación de la selección de biblioteca desde la interfaz de usuario

Si el programa permite al usuario seleccionar una carpeta, como para las funciones de importación o exportación, en Windows 7, también debe permitir que el usuario seleccione una biblioteca. La [**interfaz IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) y la función [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) permiten al usuario seleccionar una biblioteca cuando se le pida que seleccione una carpeta. La **interfaz IFileOpenDialog** es preferible a la función **SHBrowseForFolder** porque **IFileOpenDialog** admite la interfaz de usuario Windows 7.

Para permitir que los usuarios seleccionen carpetas al usar la interfaz [**IFileOpenDialog,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) llame a SetOptions con la marca PICKFOLDERS de FOS establecida y asegúrese de que la marca FORCEFILESYSTEM de FOS está \_ \_ clara.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Para permitir que los usuarios seleccionen carpetas al llamar a la función SHBrowseForFolder, en el miembro ulFlags de la estructura [**BROWSEINFO,**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) establezca la marca USENEWUI de BIF y desactive la marca \_ BIF \_ RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Acceso al contenido de la biblioteca en un programa

Para acceder al contenido de una biblioteca, debe usar la API Windows Shell. Las funciones de la API del sistema de archivos no se pueden usar para acceder al contenido de la biblioteca porque las bibliotecas no son objetos del sistema de archivos. Si el programa usa un explorador de archivos personalizado basado en la API del sistema de archivos, no podrá examinar las bibliotecas ni acceder al contenido de la biblioteca.

En esta sección se describe cómo puede acceder al contenido de la biblioteca para que pueda seleccionar la mejor manera de actualizar el programa para que funcione con bibliotecas.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Acceso al contenido de la biblioteca con la interfaz IShellLibrary

La manera más fácil para que un programa acceda al contenido de la biblioteca es usar la [**API de biblioteca de Shell.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) Si está trabajando en un programa que usa la API del sistema de archivos, la API de biblioteca de **Shell** puede devolver las carpetas del sistema de archivos de una biblioteca, lo que minimiza el cambio en el código del programa existente.


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>Acceso al contenido de la biblioteca con las API de Shell

Dado que los objetos de biblioteca forman parte del modelo de programación de Shell, se pueden usar con otras API Windows Shell. Por ejemplo, puede usar las interfaces [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) e [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del programa, junto con las funciones auxiliares relacionadas, para acceder al contenido de una biblioteca de la misma manera que enumeraría las carpetas y el contenido de carpetas para acceder al contenido con las API del sistema de archivos.

Las API Windows Shell admiten dos modos de enumeración para acceder al contenido de una biblioteca:

-   **Enumeración Browse**

    La enumeración Browse es el modo de enumeración predeterminado y enumera el contenido de una carpeta de biblioteca. Desactive la marca SHCONTF \_ NAVIGATION \_ ENUM para usar este modo.

-   **Enumeración de navegación**

    La enumeración de navegación enumera las carpetas de la biblioteca. Establezca la marca SHCONTF \_ NAVIGATION \_ ENUM para usar este modo.

Si el programa usa un control de árbol personalizado para navegar por las carpetas del usuario, la enumeración de las carpetas en el modo de enumeración de navegación le dará una lista de las carpetas de una biblioteca que es coherente con la forma en que el Explorador de Windows enumera las carpetas de Windows 7.

Para obtener ejemplos de cómo usar estas características en un programa, consulte el ejemplo ShellStorage en Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Guardar contenido de usuario en una biblioteca

El programa puede guardar el contenido del usuario en una biblioteca, así como en una carpeta de la biblioteca. Del mismo modo, el usuario puede guardar en una carpeta específica de una biblioteca o simplemente guardar en la biblioteca.

Cada biblioteca tiene una carpeta que se designa como la ubicación de guardado predeterminada. La ubicación de guardado predeterminada se define cuando se crea la biblioteca; sin embargo, el usuario puede reasignar la ubicación de guardado predeterminada para que sea cualquier carpeta de la biblioteca. Aunque el usuario no necesita configurar una ubicación de guardado predeterminada, tiene la opción de cambiarla. Si el usuario elimina la carpeta que está establecida actualmente como la ubicación de guardado predeterminada, la biblioteca configurará automáticamente la siguiente carpeta de la biblioteca para que sea la ubicación de guardado predeterminada.

Hay varias maneras de guardar el contenido del usuario en una biblioteca.

-   **Shell API**

    Si usa el modelo de programación de Shell y guarda un elemento de Shell, representado por un [**IShellItem,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)IStorage o IStream, en un objeto de biblioteca, el elemento shell se almacenará automáticamente en la ubicación de guardado predeterminada de la biblioteca.

-   **API del sistema de archivos**

    Si tiene un programa existente que usa muchas llamadas API del sistema de archivos, puede obtener una ruta de acceso a la carpeta que se define como la ubicación de guardado predeterminada de la biblioteca. La ruta de acceso de la carpeta se puede pasar a una API del sistema de archivos.

Para obtener ejemplos de cómo usar estas características en un programa, consulte el ejemplo ShellStorage en Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Compatibilidad con operaciones de arrastrar y colocar en una biblioteca

Si el programa admite acciones de arrastrar y colocar, deben actualizarse para admitir la interacción correcta de la biblioteca. Si se deja un archivo en una biblioteca, el archivo eliminado se debe guardar en la ubicación de guardado predeterminada. Si se agrega una carpeta a una biblioteca, la carpeta descartada se debe agregar como una carpeta nueva a la biblioteca. Si un archivo se encuentra en una carpeta existente que no es la ubicación de guardado predeterminada, el archivo debe agregarse a la carpeta seleccionada.

Para obtener ejemplos de cómo agregar compatibilidad con bibliotecas para la funcionalidad de arrastrar y colocar programas, consulte el ejemplo ShellLibraryCommandLine en el SDK Windows.

## <a name="keeping-in-sync-with-a-library"></a>Mantener la sincronización con una biblioteca

En este tema se describe cómo un programa puede mantener actualizada su vista del contenido de una biblioteca.

### <a name="bulk-update"></a>Actualización masiva

Dado que el usuario puede modificar las carpetas de una biblioteca de forma interactiva cuando el programa no se está ejecutando, el programa debe llamar a [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) cuando empiece a detectar y almacenar los cambios en la biblioteca. La API de Shell proporciona la función **SHResolveLibrary** para permitir que un programa obtenga el contenido actual de una biblioteca y las ubicaciones actuales de las carpetas que la biblioteca puede contener.

Tenga en [**cuenta que SHResolveLibrary es**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) una función de bloqueo que puede tardar mucho tiempo en devolverse en función de lo que ha cambiado en la biblioteca. Por lo tanto, no debe llamarse desde un subproceso de interfaz de usuario.

Una vez actualizado el programa, puede registrarse para recibir notificaciones de cambio con el fin de mantener una vista actual.

### <a name="shell-api-notification"></a>Notificación de API de Shell

La API Windows Shell proporciona la función [**SHChangeNotifyRegister,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) que es la manera preferida para que los procesos que no son de servicio sean notificados de un cambio en la biblioteca.

Para detectar cambios en los elementos de una biblioteca mediante la API de shell de Windows, llame a [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) para registrar el programa para recibir notificaciones de cambios en los elementos de una carpeta de biblioteca. Esta función puede notificar al programa si hay un cambio en cualquier biblioteca o solo en una biblioteca específica. Las notificaciones se envían inmediatamente cuando se cambia una biblioteca.

### <a name="file-system-api-notification"></a>Notificación de API del sistema de archivos

Las notificaciones del sistema de archivos deben usarse en procesos de servicio.

Para detectar cambios en los elementos de una biblioteca mediante la API del sistema de archivos, enumere las carpetas de la biblioteca y llame a [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) para cada carpeta que se supervisará. El programa recibirá una notificación cuando cambie una carpeta supervisada. Para buscar el archivo específico de los archivos que han cambiado en la carpeta, llame a [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Para detectar cambios en el archivo de descripción de la biblioteca, supervise la carpeta que lo contiene. El archivo de descripción de la biblioteca se puede encontrar en la [**carpeta \_ Bibliotecas FOLDERID.**](knownfolderid.md) Sin embargo, el archivo de descripción de la biblioteca no debe abrirse ni modificarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[**ARGUMENTOS \_ de IID PPV \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 

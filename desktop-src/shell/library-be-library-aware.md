---
description: En este tema se describen algunos de los aspectos que se deben tener en cuenta al usar bibliotecas en el programa.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Usar bibliotecas en el programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2812a66b148d9bd16fc3951efab64a4d37afaaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361670"
---
# <a name="using-libraries-in-your-program"></a>Usar bibliotecas en el programa

En este tema se describen algunos de los aspectos que se deben tener en cuenta al usar bibliotecas en el programa.

En este tema:

-   [Información general sobre la programación de bibliotecas](#library-programming-overview)
-   [Programar con bibliotecas](#programming-with-libraries)
    -   [Mover de carpetas conocidas a bibliotecas](#moving-from-known-folders-to-libraries)
    -   [Grupo hogar y bibliotecas compartidas](#homegroup-and-shared-libraries)
-   [Usar un cuadro de diálogo de archivo común con bibliotecas](#using-a-common-file-dialog-box-with-libraries)
-   [Habilitar la selección de biblioteca desde la interfaz de usuario](#enabling-library-selection-from-the-user-interface)
-   [Acceder al contenido de una biblioteca en un programa](#accessing-library-content-in-a-program)
    -   [Acceder al contenido de la biblioteca con la interfaz IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Acceder al contenido de la biblioteca con las API de Shell](#accessing-library-content-with-the-shell-apis)
-   [Guardar el contenido de un usuario en una biblioteca](#saving-user-content-in-a-library)
-   [Admitir operaciones de arrastrar y colocar en una biblioteca](#supporting-drag-and-drop-operations-in-a-library)
-   [Mantener la sincronización con una biblioteca](#keeping-in-sync-with-a-library)
    -   [Actualización masiva](#bulk-update)
    -   [Notificación de API de Shell](#shell-api-notification)
    -   [Notificación de API del sistema de archivos](#file-system-api-notification)
-   [Temas relacionados](#related-topics)

## <a name="library-programming-overview"></a>Información general sobre la programación de bibliotecas

Las bibliotecas permiten a los usuarios organizar su contenido basado en archivos de forma que sean significativos para ellos y no estén limitados por la organización del sistema de archivos. Cuando el programa es compatible con las bibliotecas, permite al usuario buscar su contenido de forma que le resulte útil a la hora de presentar una interfaz de usuario coherente con la experiencia del usuario de Windows 7. Las bibliotecas también facilitan que el programa busque contenido basado en archivos que se almacena en carpetas diferentes o en equipos diferentes.

En los temas de esta sección se describe cómo puede Agregar compatibilidad con la biblioteca a su programa y aprovechar las nuevas funcionalidades que ofrecen las bibliotecas. Windows 7 proporciona parte de esta compatibilidad de forma predeterminada. Si el programa no modifica los cuadros de diálogo de archivos comunes que usa actualmente, podría requerir muy poca programación adicional para admitir las bibliotecas.

En esta sección se describen algunas de las características clave que proporcionan las bibliotecas y cómo admitirlas en el programa. Con esta información, puede decidir qué características proporcionarán la mejor experiencia de usuario de su programa. Si el programa Personaliza los cuadros de diálogo de archivos comunes, la información de esta sección puede ayudarle a determinar cómo usar los cuadros de diálogo nuevos archivos comunes para usar las bibliotecas y proporcionar una funcionalidad equivalente en Windows 7.

## <a name="programming-with-libraries"></a>Programar con bibliotecas

El modelo de programación del shell de Windows describe cómo interactúa un programa con objetos de programación del shell de Windows. Mientras que los objetos del sistema de archivos, como archivos y directorios, están representados por objetos de Shell de Windows, no todos los objetos de Shell de Windows están representados por el sistema de archivos. Por ejemplo, las bibliotecas son objetos del shell de Windows que no tienen un equivalente del sistema de archivos. El uso de objetos de Shell de Windows en el programa permite que el programa tenga acceso a todos los objetos de Shell y no solo a los objetos del sistema de archivos.

Para obtener los mejores resultados, el programa usaría la [**API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) de la biblioteca de Shell para interactuar con las bibliotecas y acceder a su contenido. Mientras que las bibliotecas contienen elementos del sistema de archivos, como carpetas y archivos, las bibliotecas no son elementos del sistema de archivos. Como tal, las API del sistema de archivos no se pueden usar para tener acceso a las características de la biblioteca o al contenido de la biblioteca.

Si tiene un programa existente que actualmente usa muchas API del sistema de archivos, el programa puede seguir aprovechando las características de la biblioteca. La [**API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) de la biblioteca de Shell puede proporcionar referencias del sistema de archivos a los elementos que se encuentran en una biblioteca y estas referencias del sistema de archivos, como el nombre de archivo y la ruta de acceso, se pueden pasar a las API del sistema de archivos existentes que se encuentran en el programa existente.

### <a name="moving-from-known-folders-to-libraries"></a>Mover de carpetas conocidas a bibliotecas

Antes de Windows 7 era habitual usar una carpeta conocida, como la carpeta Mis documentos, como carpeta predeterminada en operaciones de archivo guardar o abrir archivo. En Windows 7, se debe usar la biblioteca correspondiente, de modo que el usuario tendrá la misma experiencia en el programa que con otros programas de Windows 7, como el explorador de Windows.

Si actualmente usa la API de Shell de Windows en su programa, la compatibilidad con la biblioteca es sencilla. Por ejemplo, si actualmente llama a la función [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) para obtener la ubicación de la carpeta Mis documentos, puede reemplazar el valor de [**KNOWNFOLDERID**](knownfolderid.md) de la carpeta Mis documentos conocidos por el valor **KNOWNFOLDERID** de la biblioteca correspondiente.

En la tabla siguiente se muestra la relación entre los valores [**KNOWNFOLDERID**](knownfolderid.md) de las carpetas conocidas y el valor **KNOWNFOLDERID** de la biblioteca correspondiente en Windows 7. 

| Valores de KNOWNFOLDERID de carpeta conocidos | Valores de KNOWNFOLDERID de biblioteca |
|-----------------------------------|------------------------------|
| Documentos de FOLDERID \_               | FOLDERID \_ DocumentsLibrary   |
| Imágenes de FOLDERID \_                | FOLDERID \_ PicturesLibrary    |
| \_Música FOLDERID                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>Grupo hogar y bibliotecas compartidas

La incorporación de compatibilidad con la biblioteca al programa habilitará la compatibilidad con las bibliotecas compartidas en un grupo en el hogar. El grupo en el hogar se identifica mediante su valor [**KNOWNFOLDERID**](knownfolderid.md) de [**FOLDERID \_ Grupo**](knownfolderid.md)en el hogar. El programa puede identificar la ubicación de almacenamiento predeterminada privada o compartida del usuario estableciendo el valor de [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) en la llamada al método [**IShellLibrary:: GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) .

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Usar un cuadro de diálogo de archivo común con bibliotecas

Usar un cuadro de diálogo de archivo común con bibliotecas el cuadro de diálogo archivo común se ha actualizado para admitir las bibliotecas de Windows 7. La siguiente ilustración muestra cómo aparece el cuadro de diálogo archivo común a un usuario en Windows 7.

![captura de pantalla del cuadro de diálogo de archivo común que muestra las bibliotecas](images/libraries-commonfiledialog.png)

En Windows 7, si el programa muestra actualmente un cuadro de diálogo de archivo común y no cambia la plantilla de cuadro de diálogo ni enlaza ninguno de sus eventos, se mostrará automáticamente la nueva versión de Windows 7 del cuadro de diálogo. En concreto, en la función de la llamada al cuadro de diálogo de archivo común, los miembros **lpfnHook**, **hInstance**, **lpTemplatename** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deben ser **null** y los marcadores **OFN \_ ENABLEHOOK** y **OFN \_ ENABLETEMPLATE** deben ser claros.

En Windows 7, las interfaces relacionadas con [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)reemplazan las funciones del cuadro de diálogo de archivos comunes que se usaban en versiones anteriores de Windows. Las funciones del cuadro de diálogo de archivos comunes anteriores todavía se admiten en Windows 7, pero no proporcionan la experiencia del usuario completa de Windows 7 y no admiten bibliotecas. Algunas de las nuevas características admitidas por las interfaces relacionadas con **IFileDialog** incluyen:

-   El usuario puede tener acceso a las propiedades de archivo admitidas por el explorador de Windows 7 para buscar y seleccionar los archivos.
-   El programa puede utilizar interfaces y métodos de la API del espacio de nombres del shell para trabajar con los elementos.
-   El programa puede usar un modelo de personalización controlado por datos en lugar de un modelo de personalización controlado por archivos de recursos para agregar nuevos controles a los cuadros de diálogo de archivos comunes.

Debe usar las interfaces relacionadas con [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)cuando:

-   debe personalizar el cuadro de diálogo archivo común para el programa en Windows 7. Esto permitirá que el programa funcione con las bibliotecas y admita la personalización del cuadro de diálogo.
-   quiere que el usuario pueda seleccionar varios archivos desde un cuadro de diálogo de archivo común. Así se asegurará de que obtiene las rutas de acceso correctas al objeto seleccionado, ya que una biblioteca puede tener contenido que se almacena en carpetas diferentes.

Para obtener más información sobre las interfaces relacionadas con [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), vea:

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Habilitar la selección de biblioteca desde la interfaz de usuario

Si el programa permite al usuario seleccionar una carpeta, como las funciones de importación o exportación, en Windows 7, debe permitir que el usuario seleccione también una biblioteca. La interfaz [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) y la función [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) permiten al usuario seleccionar una biblioteca cuando se le pide que seleccione una carpeta. La interfaz **IFileOpenDialog** es preferible a la función **SHBrowseForFolder** porque **IFileOpenDialog** es compatible con la interfaz de usuario de Windows 7.

Para permitir que los usuarios seleccionen carpetas al usar la interfaz [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) , llame a SetOptions con la marca de FOS \_ PICKFOLDERS establecida y asegúrese de que la marca de FOS \_ FORCEFILESYSTEM está clara.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Para permitir que los usuarios seleccionen carpetas al llamar a la función SHBrowseForFolder, en el miembro ulFlags de la estructura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) , establezca la \_ marca BIF USENEWUI y borre la \_ marca BIF RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Acceder al contenido de una biblioteca en un programa

Para tener acceso al contenido de una biblioteca, debe usar la API de Shell de Windows. Las funciones de la API de sistema de archivos no se pueden usar para tener acceso al contenido de la biblioteca porque las bibliotecas no son objetos del sistema de archivos. Si el programa usa un explorador de archivos personalizado que se basa en la API del sistema de archivos, no podrá examinar bibliotecas ni acceder al contenido de la biblioteca.

En esta sección se describe cómo puede tener acceso al contenido de la biblioteca para que pueda seleccionar la mejor manera de actualizar el programa para trabajar con las bibliotecas.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Acceder al contenido de la biblioteca con la interfaz IShellLibrary

La forma más sencilla de que un programa tenga acceso al contenido de la biblioteca es usar la API de la [**biblioteca de Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary). Si está trabajando en un programa que usa la API del sistema de archivos, la **API** de la biblioteca de Shell puede devolver las carpetas del sistema de archivos de una biblioteca, lo que minimiza el cambio en el código de programa existente.


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



### <a name="accessing-library-content-with-the-shell-apis"></a>Acceder al contenido de la biblioteca con las API de Shell

Dado que los objetos de biblioteca forman parte del modelo de programación de Shell, se pueden usar con otras API del shell de Windows. Por ejemplo, puede usar las interfaces [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) y [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) en el programa, junto con las funciones auxiliares relacionadas, para tener acceso al contenido de una biblioteca de la misma manera en que se enumeran las carpetas y el contenido de la carpeta para tener acceso al contenido con las API del sistema de archivos.

Las API del shell de Windows admiten dos modos de enumeración para tener acceso al contenido de una biblioteca:

-   **Examinar enumeración**

    Examinar enumeración es el modo de enumeración predeterminado y enumera el contenido de una carpeta de biblioteca. Desactive la \_ marca de la enumeración de navegación SHCONTF \_ para usar este modo.

-   **Enumeración de navegación**

    La enumeración de navegación enumera las carpetas de la biblioteca. Establezca la marca de la \_ enumeración de navegación SHCONTF \_ para usar este modo.

Si el programa usa un control de árbol personalizado para navegar por las carpetas del usuario, la enumeración de las carpetas en el modo de enumeración de navegación le proporcionará una lista de las carpetas de la biblioteca que es coherente con la forma en que el explorador de Windows enumera las carpetas en Windows 7.

Para obtener ejemplos de cómo usar estas características en un programa, vea el ejemplo ShellStorage en el Windows SDK.

## <a name="saving-user-content-in-a-library"></a>Guardar el contenido de un usuario en una biblioteca

El programa puede guardar el contenido de un usuario en una biblioteca, así como en una carpeta de la biblioteca. Del mismo modo, el usuario puede guardar en una carpeta específica de una biblioteca o simplemente guardar en la biblioteca.

Cada biblioteca tiene una carpeta que se designa como ubicación de almacenamiento predeterminada. La ubicación de almacenamiento predeterminada se define cuando se crea la biblioteca. sin embargo, el usuario puede reasignar la ubicación de almacenamiento predeterminada para que sea cualquier carpeta de la biblioteca. Aunque el usuario no necesita configurar una ubicación de almacenamiento predeterminada, tiene la opción de cambiarla. Si el usuario elimina la carpeta que está configurada actualmente como ubicación de almacenamiento predeterminada, la biblioteca configurará automáticamente la carpeta siguiente en la biblioteca para que sea la ubicación de almacenamiento predeterminada.

Hay varias maneras de guardar el contenido de un usuario en una biblioteca.

-   **API de Shell**

    Si usa el modelo de programación de Shell y guarda un elemento de Shell, como se representa mediante [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem), IStorage o IStream, en un objeto de biblioteca, el elemento de Shell se almacenará automáticamente en la ubicación de almacenamiento predeterminada de la biblioteca.

-   **API del sistema de archivos**

    Si tiene un programa existente que usa muchas llamadas API del sistema de archivos, puede obtener una ruta de acceso a la carpeta definida como la ubicación de almacenamiento predeterminada de la biblioteca. La ruta de acceso de la carpeta se puede pasar a una API del sistema de archivos.

Para obtener ejemplos de cómo usar estas características en un programa, vea el ejemplo ShellStorage en el Windows SDK.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Admitir operaciones de arrastrar y colocar en una biblioteca

Si el programa admite acciones de arrastrar y colocar, deben actualizarse para admitir la interacción de biblioteca correcta. Si se coloca un archivo en una biblioteca, el archivo quitado debe guardarse en la ubicación de almacenamiento predeterminada. Si una carpeta se coloca en una biblioteca, la carpeta quitada debe agregarse como una nueva carpeta a la biblioteca. Si un archivo se coloca en una carpeta existente que no es la ubicación de almacenamiento predeterminada, el archivo debe agregarse a la carpeta seleccionada.

Para obtener ejemplos de cómo agregar compatibilidad de biblioteca para la funcionalidad de arrastrar y colocar de programas, consulte el ejemplo ShellLibraryCommandLine en el Windows SDK.

## <a name="keeping-in-sync-with-a-library"></a>Mantener la sincronización con una biblioteca

En este tema se describe cómo un programa puede mantener actualizada su vista del contenido de una biblioteca.

### <a name="bulk-update"></a>Actualización masiva

Dado que el usuario puede modificar las carpetas de una biblioteca de forma interactiva cuando el programa no se está ejecutando, el programa debe llamar a [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) cuando empiece a detectar y almacenar los cambios en la biblioteca. La API de Shell proporciona la función **SHResolveLibrary** para permitir que un programa obtenga el contenido actual de una biblioteca y las ubicaciones actuales de cualquier carpeta que la biblioteca pueda contener.

Tenga en cuenta que [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) es una función de bloqueo que podría tardar mucho tiempo en devolverse según lo que haya cambiado en la biblioteca. Como tal, no se debe llamar desde un subproceso de interfaz de usuario.

Una vez que el programa se ha actualizado, puede registrarse para recibir notificaciones de cambio con el fin de mantener una vista actual.

### <a name="shell-api-notification"></a>Notificación de API de Shell

La API de Shell de Windows proporciona la función [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) , que es la manera preferida para que los procesos que no son de servicio reciban una notificación de un cambio en la biblioteca.

Para detectar cambios en los elementos de una biblioteca mediante la API de Shell de Windows, llame a [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) para registrar el programa para las notificaciones de cambios en los elementos de una carpeta de biblioteca. Esta función puede notificar al programa si hay un cambio en alguna biblioteca o simplemente en una biblioteca específica. Las notificaciones se envían inmediatamente cuando se cambia una biblioteca.

### <a name="file-system-api-notification"></a>Notificación de API del sistema de archivos

Las notificaciones del sistema de archivos se deben usar en los procesos de servicio.

Para detectar cambios en los elementos de una biblioteca mediante la API del sistema de archivos, enumere las carpetas de la biblioteca y llame a [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) para cada carpeta que se va a supervisar. El programa recibirá una notificación cuando cambie una carpeta supervisada. Para buscar el archivo específico de archivos que han cambiado en la carpeta, llame a [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Para detectar cambios en el archivo de descripción de la biblioteca, supervise la carpeta que lo contiene. El archivo de descripción de la biblioteca se puede encontrar en la carpeta [**FOLDERID \_ Libraries**](knownfolderid.md) . El archivo de descripción de la biblioteca, sin embargo, no se debe abrir ni modificar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Vínculos de Shell](./links.md)
</dt> <dt>

[Carpetas conocidas](known-folders.md)
</dt> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 

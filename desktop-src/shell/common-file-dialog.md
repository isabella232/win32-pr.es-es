---
description: A partir de Windows Vista, el cuadro de diálogo de elementos comunes reemplaza al cuadro de diálogo de archivos común más antiguo cuando se usa para abrir o guardar un archivo.
title: Cuadro de diálogo de elementos comunes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360168"
---
# <a name="common-item-dialog"></a>Cuadro de diálogo de elementos comunes

A partir de Windows Vista, el cuadro de diálogo de elementos comunes reemplaza al cuadro de diálogo de archivos común más antiguo cuando se usa para abrir o guardar un archivo. El cuadro de diálogo de elementos comunes se usa en dos variaciones: el cuadro de diálogo **abrir** y el cuadro de diálogo **Guardar** . Estos dos cuadros de diálogo comparten la mayor parte de su funcionalidad, pero cada uno tiene sus propios métodos únicos.

Aunque esta nueva versión se denomina cuadro de diálogo de elementos comunes, se sigue llamando cuadro de diálogo de archivo común en la mayoría de la documentación. A menos que esté tratando específicamente con una versión anterior de Windows, debe suponer que cualquier mención del cuadro de diálogo de archivo común hace referencia a este cuadro de diálogo de elementos comunes.

Los temas siguientes se tratan aquí:

-   [IFileDialog, IFileOpenDialog y IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Ejemplo de uso](#sample-usage)
-   [Escuchar eventos desde el cuadro de diálogo](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation y OnOverwrite](#onshareviolation-and-onoverwrite)
-   [Personalización del cuadro de diálogo](#customizing-the-dialog)
    -   [Agregar opciones al botón Aceptar](#adding-options-to-the-ok-button)
    -   [Responder a eventos en controles agregados](#responding-to-events-in-added-controls)
-   [Ejemplos completos](#full-samples)
-   [Temas relacionados](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog y IFileSaveDialog

Windows Vista proporciona implementaciones de los cuadros de diálogo de **apertura** y **guardado** : CLSID \_ FileOpenDialog y CLSID \_ FileSaveDialog. Estos cuadros de diálogo se muestran aquí.

![captura de pantalla del cuadro de diálogo abrir](images/cid/openfiledialog.png)

![captura de pantalla del cuadro de diálogo Guardar como](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) y [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) se heredan de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) y comparten gran parte de su funcionalidad. Además, el cuadro de diálogo **abrir** admite **IFileOpenDialog** y el cuadro de diálogo **Guardar** es compatible con **IFileSaveDialog**.

La implementación del cuadro de diálogo de elementos comunes que se encuentra en Windows Vista proporciona varias ventajas con respecto a la implementación proporcionada en versiones anteriores:

-   Admite el uso directo del espacio de nombres del shell a través de [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) en lugar de usar rutas de acceso del sistema de archivos.
-   Habilita la personalización simple del cuadro de diálogo, como la configuración de la etiqueta en el botón **Aceptar** , sin necesidad de un procedimiento de enlace.
-   Admite la personalización más amplia del cuadro de diálogo mediante la adición de un conjunto de controles controlados por datos que funcionan sin una plantilla de cuadro de diálogo de Win32. Este esquema de personalización libera el proceso de llamada del diseño de la interfaz de usuario. Dado que los cambios realizados en el diseño del cuadro de diálogo siguen utilizando este modelo de datos, la implementación del cuadro de diálogo no está asociada a la versión específica actual del cuadro de diálogo.
-   Admite la notificación del llamador de eventos dentro del cuadro de diálogo, como el cambio de selección o el cambio de tipo de archivo. También permite que el proceso de llamada enlace determinados eventos en el cuadro de diálogo, como el análisis.
-   Presenta nuevas características de diálogo como agregar lugares especificados por el autor de la llamada a la barra de **ubicaciones** .
-   En el cuadro de diálogo **Guardar** , los desarrolladores pueden aprovechar las nuevas características de metadatos del shell de Windows Vista.

Además, los desarrolladores pueden optar por implementar las siguientes interfaces:

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) para recibir notificaciones de eventos en el cuadro de diálogo.
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) para agregar controles al cuadro de diálogo.
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) para recibir notificaciones de eventos en esos controles agregados.

El cuadro de diálogo **abrir** o **Guardar** devuelve un objeto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) al proceso de llamada. A continuación, el autor de la llamada puede usar un objeto **IShellItem** individual para obtener una ruta de acceso del sistema de archivos o para abrir un flujo en el elemento para leer o escribir información.

Las marcas y opciones disponibles para los nuevos métodos de diálogo son muy similares a las anteriores marcas de **OFN** que se encuentran en la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y se usan en [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) y [**getSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Muchos de ellos son exactamente iguales, salvo que comienzan con un prefijo de FOS. La lista completa se puede encontrar en los temas [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) y [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . Los cuadros de diálogo **abrir** y **Guardar** se crean de forma predeterminada con las marcas más comunes. En el cuadro de diálogo **abrir** , es (FOS \_ PATHMUSTEXIST \| FOS \_ FILEMUSTEXIST \| FOS \_ NOCHANGEDIR) y para el cuadro de diálogo **Guardar** esto es (FOS \_ OVERWRITEPROMPT \| FOS \_ NOREADONLYRETURN \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).

[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) y sus interfaces descendientes heredan de y extienden [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) toma como único parámetro el identificador de la ventana primaria. Si **Show** se devuelve correctamente, hay un resultado válido. Si devuelve `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa que el usuario canceló el cuadro de diálogo. También podría devolver de forma legítima otro código de error, como **E \_ OUTOFMEMORY**.

### <a name="sample-usage"></a>Ejemplo de uso

En las secciones siguientes se muestra código de ejemplo para una variedad de tareas de diálogo.

-   [Uso básico](#basic-usage)
-   [Limitar los resultados a los elementos del sistema de archivos](#limiting-results-to-file-system-items)
-   [Especificar tipos de archivo para un cuadro de diálogo](#specifying-file-types-for-a-dialog)
-   [Controlar la carpeta predeterminada](#controlling-the-default-folder)
-   [Agregar elementos a la barra de ubicaciones](#adding-items-to-the-places-bar)
-   [Persistencia de estado](#state-persistence)
-   [Funcionalidades de selección MultiSelect](#multiselect-capabilities)

La mayor parte del código de ejemplo puede encontrarse en el [ejemplo de cuadro de diálogo Windows SDK Common File](samples-commonfiledialog.md).

### <a name="basic-usage"></a>Uso básico

En el ejemplo siguiente se muestra cómo iniciar un cuadro de diálogo **abierto** . En este ejemplo, está restringido a los documentos de Microsoft Word.

> [!Note]  
> En varios ejemplos de este tema se usa la `CDialogEventHandler_CreateInstance` función auxiliar para crear una instancia de la implementación de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) . Para usar esta función en su propio código, copie el código fuente de la `CDialogEventHandler_CreateInstance` función del [ejemplo de cuadro de diálogo de archivo común](samples-commonfiledialog.md), del que se toman todos los ejemplos de este tema.

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a>Limitar los resultados a los elementos del sistema de archivos

En el ejemplo siguiente, tomado de arriba, se muestra cómo restringir los resultados a los elementos del sistema de archivos. Tenga en cuenta que [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) agrega la nueva marca a un valor obtenido a través de [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Éste es el método recomendado.


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a>Especificar tipos de archivo para un cuadro de diálogo

Para establecer tipos de archivo específicos que el cuadro de diálogo puede controlar, use el método [**IFileDialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) . Ese método acepta una matriz de estructuras [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , cada una de las cuales representa un tipo de archivo.

El mecanismo de extensión predeterminado en un cuadro de diálogo no cambia de [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) y [**getSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). La extensión de nombre de archivo que se anexa al texto que escribe el usuario en el cuadro de edición nombre de archivo se inicializa al abrir el cuadro de diálogo. Debe coincidir con el tipo de archivo predeterminado (que se selecciona al abrir el cuadro de diálogo). Si el tipo de archivo predeterminado es " \* . \* " (todos los archivos), el archivo puede ser una extensión de su elección. Si el usuario elige otro tipo de archivo, la extensión se actualiza automáticamente a la primera extensión de nombre de archivo asociada a ese tipo de archivo. Si el usuario elige "" \* . \* (todos los archivos), la extensión vuelve a su valor original.

En el ejemplo siguiente se muestra cómo se hizo anteriormente.


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a>Controlar la carpeta predeterminada

Casi cualquier carpeta en el espacio de nombres del shell se puede usar como carpeta predeterminada para el cuadro de diálogo (la carpeta que se presenta cuando el usuario elige abrir o guardar un archivo). Llame a [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) antes de llamar a [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) para hacerlo.

La carpeta predeterminada es la carpeta en la que se inicia el cuadro de diálogo la primera vez que un usuario lo abre desde la aplicación. Después, el cuadro de diálogo se abrirá en la última carpeta que un usuario abrió o en la última carpeta que usó para guardar un elemento. Vea [persistencia del estado](#state-persistence) para obtener más detalles.

Puede forzar que el cuadro de diálogo muestre siempre la misma carpeta cuando se abra, independientemente de la acción anterior del usuario, mediante una llamada a [**IFileDialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder). Sin embargo, no se recomienda hacerlo. Si llama a **SetFolder** antes de mostrar el cuadro de diálogo, no se muestra la ubicación más reciente en la que el usuario guardó o se abrió. A menos que haya un motivo muy específico para este comportamiento, no es una experiencia de usuario buena o esperada y se debe evitar. En casi todas las instancias, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) es el mejor método.

Al guardar un documento por primera vez en el cuadro de diálogo **Guardar** , debe seguir las mismas directrices para determinar la carpeta inicial como hizo en el cuadro de diálogo **abrir** . Si el usuario está editando un documento existente previamente, abra el cuadro de diálogo en la carpeta donde se almacena ese documento y rellene el cuadro de edición con el nombre del documento. Llame a [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) con el elemento actual antes de llamar a [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Agregar elementos a la barra de ubicaciones

En el ejemplo siguiente se muestra la adición de elementos a la barra de **ubicaciones** :


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a>Persistencia de estado

Antes de Windows Vista, un estado, como la última carpeta visitada, se guardaba por proceso. Sin embargo, esa información se usó independientemente de la acción concreta. Por ejemplo, una aplicación de edición de vídeo presentaría la misma carpeta en el cuadro de diálogo **representar como** en el cuadro de diálogo **importar medios** . En Windows Vista puede ser más específico a través del uso de GUID. Para asignar un **GUID** al cuadro de diálogo, llame a [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Funcionalidades de selección MultiSelect

La funcionalidad de selección MultiSelect está disponible en el cuadro de diálogo **abrir** con el método [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , tal como se muestra aquí.


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a>Escuchar eventos desde el cuadro de diálogo

Un proceso de llamada puede registrar una interfaz [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) con el cuadro de diálogo mediante los métodos [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) y [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) como se muestra aquí.

Esto se toma del ejemplo de [uso básico](#basic-usage) .


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



La mayor parte del procesamiento de cuadros de diálogo se situaría aquí.


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



El proceso de llamada puede usar eventos para la notificación cuando el usuario cambia la carpeta, el tipo de archivo o la selección. Estos eventos son especialmente útiles cuando el proceso de llamada agrega controles al cuadro de diálogo (vea [personalizar el cuadro de diálogo](#customizing-the-dialog)) y debe cambiar el estado de dichos controles en respuesta a estos eventos. Útil en todos los casos es la capacidad del proceso de llamada de proporcionar código personalizado para tratar situaciones como el uso compartido de infracciones, la sobrescritura de archivos o la determinación de si un archivo es válido antes de que se cierre el cuadro de diálogo. Algunos de estos casos se describen en esta sección.

### <a name="onfileok"></a>OnFileOk

Se llama a este método después de que el usuario elija un elemento, justo antes de que se cierre el cuadro de diálogo. A continuación, la aplicación puede llamar a [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) o [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) tal como se haría una vez que el cuadro de diálogo se hubiera cerrado. Si el elemento elegido es aceptable, pueden devolver S \_ correctos. De lo contrario, devuelven S \_ false y muestran la interfaz de usuario que indica al usuario por qué el elemento elegido no es válido. Si \_ se devuelve S false, el cuadro de diálogo no se cierra.

El proceso de llamada puede usar el identificador de ventana del propio cuadro de diálogo como elemento primario de la interfaz de usuario. Ese identificador se puede obtener llamando primero a [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) y llamando a [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) con el identificador tal como se muestra en este ejemplo.


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation y OnOverwrite

Si el usuario elige sobrescribir un archivo en el cuadro de diálogo **Guardar** o si un archivo que se está guardando o reemplazando está en uso y no se puede escribir en él (una infracción de uso compartido), la aplicación puede proporcionar funcionalidad personalizada para invalidar el comportamiento predeterminado del cuadro de diálogo. De forma predeterminada, al sobrescribir un archivo, el cuadro de diálogo muestra un mensaje que permite al usuario comprobar esta acción. Para las infracciones de uso compartido, de forma predeterminada el cuadro de diálogo muestra un mensaje de error, no se cierra y el usuario debe tomar otra decisión. El proceso de llamada puede invalidar estos valores predeterminados y mostrar su propia interfaz de usuario si lo desea. Se puede indicar al cuadro de diálogo que rechace el archivo y que permanezca abierto o acepte el archivo y se cierre correctamente.

## <a name="customizing-the-dialog"></a>Personalización del cuadro de diálogo

Se pueden agregar varios controles al cuadro de diálogo sin proporcionar una plantilla de cuadro de diálogo de Win32. Estos controles incluyen PushButton, ComboBox, EditBox, CheckButton, listas de RadioButton, grupos, separadores y controles de texto estático. Llame a **QueryInterface** en el objeto de cuadro de diálogo ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) para obtener un puntero de [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . Utilice esa interfaz para agregar controles. Cada control tiene asociado un identificador proporcionado por el autor de la llamada, así como un estado *visible* y *habilitado* que puede establecer el proceso que realiza la llamada. Algunos controles, como PushButton, también tienen texto asociado.

Se pueden agregar varios controles a un "grupo visual" que se mueve como una sola unidad en el diseño del cuadro de diálogo. Los grupos pueden tener una etiqueta asociada.

Los controles solo se pueden agregar antes de que se muestre el cuadro de diálogo. Sin embargo, una vez que se muestra el cuadro de diálogo, los controles pueden ocultarse o mostrarse como se desee, quizás en respuesta a la acción del usuario. En los siguientes ejemplos se muestra cómo agregar una lista de botones de radio al cuadro de diálogo.


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a>Agregar opciones al botón Aceptar

Del mismo modo, se pueden agregar opciones a los botones **abrir** o **Guardar** , que son el botón **Aceptar** para sus respectivos tipos de diálogo. Se puede tener acceso a las opciones a través de un cuadro de lista desplegable asociado al botón. El primer elemento de la lista se convierte en el texto del botón. En el ejemplo siguiente se muestra cómo proporcionar un botón **abrir** con dos posibilidades: "abrir" y "abrir como solo lectura".


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





La elección del usuario puede comprobarse después de que el cuadro de diálogo vuelva del método [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) como lo haría para un ComboBox, o bien puede comprobarse como parte del control por [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).

### <a name="responding-to-events-in-added-controls"></a>Responder a eventos en controles agregados

El controlador de eventos proporcionado por el proceso de llamada puede implementar [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) además de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents). **IFileDialogControlEvents** permite al proceso de llamada reaccionar a estos eventos:

-   Clic en el pulsador
-   Estado de CheckButton cambiado
-   Elemento seleccionado en un menú, cuadro combinado o lista de controles RadioButton
-   Control que se va a activar. Se envía cuando un menú está a punto de mostrar una lista desplegable, en caso de que el proceso de llamada desee cambiar los elementos de la lista.

## <a name="full-samples"></a>Ejemplos completos

A continuación se muestran ejemplos de C++ completos y descargables del kit de desarrollo de software (SDK) de Windows que muestran el uso de e interacción con el cuadro de diálogo de elementos comunes.

-   [Ejemplo de cuadro de diálogo de archivo común](samples-commonfiledialog.md)
-   [Ejemplo de modos de cuadro de diálogo de archivo común](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 

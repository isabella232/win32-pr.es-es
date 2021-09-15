---
description: Las funcionalidades del shell se pueden ampliar con entradas del Registro y .ini archivos.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Creación de controladores de extensiones de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572532"
---
# <a name="creating-shell-extension-handlers"></a>Creación de controladores de extensiones de shell

Las funcionalidades del shell se pueden ampliar con entradas del Registro y .ini archivos. Aunque este enfoque para extender el shell es sencillo y adecuado para muchos propósitos, es limitado. Por ejemplo, si usa el Registro para especificar un icono personalizado para un tipo de archivo, aparecerá el mismo icono para cada archivo de ese tipo. La extensión del Shell con el Registro no permite variar el icono para diferentes archivos del mismo tipo. Otros aspectos del Shell,  como la hoja de propiedades Propiedades que se puede mostrar cuando se hace clic con el botón derecho en un archivo, no se pueden modificar en absoluto con el Registro.

Un enfoque más eficaz y flexible para extender el shell es implementar controladores *de extensión de shell*. Estos controladores se pueden implementar para diversas acciones que el Shell puede realizar. Antes de realizar la acción, el Shell consulta el controlador de extensión, lo que le ofrece la oportunidad de modificar la acción. Un ejemplo común es un controlador de extensión de menú contextual. Si se implementa uno para un tipo de archivo, se consultará cada vez que se haga clic con el botón derecho en uno de los archivos. A continuación, el controlador puede especificar elementos de menú adicionales en función del archivo por archivo, en lugar de tener el mismo conjunto para todo el tipo de archivo.

En este documento se describe cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell. Los siguientes controladores están asociados a un tipo de archivo determinado y permiten especificar archivos por archivo:



| Controlador                                               | Descripción                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de menú contextual](context-menu-handlers.md)    | Se llama antes de que se muestre el menú contextual de un archivo. Permite agregar elementos al menú contextual archivo por archivo.                                               |
| [Controlador de datos](how-to-create-data-handlers.md)       | Se llama cuando se realiza una operación de arrastrar y colocar en objetos de DragShell. Permite proporcionar formatos de Portapapeles adicionales al destino de colocación.                        |
| [Controlador de colocación](how-to-create-drop-handlers.md)       | Se llama cuando se arrastra o se descarta un objeto de datos en un archivo. Permite convertir un archivo en un destino de colocación.                                                          |
| [Controlador de iconos](how-to-create-icon-handlers.md)       | Se llama antes de que se muestre el icono de un archivo. Le permite reemplazar el icono predeterminado del archivo por un icono personalizado en función de archivo por archivo.                                    |
| [Controlador de la hoja de propiedades](propsheet-handlers.md)      | Se llama antes de que se muestre **la hoja de** propiedades Propiedades de un objeto. Permite agregar o reemplazar páginas.                                                              |
| [**Controlador de imágenes en miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Proporciona una imagen para representar el elemento.                                                                                                                                   |
| [**Controlador de recuadro informativo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre el objeto.                                                                                               |
| [**Controlador de metadatos**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Proporciona acceso de lectura y escritura a los metadatos (propiedades) almacenados en un archivo. Se puede usar para ampliar la vista Detalles, la información sobre información, la página de propiedades y las características de agrupación. |



 

Otros controladores no están asociados a un tipo de archivo determinado, pero se llama a ellos antes de algunas operaciones de Shell:



| Controlador                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de columnas](../lwef/column-handlers.md)                             | Lo llama Windows explorador antes de mostrar la vista Detalles de una carpeta. Permite agregar columnas personalizadas a la vista Detalles.        |
| [Controlador de enlace de copia](how-to-create-copy-hook-handlers.md)          | Se llama cuando se va a mover, copiar, eliminar o cambiar el nombre de una carpeta o un objeto de impresora. Permite aprobar o vetar la operación.   |
| [Controlador de arrastrar y colocar](context-menu-handlers.md)                 | Se llama cuando se arrastra un archivo con el botón derecho del mouse. Permite modificar el menú contextual que se muestra.                     |
| [Controlador de superposición de iconos](how-to-implement-icon-overlay-handlers.md) | Se llama antes de que se muestre el icono de un archivo. Permite especificar una superposición para el icono del archivo.                                          |
| [Controlador de búsqueda](../lwef/search-handlers.md)                             | Se llama para iniciar un motor de búsqueda. Permite implementar un motor de búsqueda personalizado accesible desde el **menú** Inicio o Windows Explorer. |



 

Los detalles de cómo implementar controladores de extensión específicos se tratan en las secciones enumeradas anteriormente. En el resto de este documento se tratan algunos problemas de implementación que son comunes a todos los controladores de extensión de Shell.

-   [Implementar controladores de extensión de shell](#implementing-shell-extension-handlers)
    -   [Implementación de IPersistFile](#implementing-ipersistfile)
    -   [Implementación de IShellExtInit](#implementing-ishellextinit)
    -   [Personalización de información](#infotip-customization)
-   [Mejorar la Windows búsqueda con controladores de extensión de shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registro de controladores de extensión de shell](#registering-shell-extension-handlers)
    -   [Nombres de controlador](#handler-names)
    -   [Objetos de shell predefinidos](#predefined-shell-objects)
    -   [Ejemplo de un registro de controlador de extensión](#example-of-an-extension-handler-registration)
-   [Temas relacionados](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementar controladores de extensión de shell

Gran parte de la implementación de un objeto de controlador de extensión de Shell depende de su tipo. Sin embargo, hay algunos elementos comunes. En esta sección se de abordan los aspectos de implementación que comparten todos los controladores de extensión de Shell.

Muchos controladores de extensión de Shell son objetos del Modelo de objetos componentes (COM) en proceso. Se les debe asignar un GUID y registrarse como se describe en Registro de controladores de extensión de shell. Se implementan como archivos DLL y deben exportar las siguientes funciones estándar:

-   [**DllMain**](../dlls/dllmain.md). Punto de entrada estándar al archivo DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expone el generador de clases del objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM llama a esta función para determinar si el objeto está atendiendo a algún cliente. Si no es así, el sistema puede descargar el archivo DLL y liberar la memoria asociada.

Al igual que todos los objetos COM, los controladores de extensiones de Shell deben implementar una [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un generador [de clases](../com/implementing-iclassfactory.md). La mayoría de los controladores de extensión también deben implementar una [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en Windows XP o versiones anteriores. Estos se reemplazaron por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) en Windows Vista. El Shell usa estas interfaces para inicializar el controlador.

La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) debe implementarse mediante lo siguiente:

-   Controladores de datos
-   Controladores de colocación

En el pasado, los controladores de iconos también eran necesarios para implementar [**IPersistFile,**](/windows/win32/api/objidl/nn-objidl-ipersistfile)pero esto ya no es cierto. Para los controladores de iconos, **IPersistFile** ahora es opcional y se prefieren otras interfaces como [**IInitializeWithItem.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)

La [**interfaz IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) debe implementarse mediante lo siguiente:

-   Controladores de menús contextuales
-   Controladores de arrastrar y colocar
-   Controladores de hoja de propiedades

### <a name="implementing-ipersistfile"></a>Implementación de IPersistFile

La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) está diseñada para permitir que un objeto se cargue o guarde en un archivo de disco. Tiene seis métodos además de [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)cinco propios y el [**método GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que hereda de [**IPersist.**](/windows/win32/api/objidl/nn-objidl-ipersist) Con las extensiones de Shell, **IPersist** solo se usa para inicializar un objeto de controlador de extensiones de Shell. Dado que normalmente no es necesario leer o escribir en el disco, solo los métodos **GetClassID** y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requieren una implementación sintoken.

El shell llama [**primero a GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y la función devuelve el identificador de clase (CLSID) del objeto de controlador de extensión. A continuación, el shell [**llama a Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) y pasa dos valores. El primero, *pszFileName*, es una cadena Unicode con el nombre del archivo o carpeta en la que shell está a punto de funcionar. El segundo es *dwMode*, que indica el modo de acceso a archivos. Dado que normalmente no es necesario tener acceso a los archivos, *dwMode* suele ser cero. El método almacena estos valores según sea necesario para su referencia posterior.

En el fragmento de código siguiente se muestra cómo un controlador de extensión de Shell típico implementa los [**métodos GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) [**y Load.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) Está diseñado para controlar ANSI o Unicode. CLSID SampleExtHandler es el GUID del objeto de controlador de extensiones y CSampleExtHandler es el nombre de la clase utilizada para \_ implementar la interfaz . Las variables **m \_ szFileName** y **m \_ dwMode** son variables privadas que se usan para almacenar el nombre del archivo y las marcas de acceso.


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

La [**interfaz IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) solo tiene un método, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). El método tiene tres parámetros que el Shell puede usar para pasar varios tipos de información. Los valores pasados en dependen del tipo de controlador y algunos se pueden establecer en **NULL.**

-   *pIDFolder* contiene el puntero de una carpeta a una lista de identificadores de elemento (PIDL). Para las extensiones de hoja de propiedades, es **NULL.** Para las extensiones de menú contextual, es el PIDL de la carpeta que contiene el elemento cuyo menú contextual se muestra. Para los controladores de arrastrar y colocar no predeterminados, es el PIDL de la carpeta de destino.
-   *pDataObject* contiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un objeto de datos. El objeto de datos contiene uno o varios nombres de archivo en [formato CF \_ HDROP.](dragdrop.md)
-   *hRegKey contiene* una clave del Registro para el tipo de carpeta o objeto de archivo.

El [**método IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) almacena el nombre de archivo, el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) y la clave del Registro según sea necesario para su uso posterior. El fragmento de código siguiente muestra una implementación de **IShellExtInit::Initialize**. Para simplificar, en este ejemplo se supone que el objeto de datos contiene solo un archivo. En general, puede contener varios archivos que cada uno de ellos tendrá que extraer.


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler es el nombre de la clase utilizada para implementar la interfaz . Las variables **m \_ pIDFolder**, **m \_ pDataObject,** **m \_ szFileName** y **m \_ hRegKey** son variables privadas que se usan para almacenar la información que se pasa. Para simplificar, en este ejemplo se supone que el objeto de datos solo mantendrá un nombre de archivo. Después de recuperar la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) del objeto de datos, [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) se usa para extraer el nombre de archivo del miembro **medium.hGlobal** de la estructura **FORMATETC.** Si se pasa una clave del Registro, el método usa [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para abrir la clave y asigna el identificador a **m \_ hRegKey**.

### <a name="infotip-customization"></a>Personalización de información

Hay dos maneras de personalizar la información:

-   Implemente un objeto que admita [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) y, a continuación, registre ese objeto en la subclave adecuada en el Registro (vea Registrar controladores de extensión [de shell a](#registering-shell-extension-handlers) continuación).
-   Especifique una cadena fija o una lista de propiedades de archivo específicas que se mostrarán.

Para mostrar una cadena fija para una extensión de espacio de nombres, cree una entrada denominada en la `InfoTip` *clave {CLSID}* de la extensión de espacio de nombres. Establezca el valor de esa entrada como la cadena literal que desea mostrar, como se muestra en este ejemplo, o una cadena indirecta que especifica un recurso e índice dentro de ese recurso (con fines de localización).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para mostrar una cadena fija para un tipo de archivo, cree una entrada llamada en `InfoTip` la *clave ProgID* de ese tipo de archivo. Establezca el valor de esa entrada como la cadena literal que desea mostrar o una cadena indirecta que especifica un recurso e índice dentro de ese recurso (con fines de localización), como se muestra en este ejemplo.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Si desea que el Shell muestre propiedades de archivo específicas en la información sobre un tipo de archivo específico, cree una entrada llamada en la clave `InfoTip` *ProgID* para ese tipo de archivo. Establezca el valor de esa entrada como una lista delimitada por punto y coma de nombres de propiedad canónicos, pares de identificador de formato (FMTID)/identificador de propiedad (PID) o ambos. Este valor debe comenzar por "prop:" para identificarlo como una cadena de lista de propiedades. Si omite "prop:", el valor se ve como una cadena literal y se muestra como tal.

En el ejemplo siguiente, *propname* es un nombre de propiedad canónico (como System.Date) y *{fmtid}, pid* es un [**par FMTID/PID.**](./objects.md)

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Se pueden usar los siguientes nombres de propiedad:



| Nombre de la propiedad    | Descripción                   | Recuperado de                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autor           | Autor del documento        | [**PIDSI \_ AUTHOR**](../stg/the-summary-information-property-set.md)                              |
| Título            | Título del documento         | [**PIDSI \_ TITLE**](../stg/the-summary-information-property-set.md)                               |
| Asunto          | Resumen del asunto               | [**ASUNTO \_ PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Comentario          | Comentarios de documentos             | [**PIDSI \_ COMMENT**](../stg/the-summary-information-property-set.md) o propiedades de carpeta o controlador |
| PageCount        | Número de páginas               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                           |
| Nombre             | Nombre descriptivo                 | Vista de carpeta estándar                                                                       |
| OriginalLocation | Ubicación del archivo original     | Carpeta de minúsculas y papelera de reciclaje carpeta                                                    |
| DateDeleted      | Archivo de fecha eliminado         | papelera de reciclaje carpeta                                                                         |
| Tipo             | Tipo de archivo                  | Vista de detalles de carpeta estándar                                                               |
| Size             | Tamaño del archivo                  | Vista de detalles de carpeta estándar                                                               |
| SyncCopyIn       | Igual que OriginalLocation      | Igual que OriginalLocation                                                                   |
| Modificado         | Fecha de última modificación            | Vista de detalles de carpeta estándar                                                               |
| Creado          | Fecha de creación                  | Vista de detalles de carpeta estándar                                                               |
| Acceder         | Fecha a la que se ha accedido por última vez            | Vista de detalles de carpeta estándar                                                               |
| InFolder         | Directorio que contiene el archivo | Resultados de búsqueda de documentos                                                                    |
| Rango             | Calidad de la coincidencia de búsqueda       | Resultados de búsqueda de documentos                                                                    |
| FreeSpace        | Espacio de almacenamiento disponible       | Unidades de disco                                                                                |
| NumberOfVisits   | Número de visitas              | carpeta Favoritos                                                                           |
| Atributos       | Atributos de archivo               | Vista de detalles de carpeta estándar                                                               |
| Compañía          | Nombre de la compañía                  | [**PIDDSI \_ COMPANY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Categoría del documento             | [**PIDDSI \_ (CATEGORÍA)**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Copyright multimedia               | [**COPYRIGHT de \_ PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | Archivo de información sobre HTML             | Desktop.ini archivo para la carpeta                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Mejorar la Windows con controladores de extensión de Shell

Los controladores de extensión de Shell se pueden usar para mejorar la experiencia del usuario proporcionada por un controlador de protocolo Windows Search. Para habilitar estas mejoras, el controlador de extensión de Shell compatible debe estar diseñado para integrarse con el controlador de protocolo de búsqueda como origen de datos. Para obtener información sobre cómo mejorar un controlador de protocolo Windows Search mediante la integración con un controlador de extensiones de Shell, vea Agregar iconos, vistas previas y [menús contextuales.](../search/-search-3x-wds-ph-ui-extensions.md) Para obtener más información sobre Windows de protocolo search, vea [Developing Protocol Handlers](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Registro de controladores de extensión de Shell

Se debe registrar un objeto de controlador de extensión de Shell para poder usarlo. Esta sección es una explicación general de cómo registrar un controlador de extensión de Shell.

Cada vez que cree o cambie un controlador de extensión de Shell, es importante notificar al sistema que ha realizado un cambio con [**SHChangeNotify,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)especificando el evento **\_ ASSOCCHANGED de SHCNE.** Si no llama a **SHChangeNotify,** es posible que el cambio no se reconozca hasta que se reinicie el sistema.

Al igual que con todos los objetos COM, debe crear un GUID para el controlador mediante una herramienta como UUIDGEN.exe. Cree una clave en **HKEY \_ CLASSES \_ ROOT** \\ **CLSID** cuyo nombre sea la forma de cadena del GUID. Dado que los controladores de extensiones de Shell son servidores en proceso, debe crear una clave **InProcServer32** en la clave GUID con el valor predeterminado establecido en la ruta de acceso del archivo DLL del controlador. Use el modelo de subprocesamiento Apartment.

Cada vez que shell realiza una acción que puede implicar un controlador de extensión de Shell, comprueba la clave del Registro adecuada. La clave con la que se registra un controlador de extensión controla cuándo se llamará. Por ejemplo, es una práctica común tener un controlador de menú contextual llamado cuando el Shell muestra un menú contextual para un miembro de un [tipo de archivo](fa-file-types.md). En este caso, el controlador debe registrarse en la clave **ProgID** del tipo de archivo.

### <a name="handler-names"></a>Nombres de controlador

Para habilitar un controlador de extensión de Shell, cree una subclave con el nombre de subclave del controlador (consulte a continuación) en la subclave **ShellEx** del **ProgID** (para los tipos de archivo) o el nombre del tipo de objeto shell (para objetos de [shell](#predefined-shell-objects)predefinidos).

Por ejemplo, si quisiera registrar un controlador de extensión de menú contextual para MyProgram.1, comenzaría creando la subclave siguiente:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Para los siguientes controladores, cree una subclave debajo de la clave "Nombre de subclave del controlador" cuyo nombre sea la versión de cadena del CLSID de la extensión de Shell. Se pueden registrar varias extensiones en la clave de nombre de subclave del controlador mediante la creación de varias subclaves.



| Controlador                                               | Interfaz          | Nombre de subclave del controlador       |
|-------------------------------------------------------|--------------------|---------------------------|
| Controlador de menú contextual                                 | IContextMenu       | **ContextMenuHandlers**   |
| Controlador de copyhook                                      | ICopyHook          | **CopyHookHandlers**      |
| Controlador de arrastrar y colocar                                 | IContextMenu       | **DragDropHandlers**      |
| Controlador de la hoja de propiedades                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Controlador de proveedor de columnas (en desuso en Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Para los siguientes controladores, el valor predeterminado de la clave "Nombre de subclave del controlador" es la versión de cadena del CLSID de la extensión shell. Solo se puede registrar una extensión para estos controladores.



| Controlador                 | Interfaz                                         | Nombre de subclave del controlador                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Controlador de datos            | IDataObject                                       | **Datahandler**                            |
| Controlador de colocación            | IDropTarget                                       | **DropHandler**                            |
| Controlador de iconos            | IExtractIconA/W                                   | **IconHandler**                            |
| Controlador de imágenes           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Controlador de imágenes en miniatura | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Controlador de recuadro informativo         | IQueryInfo                                        | **{00021500-0000-0000-C000-00000000046}** |
| Vínculo de shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-00000000046}** |
| Vínculo de shell (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-00000000046}** |
| Almacenamiento estructurado      | IStorage                                          | **{0000000B-0000-0000-C000-00000000046}** |
| Metadatos                | IPropertyStore                                    | **PropertyHandler**                        |
| Metadatos                | IPropertySetStorage (en desuso en Windows Vista) | **PropertyHandler**                        |
| Anclar al menú Inicio       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Anclar a la barra de tareas          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Las subclaves especificadas  para agregar  Anclar al menú Inicio y Anclar a la barra de tareas al menú contextual de un elemento solo son necesarias para los tipos de archivo que incluyen la [entrada IsShortCut.](./links.md)

Se quitó la compatibilidad con controladores de proveedor de columnas Windows Vista. Además, a Windows Vista, [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) ha quedado en desuso en favor de [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Aunque [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) sigue siendo compatible, [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) es preferible para Windows Vista y versiones posteriores.

### <a name="predefined-shell-objects"></a>Objetos de shell predefinidos

El shell define objetos adicionales en **HKEY \_ CLASSES \_ ROOT** que se pueden extender de la misma manera que los tipos de archivo. Por ejemplo, para agregar un controlador de hoja de propiedades para todos los archivos, puede registrarse en la **clave PropertySheetHandlers.**

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

En la tabla siguiente se ofrecen las distintas subclaves **de HKEY \_ CLASSES \_ ROOT** en las que se pueden registrar controladores de extensión. Tenga en cuenta que muchos controladores de extensión no se pueden registrar en todas las subclaves enumeradas. Para obtener más información, vea la documentación del controlador específico.



| Subclave                    | Descripción                                                          | Posibles controladores                                | Versión |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\***                    | Todos los archivos                                                            | Menú contextual, hoja de propiedades, verbos (ver a continuación) | All     |
| **AllFileSystemObjects**  | Todos los archivos y carpetas de archivos                                           | Menú contextual, hoja de propiedades, verbos             | 4.71    |
| **Carpeta**                | Todas las carpetas                                                          | Menú contextual, hoja de propiedades, verbos             | All     |
| **Directorio**             | Carpetas de archivos                                                         | Menú contextual, hoja de propiedades, verbos             | All     |
| **Fondo del \\ directorio** | Fondo de la carpeta de archivos                                               | Solo menú contextual                               | 4.71    |
| **Unidad**                 | Todas las unidades de MyComputer, como "C: \\ "                             | Menú contextual, hoja de propiedades, verbos             | All     |
| **Network**               | Toda la red (en Mis lugares de red)                             | Menú contextual, hoja de propiedades, verbos             | All     |
| **Tipo de \\ red\\\#**     | Todos los objetos de tipo \# (consulte a continuación)                                   | Menú contextual, Hoja de propiedades, Verbos             | 4.71    |
| **NetShare**              | Todos los recursos compartidos de red                                                   | Menú contextual, Hoja de propiedades, Verbos             | 4.71    |
| **Netserver**             | Todos los servidores de red                                                  | Menú contextual, Hoja de propiedades, Verbos             | 4.71    |
| *nombre \_ del proveedor de \_ red* | Todos los objetos proporcionados por el proveedor de red "*nombre del proveedor de \_ \_ red*" | Menú contextual, Hoja de propiedades, Verbos             | All     |
| **Impresoras**              | Todas las impresoras                                                         | Menú contextual, Hoja de propiedades                    | All     |
| **AudioCD**               | CD de audio en la unidad de CD                                                 | Solo verbos                                       | All     |
| **DVD**                   | Unidad de DVD (Windows 2000)                                             | Menú contextual, hoja de propiedades, verbos             | 4.71    |



 

Notas:

-   Para acceder al menú contextual de fondo de la carpeta de archivos, haga clic con el botón derecho en una carpeta de archivos, pero no sobre el contenido de la carpeta.
-   "Verbos" son comandos especiales registrados en el verbo de shell de subclave **\_ \_ ROOT HKEY CLASSES** \\  \\  \\  .
-   Para **Tipo de** \\ **red** , " " es un código de tipo de proveedor de red en \\ **\#** \# decimal. El código de tipo de proveedor de red es la palabra alta de un tipo de red. La lista de tipos de red se muestra en el archivo de encabezado Winnetwk.h (valores de WNNC \_ \_ \* NET). Por ejemplo, WNNC NET 0X00330000, por lo que la clave de tipo correspondiente sería \_ \_ **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51** .
-   "*nombre del proveedor \_ \_ de* red " es un nombre de proveedor de red especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con los espacios convertidos en caracteres de subrayado. Por ejemplo, si está instalado el proveedor de red de redes de Microsoft, su nombre de proveedor es "Microsoft Windows Network" y el nombre del proveedor de red correspondiente es **Microsoft \_ Windows \_ Network**. *\_ \_*

### <a name="example-of-an-extension-handler-registration"></a>Ejemplo de un registro de controlador de extensión

Para habilitar un controlador determinado, cree una subclave en la clave de tipo del controlador de extensión con el nombre del controlador. El Shell no usa el nombre del controlador, pero debe ser diferente de todos los demás nombres de esa subclave de tipo. Establezca el valor predeterminado de la subclave name en el formato de cadena del GUID del controlador.

En el ejemplo siguiente se muestran las entradas del Registro que habilitan el menú contextual y los controladores de extensión de la hoja de propiedades, con un tipo de archivo .myp de ejemplo:

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

El procedimiento de registro descrito en esta sección debe seguirse para todos Windows sistemas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía para implementar In-Process de archivos](shell-and-managed-code.md)
</dt> </dl>

 

 

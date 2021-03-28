---
description: Las capacidades del shell se pueden extender con las entradas del registro y los archivos. ini.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Creación de controladores de extensiones de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997717"
---
# <a name="creating-shell-extension-handlers"></a>Creación de controladores de extensiones de shell

Las capacidades del shell se pueden extender con las entradas del registro y los archivos. ini. Aunque este enfoque para extender el Shell es sencillo y adecuado para muchos propósitos, es limitado. Por ejemplo, si usa el registro para especificar un icono personalizado para un tipo de archivo, aparecerá el mismo icono para cada archivo de ese tipo. La extensión del shell con el registro no le permite modificar el icono de los distintos archivos del mismo tipo. Otros aspectos del shell, como la hoja de propiedades **propiedades** que se pueden mostrar cuando se hace clic con el botón derecho en un archivo, no se pueden modificar en absoluto con el registro.

Un enfoque más eficaz y flexible para extender el Shell es implementar *controladores de extensión de Shell*. Estos controladores se pueden implementar para diversas acciones que puede realizar el shell. Antes de realizar la acción, el shell consulta el controlador de extensión, lo que le otorga la oportunidad de modificar la acción. Un ejemplo común es un controlador de extensión de menú contextual. Si se implementa una para un tipo de archivo, se consultará cada vez que se haga clic con el botón derecho en uno de los archivos. A continuación, el controlador puede especificar elementos de menú adicionales cada archivo, en lugar de tener el mismo conjunto para todo el tipo de archivo.

En este documento se explica cómo implementar los controladores de extensión que permiten modificar diversas acciones de Shell. Los siguientes controladores están asociados a un tipo de archivo determinado y le permiten especificar uno por archivo:



| Controlador                                               | Descripción                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador del menú contextual](context-menu-handlers.md)    | Se llama antes de que se muestre el menú contextual de un archivo. Permite agregar elementos al menú contextual de forma individual para cada archivo.                                               |
| [Controlador de datos](how-to-create-data-handlers.md)       | Se llama cuando se realiza una operación de arrastrar y colocar en objetos dragShell. Permite proporcionar formatos de Portapapeles adicionales al destino de colocación.                        |
| [Quitar controlador](how-to-create-drop-handlers.md)       | Se llama cuando se arrastra un objeto de datos o se coloca en un archivo. Permite crear un archivo en un destino de colocación.                                                          |
| [Controlador de iconos](how-to-create-icon-handlers.md)       | Se llama antes de que se muestre el icono de un archivo. Permite reemplazar el icono predeterminado del archivo con un icono personalizado en función de cada archivo.                                    |
| [Controlador de la hoja de propiedades](propsheet-handlers.md)      | Se llama antes de que se muestre la hoja de propiedades de **propiedades** de un objeto. Permite agregar o reemplazar páginas.                                                              |
| [**Controlador de imagen en miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Proporciona una imagen para representar el elemento.                                                                                                                                   |
| [**Controlador de recuadro informativo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre el objeto.                                                                                               |
| [**Controlador de metadatos**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Proporciona acceso de lectura y escritura a los metadatos (propiedades) almacenados en un archivo. Se puede usar para ampliar la vista de detalles, recuadros informativos, la página de propiedades y las características de agrupación. |



 

Otros controladores no están asociados a un tipo de archivo determinado, pero se les llama antes que algunas operaciones de Shell:



| Controlador                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlador de columnas](../lwef/column-handlers.md)                             | Lo llama el explorador de Windows antes de mostrar la vista de detalles de una carpeta. Permite agregar columnas personalizadas a la vista de detalles.        |
| [Copiar controlador de enlace](how-to-create-copy-hook-handlers.md)          | Se llama cuando una carpeta o un objeto de impresora está a punto de moverse, copiarse, eliminarse o cambiarse de nombre. Permite aprobar o vetar la operación.   |
| [Controlador de arrastrar y colocar](context-menu-handlers.md)                 | Se le llama cuando se arrastra un archivo con el botón secundario del mouse. Permite modificar el menú contextual que se muestra.                     |
| [Controlador de superposición de iconos](how-to-implement-icon-overlay-handlers.md) | Se llama antes de que se muestre el icono de un archivo. Permite especificar una superposición para el icono del archivo.                                          |
| [Controlador de búsqueda](../lwef/search-handlers.md)                             | Se llama para iniciar un motor de búsqueda. Permite implementar un motor de búsqueda personalizado accesible desde el menú **Inicio** o el explorador de Windows. |



 

Los detalles sobre cómo implementar controladores de extensión específicos se tratan en las secciones anteriores. En el resto de este documento se tratan algunos problemas de implementación comunes a todos los controladores de extensión de Shell.

-   [Implementar controladores de extensión de Shell](#implementing-shell-extension-handlers)
    -   [Implementar IPersistFile](#implementing-ipersistfile)
    -   [Implementación de IShellExtInit](#implementing-ishellextinit)
    -   [Personalización de recuadro informativo](#infotip-customization)
-   [Mejorar Windows Search con controladores de extensión de Shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrando controladores de extensión de Shell](#registering-shell-extension-handlers)
    -   [Nombres de controlador](#handler-names)
    -   [Objetos de Shell predefinidos](#predefined-shell-objects)
    -   [Ejemplo de registro de un controlador de extensión](#example-of-an-extension-handler-registration)
-   [Temas relacionados](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementar controladores de extensión de Shell

Gran parte de la implementación de un objeto de controlador de extensión de Shell depende de su tipo. Sin embargo, hay algunos elementos comunes. En esta sección se describen los aspectos de la implementación que comparten todos los controladores de extensión de Shell.

Muchos controladores de extensión de Shell son objetos de modelo de objetos componentes (COM) en proceso. Se les debe asignar un GUID y registrarse como se describe en registrar controladores de extensión de Shell. Se implementan como archivos dll y deben exportar las siguientes funciones estándar:

-   [**DllMain**](../dlls/dllmain.md). Punto de entrada estándar al archivo DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expone el generador de clases del objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM llama a esta función para determinar si el objeto atiende a los clientes. De lo contrario, el sistema puede descargar el archivo DLL y liberar la memoria asociada.

Al igual que todos los objetos COM, los controladores de la extensión de Shell deben implementar una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un [generador de clases](../com/implementing-iclassfactory.md). La mayoría de los controladores de extensión también deben implementar una interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en Windows XP o versiones anteriores. Se reemplazaron por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) y [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) en Windows Vista. El shell usa estas interfaces para inicializar el controlador.

La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) debe implementarse de la siguiente manera:

-   Controladores de datos
-   Quitar controladores

En el pasado, los controladores de iconos también eran necesarios para implementar [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), pero esto ya no es así. En el caso de los controladores de iconos, **IPersistFile** es opcional y se prefieren otras interfaces como [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) .

La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) debe implementarse de la siguiente manera:

-   Controladores de menú contextual
-   Controladores de arrastrar y colocar
-   Controladores de hoja de propiedades

### <a name="implementing-ipersistfile"></a>Implementar IPersistFile

La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) está pensada para permitir que un objeto se cargue desde un archivo de disco o se guarde en él. Tiene seis métodos además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de los suyos propios y el método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que hereda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Con las extensiones de Shell, **IPersist** solo se usa para inicializar un objeto de controlador de extensión de Shell. Dado que normalmente no es necesario leer o escribir en el disco, solo los métodos **GetClassID** y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requieren una implementación sin token.

El shell llama primero a [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y la función devuelve el identificador de clase (CLSID) del objeto de controlador de extensión. Después, el shell llama a [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) y pasa dos valores. La primera, *pszFileName*, es una cadena Unicode con el nombre del archivo o carpeta en el que está a punto de trabajar el shell. La segunda es *dwMode*, que indica el modo de acceso a archivos. Dado que normalmente no es necesario tener acceso a los archivos, *dwMode* suele ser cero. El método almacena estos valores según sea necesario para su posterior referencia.

En el fragmento de código siguiente se muestra cómo un controlador de extensión de Shell típico implementa los métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Está diseñado para controlar ANSI o Unicode. CLSID \_ SampleExtHandler es el GUID del objeto del controlador de extensión y CSampleExtHandler es el nombre de la clase que se usa para implementar la interfaz. Las variables **m \_ szFileName** y **m \_ dwMode** son variables privadas que se usan para almacenar el nombre y las marcas de acceso del archivo.


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

La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tiene solo un método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). El método tiene tres parámetros que el shell puede usar para pasar varios tipos de información. Los valores pasados dependen del tipo de controlador y otros pueden establecerse en **null**.

-   *pIDFolder* contiene el puntero de una carpeta a una lista de identificadores de elementos (PIDL). En el caso de las extensiones de la hoja de propiedades, es **null**. En el caso de las extensiones de menú contextual, es el PIDL de la carpeta que contiene el elemento cuyo menú contextual se muestra. En el caso de los controladores no predeterminados de arrastrar y colocar, es el PIDL de la carpeta de destino.
-   *pDataObject* contiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un objeto de datos. El objeto de datos contiene uno o varios nombres de archivo en formato [ \_ HDROP de CF](dragdrop.md) .
-   *hRegKey* contiene una clave del registro para el tipo de carpeta o objeto de archivo.

El método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) almacena el nombre de archivo, el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) y la clave del registro según sea necesario para su uso posterior. En el fragmento de código siguiente se muestra una implementación de **IShellExtInit:: Initialize**. Para simplificar, en este ejemplo se da por supuesto que el objeto de datos contiene un solo archivo. En general, puede que contenga varios archivos que deberán extraerse cada uno.


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

CSampleExtHandler es el nombre de la clase que se usa para implementar la interfaz. Las **variables \_ m pIDFolder**, **m \_ pDataObject**, **m \_ szFileName** y **m \_ hRegKey** son variables privadas que se usan para almacenar la información que se pasa. Para simplificar, en este ejemplo se da por supuesto que solo el objeto de datos conservará un nombre de archivo. Una vez recuperada la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) del objeto de datos, se usa [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) para extraer el nombre de archivo del miembro **Medium. hGlobal** de la estructura **FORMATETC** . Si se pasa una clave del registro, el método usa [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para abrir la clave y asigna el identificador a **m \_ hRegKey**.

### <a name="infotip-customization"></a>Personalización de recuadro informativo

Hay dos maneras de personalizar recuadros informativos:

-   Implemente un objeto que admita [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) y, a continuación, registre ese objeto en la subclave adecuada del registro (consulte [registro de controladores de extensión de Shell](#registering-shell-extension-handlers) a continuación).
-   Especifique una cadena fija o una lista de propiedades de archivo específicas que se van a mostrar.

Para mostrar una cadena fija para una extensión de espacio de nombres, cree una entrada llamada `InfoTip` en la clave *{CLSID}* de la extensión de espacio de nombres. Establezca el valor de la entrada para que sea la cadena literal que desea mostrar, como se muestra en este ejemplo, o una cadena indirecta que especifique un recurso y un índice dentro de ese recurso (con fines de localización).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para mostrar una cadena fija para un tipo de archivo, cree una entrada llamada `InfoTip` en la clave *ProgID* de ese tipo de archivo. Establezca el valor de la entrada para que sea la cadena literal que desea mostrar o una cadena indirecta que especifique un recurso y un índice dentro de ese recurso (para la localización), tal como se muestra en este ejemplo.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Si desea que el shell muestre propiedades de archivo específicas en el recuadro informativo para un tipo de archivo específico, cree una entrada llamada `InfoTip` en la clave *ProgID* para ese tipo de archivo. Establezca el valor de esa entrada en una lista delimitada por punto y coma de nombres de propiedad canónicos, pares de identificador de formato (FMTID) (PID) o ambos. Este valor debe comenzar por "prop:" para identificarlo como una cadena de lista de propiedades. Si se omite "prop:", el valor se considera una cadena literal y se muestra como tal.

En el ejemplo siguiente, *propName* es un nombre de propiedad canónico (como System. Date) y *{fmtid}, el PID* es un par [**fmtid/PID**](./objects.md) .

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Se pueden usar los siguientes nombres de propiedad:



| Nombre de la propiedad    | Descripción                   | Recuperado de                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autor           | Autor del documento        | [**autor de PIDSI \_**](../stg/the-summary-information-property-set.md)                              |
| Title            | Título del documento         | [**título de PIDSI \_**](../stg/the-summary-information-property-set.md)                               |
| Asunto          | Resumen de asunto               | [**\_asunto PIDSI**](../stg/the-summary-information-property-set.md)                             |
| Comentario          | Comentarios del documento             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propiedades de comentario o carpeta/controlador |
| PageCount        | Número de páginas               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                           |
| Nombre             | Nombre descriptivo                 | Vista de carpetas estándar                                                                       |
| OriginalLocation | Ubicación del archivo original     | Carpeta de mi maletín y carpeta de la papelera de reciclaje                                                    |
| DateDeleted      | Se eliminó el archivo de fecha         | Carpeta de la papelera de reciclaje                                                                         |
| Tipo             | Tipo de archivo                  | Vista de detalles de carpetas estándar                                                               |
| Tamaño             | Tamaño del archivo                  | Vista de detalles de carpetas estándar                                                               |
| SyncCopyIn       | Igual que OriginalLocation      | Igual que OriginalLocation                                                                   |
| Modificado         | Fecha de última modificación            | Vista de detalles de carpetas estándar                                                               |
| Creado          | Fecha de creación                  | Vista de detalles de carpetas estándar                                                               |
| Acceso         | Fecha de último acceso            | Vista de detalles de carpetas estándar                                                               |
| InFolder         | Directorio que contiene el archivo | Resultados de búsqueda de documentos                                                                    |
| Rango             | Calidad de coincidencia de búsqueda       | Resultados de búsqueda de documentos                                                                    |
| FreeSpace        | Espacio de almacenamiento disponible       | Unidades de disco                                                                                |
| NumberOfVisits   | Número de visitas              | carpeta Favoritos                                                                           |
| Atributos       | Atributos de archivo               | Vista de detalles de carpetas estándar                                                               |
| Compañía          | Nombre de la compañía                  | [**\_empresa PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Category         | Categoría del documento             | [**\_categoría PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Copyright        | Copyright de los medios               | [**COPYRIGHT de PIDMSI \_**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | Archivo recuadro informativo HTML             | Desktop.ini archivo para la carpeta                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Mejorar Windows Search con controladores de extensión de Shell

Los controladores de extensión de Shell se pueden usar para mejorar la experiencia del usuario que proporciona un controlador de protocolo de Windows Search. Para habilitar dichas mejoras, el controlador de extensión de Shell auxiliar debe estar diseñado para integrarse con el controlador de protocolo de búsqueda como origen de datos. Para obtener información sobre cómo mejorar un controlador de protocolo de Windows Search mediante la integración con un controlador de extensión de Shell, vea [Agregar iconos, vistas previas y menús contextuales](../search/-search-3x-wds-ph-ui-extensions.md). Para obtener más información acerca de los controladores de protocolo de Windows Search, consulte [desarrollar controladores de protocolo](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Registrando controladores de extensión de Shell

Un objeto de controlador de extensión de Shell debe registrarse antes de que el shell pueda usarlo. Esta sección es una discusión general sobre cómo registrar un controlador de extensión de Shell.

Cada vez que crea o cambia un controlador de extensión de Shell, es importante notificar al sistema que ha realizado un cambio con [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando el **evento \_ ASSOCCHANGED de SHCNE** . Si no llama a **SHChangeNotify**, es posible que no se reconozca el cambio hasta que se reinicie el sistema.

Al igual que con todos los objetos COM, debe crear un GUID para el controlador mediante una herramienta como UUIDGEN.exe. Cree una clave en **\_ las clases HKEY \_ raíz** \\ **CLSID** cuyo nombre es la forma de cadena del GUID. Dado que los controladores de la extensión de Shell son servidores en proceso, debe crear una clave **InProcServer32** en la clave GUID con el valor predeterminado establecido en la ruta de acceso de la dll del controlador. Use el modelo de subprocesos de apartamento.

Cada vez que el shell realiza una acción que puede incluir un controlador de extensión de Shell, comprueba la clave del registro adecuada. La clave bajo la que se registra un controlador de extensión, por lo que controla cuándo se llamará. Por ejemplo, es una práctica común tener un controlador de menú contextual llamado cuando el shell muestra un menú contextual para un miembro de un [tipo de archivo](fa-file-types.md). En este caso, el controlador debe estar registrado en la clave **ProgID** del tipo de archivo.

### <a name="handler-names"></a>Nombres de controlador

Para habilitar un controlador de extensión de Shell, cree una subclave con el nombre de la subclave del controlador (consulte a continuación) en la subclave **ShellEx** del **ProgID** (para tipos de archivo) o el nombre del tipo de objeto de Shell (para [objetos de Shell predefinidos](#predefined-shell-objects)).

Por ejemplo, si desea registrar un controlador de extensión de menú contextual para el programa. 1, comenzaría con la creación de la siguiente subclave:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

En el caso de los siguientes controladores, cree una subclave debajo de la clave "controlador nombre de la subclave" cuyo nombre es la versión de cadena del CLSID de la extensión de Shell. Se pueden registrar varias extensiones en la clave de nombre de la subclave del controlador mediante la creación de varias subclaves.



| Controlador                                               | Interfaz          | Nombre de la subclave del controlador       |
|-------------------------------------------------------|--------------------|---------------------------|
| Controlador del menú contextual                                 | IContextMenu       | **ContextMenuHandlers**   |
| Controlador Copyhook                                      | ICopyHook          | **CopyHookHandlers**      |
| Controlador de arrastrar y colocar                                 | IContextMenu       | **DragDropHandlers**      |
| Controlador de la hoja de propiedades                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Controlador de proveedor de columnas (desusado en Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

En el caso de los siguientes controladores, el valor predeterminado de la clave "nombre de subclave de controlador" es la versión de cadena del CLSID de la extensión de Shell. Solo se puede registrar una extensión para estos controladores.



| Controlador                 | Interfaz                                         | Nombre de la subclave del controlador                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Controlador de datos            | IDataObject                                       | **DataHandler**                            |
| Quitar controlador            | IDropTarget                                       | **DropHandler**                            |
| Controlador de iconos            | IExtractIconA/W                                   | **IconHandler**                            |
| Controlador de imagen           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Controlador de imagen en miniatura | IThumbnailProvider                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Controlador de recuadro informativo         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Vínculo de Shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Vínculo de Shell (Unicode)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Almacenamiento estructurado      | IStorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Metadatos                | IPropertyStore                                    | **PropertyHandler**                        |
| Metadatos                | IPropertySetStorage (en desuso en Windows Vista) | **PropertyHandler**                        |
| Anclar al menú Inicio       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Anclar a la barra de tareas          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Las subclaves especificadas para agregar **anclar al menú Inicio** y **anclar a la barra de tareas** al menú contextual de un elemento solo son necesarias para los tipos de archivo que incluyen la entrada [IsShortCut](./links.md) .

Se ha quitado la compatibilidad con controladores de proveedor de columnas en Windows Vista. Además, a partir de Windows Vista, [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) está en desuso en favor de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

Aunque [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) sigue siendo compatible, se prefiere [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) para Windows Vista y versiones posteriores.

### <a name="predefined-shell-objects"></a>Objetos de Shell predefinidos

El shell define objetos adicionales en **la \_ \_ raíz de las clases HKEY** que se pueden extender de la misma manera que los tipos de archivo. Por ejemplo, para agregar un controlador de hoja de propiedades para todos los archivos, puede registrarse en la clave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

En la tabla siguiente se proporcionan las diversas subclaves de **\_ las clases HKEY \_ raíz** en las que se pueden registrar controladores de extensión. Tenga en cuenta que muchos controladores de extensión no se pueden registrar en todas las subclaves de la lista. Para obtener más información, vea la documentación del controlador específico.



| Subclave                    | Descripción                                                          | Controladores posibles                                | Versión |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\** _                    | Todos los archivos                                                            | Menú contextual, hoja de propiedades, verbos (ver más abajo) | All     |
| _ *AllFileSystemObjects**  | Todos los archivos y carpetas de archivos                                           | Menú contextual, hoja de propiedades, verbos             | 4.71    |
| **Carpeta**                | Todas las carpetas                                                          | Menú contextual, hoja de propiedades, verbos             | All     |
| **Directorio**             | Carpetas de archivos                                                         | Menú contextual, hoja de propiedades, verbos             | All     |
| **Fondo de directorio \\** | Fondo de carpeta de archivos                                               | Solo el menú contextual                               | 4.71    |
| **Unidad**                 | Todas las unidades de mi PC, como "C: \\ "                             | Menú contextual, hoja de propiedades, verbos             | All     |
| **Network**               | Red completa (en mis sitios de red)                             | Menú contextual, hoja de propiedades, verbos             | All     |
| **Tipo de red \\\\\#**     | Todos los objetos de tipo \# (ver más abajo)                                   | Menú contextual, hoja de propiedades, verbos             | 4.71    |
| **NetShare**              | Todos los recursos compartidos de red                                                   | Menú contextual, hoja de propiedades, verbos             | 4.71    |
| **NetServer**             | Todos los servidores de red                                                  | Menú contextual, hoja de propiedades, verbos             | 4.71    |
| *\_nombre del proveedor de red \_* | Todos los objetos proporcionados por el proveedor de red "*\_ \_ nombre de proveedor de red*" | Menú contextual, hoja de propiedades, verbos             | All     |
| **Impresoras**              | Todas las impresoras                                                         | Menú contextual, hoja de propiedades                    | All     |
| **Audio**               | CD de audio en la unidad de CD                                                 | Solo verbos                                       | All     |
| **DISCOS**                   | Unidad de DVD (Windows 2000)                                             | Menú contextual, hoja de propiedades, verbos             | 4.71    |



 

Notas:

-   Para acceder al menú contextual de fondo de la carpeta de archivos, haga clic con el botón secundario en una carpeta de archivos, pero no en el contenido de la carpeta.
-   Los "verbos" son comandos especiales registrados en el verbo de Shell de la subclave **\_ \_ raíz de las clases HKEY** \\  \\  \\  .
-   Para el tipo de **red** \\  \\ **\#** , " \# " es un código de tipo de proveedor de red en formato decimal. El código de tipo de proveedor de red es la palabra alta de un tipo de red. La lista de tipos de red se proporciona en el archivo de encabezado Winnetwk. h ( \_ valores de net WNNC \_ \* ). Por ejemplo, WNNC \_ net \_ Shiva es 0x00330000, por lo que la clave de tipo correspondiente sería **HKEY \_ classes \_ raíz** \\ **Network** \\ **Type** \\ **51** .
-   "*\_ \_ nombre de proveedor de red*" es un nombre de proveedor de red tal y como lo especifica [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), con los espacios convertidos en guiones bajos. Por ejemplo, si se instala el proveedor de red de redes de Microsoft, su nombre de proveedor es "red de Microsoft Windows" y el *\_ \_ nombre de proveedor de red* correspondiente es **\_ \_ red de Microsoft Windows**.

### <a name="example-of-an-extension-handler-registration"></a>Ejemplo de registro de un controlador de extensión

Para habilitar un controlador determinado, cree una subclave en la clave del tipo de controlador de extensión con el nombre del controlador. El shell no utiliza el nombre del controlador, pero debe ser diferente de todos los demás nombres bajo esa subclave de tipo. Establezca el valor predeterminado de la subclave Name en la forma de cadena del GUID del controlador.

En el ejemplo siguiente se muestran las entradas del registro que habilitan los controladores de extensiones de menús contextuales y hojas de propiedades mediante un tipo de archivo. MYP de ejemplo:

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

El procedimiento de registro descrito en esta sección debe seguirse para todos los sistemas de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones para implementar extensiones de In-Process](shell-and-managed-code.md)
</dt> </dl>

 

 

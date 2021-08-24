---
description: Gran parte de la implementación de un objeto de controlador de extensión de Shell viene determinada por su tipo. Sin embargo, hay algunos elementos comunes. En este tema se de abordan los aspectos de implementación que comparten todos los controladores de extensión de Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inicialización de controladores de extensión de shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f83a47400cff5d0fa4628f6f6f9d9ba74b158947c7843f61831d54f62c7a6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661225"
---
# <a name="initializing-shell-extension-handlers"></a>Inicialización de controladores de extensión de shell

Gran parte de la implementación de un objeto de controlador de extensión de Shell viene determinada por su tipo. Sin embargo, hay algunos elementos comunes. En este tema se de abordan los aspectos de implementación que comparten todos los controladores de extensión de Shell.

Todos los controladores de extensión de Shell son objetos del Modelo de objetos componentes (COM) en proceso. Se les debe asignar un GUID y registrarse como se describe [en Registro de controladores de extensión de shell](handlers.md). Se implementan como archivos DLL y deben exportar las siguientes funciones estándar:

-   [**DllMain**](../dlls/dllmain.md). Punto de entrada estándar al archivo DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expone el generador de clases del objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM llama a esta función para determinar si el objeto está atendiendo a algún cliente. Si no es así, el sistema puede descargar el archivo DLL y liberar la memoria asociada.

Al igual que todos los objetos COM, los controladores de extensiones de Shell deben implementar una [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un generador [de clases](../com/implementing-iclassfactory.md). La mayoría también debe implementar una [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en Windows XP o versiones anteriores. Estos se reemplazaron por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) en Windows Vista. El Shell usa estas interfaces para inicializar el controlador.

La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) debe implementarse mediante lo siguiente:

-   Controladores de iconos
-   Controladores de datos
-   Controladores de colocación

La [**interfaz IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) debe implementarse mediante lo siguiente:

-   Controladores de menús contextuales
-   Controladores de arrastrar y colocar
-   Controladores de hoja de propiedades

En el resto de este tema se analizan los siguientes temas:

-   [Implementación de IPersistFile](#implementing-ipersistfile)
-   [Implementación de IShellExtInit](#implementing-ishellextinit)
-   [Personalización de información](#infotip-customization)
-   [Temas relacionados](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementación de IPersistFile

La [**interfaz IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) está diseñada para permitir que un objeto se cargue o guarde en un archivo de disco. Tiene seis métodos además de [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)cinco propios y el [**método GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que hereda de [**IPersist.**](/windows/win32/api/objidl/nn-objidl-ipersist) Con las extensiones de Shell, **IPersist** solo se usa para inicializar un objeto de controlador de extensiones de Shell. Dado que normalmente no es necesario leer o escribir en el disco, solo los métodos **GetClassID** y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requieren una implementación sintoken.

El shell llama [**primero a GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y la función devuelve el identificador de clase (CLSID) del objeto de controlador de extensión. A continuación, el shell [**llama a Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) y pasa dos valores. El primero, *pszFile*, es una cadena Unicode con el nombre del archivo o la carpeta en la que shell está a punto de funcionar. El segundo es *dwMode*, que indica el modo de acceso a archivos. Dado que normalmente no hay necesidad de acceder a los archivos, *dwMode* suele ser cero. El método almacena estos valores según sea necesario para su referencia posterior.

En el fragmento de código siguiente se muestra cómo un controlador de extensión de Shell típico implementa los [**métodos GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) [**y Load.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) Está diseñado para controlar ANSI o Unicode. CLSID SampleExtHandler es el GUID del objeto de controlador de extensión y CSampleShellExtension es el nombre de la clase que se usa \_ para implementar la interfaz . Las variables **m \_ szFileName** y **m \_ dwMode** son variables privadas que se usan para almacenar el nombre del archivo y las marcas de acceso.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

La [**interfaz IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) solo tiene un método, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). El método tiene tres parámetros que el Shell puede usar para pasar varios tipos de información. Los valores pasados en dependen del tipo de controlador y algunos se pueden establecer en **NULL.**

-   *pidlFolder contiene* el puntero de una carpeta a una lista de identificadores de elemento (PIDL). Se trata de un PIDL absoluto. Para las extensiones de hoja de propiedades, este valor es **NULL.** Para las extensiones de menú contextual, es el PIDL de la carpeta que contiene el elemento cuyo menú contextual se muestra. Para los controladores de arrastrar y colocar no predeterminados, es el PIDL de la carpeta de destino.
-   *pDataObject* contiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un objeto de datos. El objeto de datos contiene uno o varios nombres de archivo en [formato CF \_ HDROP.](dragdrop.md)
-   *hRegKey contiene* una clave del Registro para el tipo de carpeta o objeto de archivo.

El [**método IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) almacena el nombre de archivo, el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) y la clave del Registro según sea necesario para su uso posterior. El fragmento de código siguiente muestra una implementación de **IShellExtInit::Initialize**. Para simplificar, en este ejemplo se supone que el objeto de datos contiene solo un archivo. En general, el objeto de datos puede contener varios archivos, cada uno de los cuales tendrá que extraerse.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Personalización de información

Hay dos maneras de personalizar la información. Una manera es implementar un objeto que admita [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) y, a continuación, registrar el objeto en la subclave adecuada en el Registro (consulte a continuación). Como alternativa, puede especificar una cadena fija o una lista de determinadas propiedades de archivo que se mostrarán.

Para mostrar una cadena fija para una extensión de espacio de nombres, cree una subclave denominada **InfoTip** debajo de la clave CLSID de la extensión de espacio de nombres. Establezca los datos de esa subclave como la cadena que desea mostrar.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para mostrar una cadena fija para un tipo de archivo, cree una subclave denominada **InfoTip** debajo de la clave **ProgID** del tipo de archivo para el que desea proporcionar información. Establezca los datos de esa subclave como la cadena que desea mostrar.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Si desea que el Shell muestre determinadas propiedades de archivo en la información sobre un tipo de archivo específico, cree una subclave denominada **InfoTip** debajo de la clave **ProgID** de ese tipo de archivo. Establezca los datos de esa subclave como una lista delimitada por punto y coma de nombres de propiedad canónicos o {fmtid}, pares pid donde *propname* es un nombre de propiedad canónica y *{fmtid}, pid* es un [**par FMTID/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Se pueden usar los siguientes nombres de propiedad.



| Nombre de la propiedad    | Descripción                   | Recuperado de                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autor           | Autor del documento        | [**PIDSI \_ AUTHOR**](../stg/the-summary-information-property-set.md)                             |
| Título            | Título del documento         | [**PIDSI \_ TITLE**](../stg/the-summary-information-property-set.md)                              |
| Asunto          | Resumen del asunto               | [**ASUNTO \_ PIDSI**](../stg/the-summary-information-property-set.md)                            |
| Comentario          | Comentarios de documentos             | [**PIDSI \_ COMMENT**](../stg/the-summary-information-property-set.md) o propiedades de carpetas o unidades |
| PageCount        | Número de páginas               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Nombre             | Nombre descriptivo                 | Vista de carpeta estándar                                                                      |
| OriginalLocation | Ubicación del archivo original     | Carpeta en mal estado y papelera de reciclaje carpeta                                                   |
| DateDeleted      | Archivo de fecha eliminado         | papelera de reciclaje carpeta                                                                        |
| Tipo             | Tipo de archivo                  | Vista de detalles de carpeta estándar                                                              |
| Size             | Tamaño del archivo                  | Vista de detalles de carpeta estándar                                                              |
| SyncCopyIn       | Igual que OriginalLocation      | Igual que OriginalLocation                                                                  |
| Modificado         | Fecha de última modificación            | Vista de detalles de carpeta estándar                                                              |
| Creado          | Fecha de creación                  | Vista de detalles de carpeta estándar                                                              |
| Acceder         | Fecha a la que se ha accedido por última vez            | Vista de detalles de carpeta estándar                                                              |
| InFolder         | Directorio que contiene el archivo | Resultados de la búsqueda de documentos                                                                   |
| Rango             | Calidad de la coincidencia de búsqueda       | Resultados de la búsqueda de documentos                                                                   |
| FreeSpace        | Espacio de almacenamiento disponible       | Unidades de disco                                                                               |
| NumberOfVisits   | Número de visitas              | carpeta Favoritos                                                                          |
| Atributos       | Atributos de archivo               | Vista de detalles de carpeta estándar                                                              |
| Compañía          | Nombre de la compañía                  | [**PIDDSI \_ COMPANY**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Categoría del documento             | [**PIDDSI \_ (CATEGORÍA)**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Copyright multimedia               | [**COPYRIGHT de \_ PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | Archivo de información sobre HTML             | Desktop.ini archivo para la carpeta                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de controladores de extensión de Shell](reg-shell-exts.md)
</dt> </dl>

 

 

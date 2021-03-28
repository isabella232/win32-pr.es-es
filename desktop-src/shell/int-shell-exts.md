---
description: Gran parte de la implementación de un objeto de controlador de extensión de Shell está dictada por su tipo. Sin embargo, hay algunos elementos comunes. En este tema se describen los aspectos de la implementación que comparten todos los controladores de extensión de Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inicializar controladores de extensión de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986050"
---
# <a name="initializing-shell-extension-handlers"></a>Inicializar controladores de extensión de Shell

Gran parte de la implementación de un objeto de controlador de extensión de Shell está dictada por su tipo. Sin embargo, hay algunos elementos comunes. En este tema se describen los aspectos de la implementación que comparten todos los controladores de extensión de Shell.

Todos los controladores de extensión de Shell son objetos de modelo de objetos componentes (COM) en proceso. Se les debe asignar un GUID y registrarse como se describe en [registrar controladores de extensión de Shell](handlers.md). Se implementan como archivos dll y deben exportar las siguientes funciones estándar:

-   [**DllMain**](../dlls/dllmain.md). Punto de entrada estándar al archivo DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expone el generador de clases del objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM llama a esta función para determinar si el objeto atiende a los clientes. De lo contrario, el sistema puede descargar el archivo DLL y liberar la memoria asociada.

Al igual que todos los objetos COM, los controladores de la extensión de Shell deben implementar una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y un [generador de clases](../com/implementing-iclassfactory.md). La mayoría también debe implementar una interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) o [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en Windows XP o versiones anteriores. Se reemplazaron por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) y [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) en Windows Vista. El shell usa estas interfaces para inicializar el controlador.

La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) debe implementarse de la siguiente manera:

-   Controladores de iconos
-   Controladores de datos
-   Quitar controladores

La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) debe implementarse de la siguiente manera:

-   Controladores de menú contextual
-   Controladores de arrastrar y colocar
-   Controladores de hoja de propiedades

En el resto de este tema se tratan los siguientes temas:

-   [Implementar IPersistFile](#implementing-ipersistfile)
-   [Implementación de IShellExtInit](#implementing-ishellextinit)
-   [Personalización de recuadro informativo](#infotip-customization)
-   [Temas relacionados](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementar IPersistFile

La interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) está diseñada para permitir la carga o el almacenamiento de un objeto en un archivo de disco. Tiene seis métodos además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de los suyos propios y el método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que hereda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Con las extensiones de Shell, **IPersist** solo se usa para inicializar un objeto de controlador de extensión de Shell. Dado que normalmente no es necesario leer o escribir en el disco, solo los métodos **GetClassID** y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) requieren una implementación sin token.

El shell llama primero a [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y la función devuelve el identificador de clase (CLSID) del objeto de controlador de extensión. Después, el shell llama a [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) y pasa dos valores. La primera, *pszFile*, es una cadena Unicode con el nombre del archivo o carpeta en el que está a punto de trabajar el shell. La segunda es *dwMode*, que indica el modo de acceso a archivos. Dado que normalmente no es necesario tener acceso a los archivos, *dwMode* suele ser cero. El método almacena estos valores según sea necesario para su posterior referencia.

En el fragmento de código siguiente se muestra cómo un controlador de extensión de Shell típico implementa los métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) y [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Está diseñado para controlar ANSI o Unicode. CLSID \_ SampleExtHandler es el GUID del objeto del controlador de extensión y CSampleShellExtension es el nombre de la clase que se usa para implementar la interfaz. Las variables **m \_ szFileName** y **m \_ dwMode** son variables privadas que se usan para almacenar el nombre y las marcas de acceso del archivo.


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

La interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tiene solo un método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). El método tiene tres parámetros que el shell puede usar para pasar varios tipos de información. Los valores pasados dependen del tipo de controlador y otros pueden establecerse en **null**.

-   *pidlFolder* contiene el puntero de una carpeta a una lista de identificadores de elementos (PIDL). Se trata de una PIDL absoluta. Para las extensiones de la hoja de propiedades, este valor es **null**. En el caso de las extensiones de menú contextual, es el PIDL de la carpeta que contiene el elemento cuyo menú contextual se muestra. En el caso de los controladores no predeterminados de arrastrar y colocar, es el PIDL de la carpeta de destino.
-   *pDataObject* contiene un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de un objeto de datos. El objeto de datos contiene uno o varios nombres de archivo en formato [ \_ HDROP de CF](dragdrop.md) .
-   *hRegKey* contiene una clave del registro para el tipo de carpeta o objeto de archivo.

El método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) almacena el nombre de archivo, el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) y la clave del registro según sea necesario para su uso posterior. En el fragmento de código siguiente se muestra una implementación de **IShellExtInit:: Initialize**. Para simplificar, en este ejemplo se da por supuesto que el objeto de datos contiene un solo archivo. En general, el objeto de datos puede contener varios archivos, cada uno de los cuales tendrá que extraerse.


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



## <a name="infotip-customization"></a>Personalización de recuadro informativo

Hay dos maneras de personalizar recuadros informativos. Una forma consiste en implementar un objeto que admita [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) y, a continuación, registrar el objeto bajo la subclave adecuada en el registro (vea más abajo). Como alternativa, puede especificar una cadena fija o una lista de determinadas propiedades de archivo que se van a mostrar.

Para mostrar una cadena fija para una extensión de espacio de nombres, cree  una subclave denominada recuadro informativo debajo de la clave CLSID de la extensión de espacio de nombres. Establezca los datos de esa subclave en la cadena que desea mostrar.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para mostrar una cadena fija para un tipo de archivo, cree una subclave **denominada** recuadro informativo debajo de la clave **ProgID** del tipo de archivo para el que desea proporcionar recuadros informativos. Establezca los datos de esa subclave en la cadena que desea mostrar.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Si desea que el shell muestre determinadas propiedades de archivo en el recuadro informativo para un tipo de archivo específico  , cree una subclave denominada recuadro informativo debajo de la clave **ProgID** de ese tipo de archivo. Establezca los datos de esa subclave en una lista delimitada por punto y coma de nombres de propiedad canónicos o {fmtid}, pares PID en los que *NombreDePropiedad* es un nombre de propiedad canónico y *{fmtid}, el PID* es un [**par fmtid/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Se pueden usar los siguientes nombres de propiedad.



| Nombre de la propiedad    | Descripción                   | Recuperado de                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autor           | Autor del documento        | [**autor de PIDSI \_**](../stg/the-summary-information-property-set.md)                             |
| Title            | Título del documento         | [**título de PIDSI \_**](../stg/the-summary-information-property-set.md)                              |
| Asunto          | Resumen de asunto               | [**\_asunto PIDSI**](../stg/the-summary-information-property-set.md)                            |
| Comentario          | Comentarios del documento             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propiedades de comentario o carpeta/unidad |
| PageCount        | Número de páginas               | [**PIDSI \_ PAGECOUNT**](../stg/the-summary-information-property-set.md)                          |
| Nombre             | Nombre descriptivo                 | Vista de carpetas estándar                                                                      |
| OriginalLocation | Ubicación del archivo original     | Carpeta de mi maletín y carpeta de la papelera de reciclaje                                                   |
| DateDeleted      | Se eliminó el archivo de fecha         | Carpeta de la papelera de reciclaje                                                                        |
| Tipo             | Tipo de archivo                  | Vista de detalles de carpetas estándar                                                              |
| Tamaño             | Tamaño del archivo                  | Vista de detalles de carpetas estándar                                                              |
| SyncCopyIn       | Igual que OriginalLocation      | Igual que OriginalLocation                                                                  |
| Modificado         | Fecha de última modificación            | Vista de detalles de carpetas estándar                                                              |
| Creado          | Fecha de creación                  | Vista de detalles de carpetas estándar                                                              |
| Acceso         | Fecha de último acceso            | Vista de detalles de carpetas estándar                                                              |
| InFolder         | Directorio que contiene el archivo | Resultados de búsqueda de documentos                                                                   |
| Rango             | Calidad de coincidencia de búsqueda       | Resultados de búsqueda de documentos                                                                   |
| FreeSpace        | Espacio de almacenamiento disponible       | Unidades de disco                                                                               |
| NumberOfVisits   | Número de visitas              | carpeta Favoritos                                                                          |
| Atributos       | Atributos de archivo               | Vista de detalles de carpetas estándar                                                              |
| Compañía          | Nombre de la compañía                  | [**\_empresa PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Category         | Categoría del documento             | [**\_categoría PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Copyright        | Copyright de los medios               | [**COPYRIGHT de PIDMSI \_**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | Archivo recuadro informativo HTML             | Desktop.ini archivo para la carpeta                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrando controladores de extensión de Shell](reg-shell-exts.md)
</dt> </dl>

 

 

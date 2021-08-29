---
description: En este artículo se explica cómo inicializar controladores de propiedades para trabajar con el Windows de propiedades.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inicialización de controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c54c7a1a5e28c5a66e28f8b2470c8f1643678af2a15025a925a5ed5e89336c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353535"
---
# <a name="initializing-property-handlers"></a>Inicialización de controladores de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el Windows de propiedades.

Este tema se organiza de la siguiente manera:

-   [Controladores de propiedades](#property-handlers)
-   [Antes de comenzar](#before-you-begin)
-   [Inicialización de controladores de propiedades](#initializing-property-handlers)
-   [In-Memory Almacén de propiedades](#in-memory-property-store)
-   [Tratar con PROPVARIANT-Based valores](#dealing-with-propvariant-based-values)
-   [Admitir metadatos abiertos](#supporting-open-metadata)
-   [Contenido de texto completo](#full-text-contents)
-   [Proporcionar valores para propiedades](#providing-values-for-properties)
-   [Reescribición de valores](#writing-back-values)
-   [Implementación de IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registro y distribución de controladores de propiedades](#registering-and-distributing-property-handlers)
-   [Temas relacionados](#related-topics)

## <a name="property-handlers"></a>Controladores de propiedades

Los controladores de propiedades son una parte fundamental del sistema de propiedades. El indexador los invoca en proceso para leer e indexar los valores de propiedad, y también se invocan mediante el Explorador de Windows en proceso para leer y escribir valores de propiedad directamente en los archivos. Estos controladores deben escribirse y probarse cuidadosamente para evitar un rendimiento degradado o la pérdida de datos en los archivos afectados. Para obtener más información sobre las consideraciones específicas del indexador que afectan a la implementación del controlador de propiedades, vea [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

En este tema se describe un formato de archivo basado en XML de ejemplo que describe una receta con una extensión de nombre de archivo .recipe. La extensión de nombre de archivo .recipe se registra como su propio formato de archivo distinto en lugar de basarse en el formato de archivo .xml más genérico, cuyo controlador usa una secuencia secundaria para almacenar propiedades. Se recomienda registrar extensiones de nombre de archivo únicas para los tipos de archivo.

## <a name="before-you-begin"></a>Antes de empezar

Los controladores de propiedades son objetos COM que crean la abstracción [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para un formato de archivo específico. Leen (analizan) y escriben este formato de archivo de forma que se ajuste a su especificación. Algunos controladores de propiedades hacen su trabajo en función de las API que abstraen el acceso a un formato de archivo específico. Antes de desarrollar un controlador de propiedades para el formato de archivo, debe comprender cómo almacena las propiedades el formato de archivo y cómo esas propiedades (nombres y valores) se asignan a la abstracción del almacén de propiedades.

Al planear la implementación, recuerde que los controladores de propiedades son componentes de bajo nivel que se cargan en el contexto de procesos como el Explorador de Windows, el indexador de Windows Search y aplicaciones de terceros que usan el modelo de programación de elementos de Shell. Como resultado, los controladores de propiedades no se pueden implementar en código administrado y deben implementarse en C++. Si el controlador usa alguna API o servicio para realizar su trabajo, debe asegurarse de que esos servicios pueden funcionar correctamente en los entornos en los que se carga el controlador de propiedades.

> [!Note]  
> Los controladores de propiedades siempre están asociados a tipos de archivo específicos; Por lo tanto, si el formato de archivo contiene propiedades que requieren un controlador de propiedades personalizado, siempre debe registrar una extensión de nombre de archivo única para cada formato de archivo.

 

## <a name="initializing-property-handlers"></a>Inicialización de controladores de propiedades

Antes de que el sistema utilice una propiedad, se inicializa mediante una llamada a una implementación de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). El controlador de propiedades se debe inicializar haciendo que el sistema le asigne una secuencia en lugar de dejar esa asignación a la implementación del controlador. Este método de inicialización garantiza lo siguiente:

-   El controlador de propiedades se puede ejecutar en un proceso restringido (una característica de seguridad importante) sin tener derechos de acceso para leer o escribir archivos directamente, en lugar de tener acceso a su contenido a través de la secuencia.
-   Se puede confiar en el sistema para controlar correctamente los bloqueos de archivos, lo que es una medida de confiabilidad importante.
-   El sistema de propiedades proporciona un servicio de guardado seguro automático sin ninguna funcionalidad adicional necesaria en la implementación del controlador de propiedades. Consulte la [sección Escribir valores](#writing-back-values) para obtener más información sobre las secuencias.
-   El uso de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrae la implementación de los detalles del sistema de archivos. Esto permite al controlador admitir la inicialización a través de almacenamientos alternativos, como una carpeta protocolo de transferencia de archivos (FTP) o un archivo comprimido con una extensión de nombre .zip archivo.

Hay casos en los que no es posible inicializar con secuencias. En esas situaciones, hay dos interfaces más que los controladores de propiedades pueden implementar: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Si un controlador de propiedades no implementa [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), debe dejar de ejecutarse en el proceso aislado en el que el indexador del sistema lo colocaría de forma predeterminada si se produjera un cambio en la secuencia. Para no participar en esta característica, establezca el siguiente valor del Registro.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Sin embargo, es mucho mejor implementar [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) y realizar una inicialización basada en secuencias. Como resultado, el controlador de propiedades será más seguro y confiable. La deshabilitación del aislamiento de procesos generalmente está pensada solo para los controladores de propiedades heredados y debe evitarse de forma continuada con cualquier código nuevo.

Para examinar la implementación de un controlador de propiedades en detalle, examine el ejemplo de código siguiente, que es una implementación de [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). El controlador se inicializa cargando un documento de receta basado en XML a través de un puntero a la instancia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) asociada de ese documento. La variable **\_ spDocEle** usada cerca del final del ejemplo de código se definió anteriormente en el ejemplo como MSXML2::IXMLDOMElementPtr.

> [!Note]  
> Los ejemplos de código siguientes y todos los siguientes se toman del ejemplo de controlador de recetas incluido en Windows Software Development Kit (SDK). .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

Una vez cargado el propio documento, las propiedades que se van a mostrar en Windows Explorer se cargan mediante una llamada al método **\_ LoadProperties** protegido, como se muestra en el ejemplo de código siguiente. Este proceso se examina en detalle en la sección siguiente.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Si la secuencia es de solo lectura pero el parámetro *grfMode* contiene la marca STGM READWRITE, la inicialización debe producir un error y devolver \_ STG \_ E \_ ACCESSDENIED. Sin esta comprobación, Windows Explorer muestra los valores de propiedad como grabables aunque no lo estén, lo que conduce a una experiencia confusa del usuario final.

El controlador de propiedades se inicializa solo una vez en su duración. Si se solicita una segunda inicialización, el controlador debe devolver `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>In-Memory Almacén de propiedades

Antes de ver la implementación de **\_ LoadProperties,** debe comprender la matriz **PropertyMap** que se usa en el ejemplo para asignar propiedades del documento XML a propiedades existentes en el sistema de propiedades a través de sus valores PKEY.

No debe exponer todos los elementos y atributos del archivo XML como una propiedad. En su lugar, seleccione solo aquellos que cree que serán útiles para los usuarios finales en la organización de sus documentos (en este caso, recetas). Este es un concepto importante que se debe tener en cuenta al desarrollar los controladores de propiedades: la diferencia entre la información que es realmente útil para escenarios organizativos y la información que pertenece a los detalles del archivo y se puede ver abriendo el propio archivo. Las propiedades no pretenden ser una duplicación completa de un archivo XML.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Esta es la implementación completa del **\_ método LoadProperties** llamado por [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



El **\_ método LoadProperties** llama a la función auxiliar de Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un almacén de propiedades en memoria (caché) para las propiedades administradas. Mediante el uso de una memoria caché, se realiza un seguimiento de los cambios. Esto le libera del seguimiento de si se ha cambiado un valor de propiedad en la memoria caché, pero aún no se ha guardado en el almacenamiento persistente. También le libera de conservar valores de propiedad que no han cambiado.

El **\_ método LoadProperties** también llama **\_ a LoadProperty** cuya implementación se ilustra en el código siguiente) una vez para cada propiedad asignada. **\_ LoadProperty** obtiene el valor de la propiedad tal como se especifica en el elemento **PropertyMap** del flujo XML y lo asigna a la memoria caché en memoria mediante una llamada a [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). La marca PSC NORMAL de la llamada a \_ **IPropertyStoreCache::SetValueAndState** indica que el valor de propiedad no se ha modificado desde el momento en que entró en la memoria caché.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Tratar con PROPVARIANT-Based valores

En la implementación de **\_ LoadProperty**, se proporciona un valor de propiedad en forma de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Se proporciona un conjunto de API en el kit de desarrollo de software (SDK) para convertir de tipos primitivos como **PWSTR** o **int** a o desde **tipos PROPVARIANT.** Estas API se encuentran en Propvarutil.h.

Por ejemplo, para convertir [**propVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en una cadena, puede usar [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) como se muestra aquí.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Para inicializar propVARIANT a partir de una cadena, puede usar [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Como puede ver en cualquiera de los archivos de receta incluidos en el ejemplo, puede haber más de una palabra clave en cada archivo. Para tener en cuenta esto, el sistema de propiedades admite cadenas multivalor representadas como un vector de cadenas (por ejemplo, "VT \_ VECTOR \| VT \_ LPWSTR"). El **\_ método LoadVectorProperty** del ejemplo usa valores basados en vectores.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Si no existe un valor en el archivo, no devuelva un error. En su lugar, establezca el valor en VT \_ EMPTY y devuelva S **\_ OK**. VT \_ EMPTY indica que el valor de propiedad no existe.

## <a name="supporting-open-metadata"></a>Admitir metadatos abiertos

En este ejemplo se usa un formato de archivo basado en XML. Su esquema se puede extender para admitir propiedades que no se pensaron durante el desarrollo, por ejemplo. Este sistema se conoce como metadatos abiertos. En este ejemplo se amplía el sistema de propiedades mediante la creación de un nodo bajo el elemento **Recipe** denominado **ExtendedProperties**, como se muestra en el ejemplo de código siguiente.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Para cargar las propiedades extendidas persistentes durante la inicialización, implemente el **\_ método LoadExtendedProperties,** como se muestra en el ejemplo de código siguiente.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



Las API de serialización declaradas en Propsys.h se usan para serializar y deserializar tipos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en blobs de datos y, a continuación, se usa la codificación Base64 para serializar esos blobs en cadenas que se pueden guardar en el XML. Estas cadenas se almacenan en el atributo **EncodedValue** del **elemento ExtendedProperties.** El siguiente método de utilidad, implementado en el archivo Util.cpp del ejemplo, realiza la serialización. Comienza con una llamada a la función [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) para realizar la serialización binaria, como se muestra en el ejemplo de código siguiente.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



A continuación, [**la función Â CryptBinaryToString,**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)declarada en Wincrypt.h, realiza la conversión de Base64.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



La **función DeserializePropVariantFromString,** que también se encuentra en Util.cpp, invierte la operación y deserializa los valores del archivo XML.

Para obtener información sobre la compatibilidad con metadatos abiertos, vea "Tipos de archivo que admiten metadatos abiertos" en [Tipos de archivo](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Full-Text contenido

Los controladores de propiedades también pueden facilitar una búsqueda de texto completo del contenido del archivo y son una manera sencilla de proporcionar esa funcionalidad si el formato de archivo no es demasiado complicado. Hay una manera alternativa y más eficaz de proporcionar el texto completo del archivo a través de la implementación de la interfaz [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)

En la tabla siguiente se resumen las ventajas de cada enfoque mediante [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)



| Capacidad                                   | Ifilter                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| ¿Permite la reescribición en archivos?                  | No                           | Sí            |
| ¿Proporciona combinación de contenido y propiedades?      | Sí                          | Sí            |
| ¿Multilingüe?                                | Sí                          | No             |
| ¿MIME/Embedded?                               | Sí                          | No             |
| ¿Límites de texto?                             | Oración, párrafo, capítulo | Ninguno           |
| ¿Implementación compatible con SPS/SQL Server? | Sí                          | No             |
| Implementación                               | Complex                      | Simple         |



 

En el ejemplo de controlador de recetas, el formato de archivo de receta no tiene requisitos complejos, por lo que solo se ha implementado [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para la compatibilidad con texto completo. La búsqueda de texto completo se implementa para los nodos XML denominados en la siguiente matriz.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



El sistema de propiedades contiene la propiedad (Contenido de búsqueda PKEY), que se creó para proporcionar contenido `System.Search.Contents` de texto completo al \_ \_ indexador. El valor de esta propiedad nunca se muestra directamente en la interfaz de usuario; el texto de todos los nodos XML denominados en la matriz anterior se concatena en una sola cadena. Después, esa cadena se proporciona al indexador como contenido de texto completo del archivo de receta mediante una llamada a [**IPropertyStoreCache::SetValueAndState,**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) como se muestra en el ejemplo de código siguiente.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Proporcionar valores para propiedades

Cuando se usa para leer valores, normalmente se invocan controladores de propiedades por una de las razones siguientes:

-   Para enumerar todos los valores de propiedad.
-   Para obtener el valor de una propiedad específica.

En el caso de la enumeración, se pide a un controlador de propiedades que enumere sus propiedades durante la indexación o cuando el cuadro de diálogo de propiedades solicita que las propiedades se muestren en **el grupo** Otros. La indexación continúa constantemente como una operación en segundo plano. Cada vez que cambia un archivo, se notifica al indexador y se vuelve a indexar el archivo solicitando al controlador de propiedades que enumere sus propiedades. Por lo tanto, es fundamental que los controladores de propiedades se implementen de forma eficaz y devuelvan valores de propiedad lo más rápido posible. Enumera todas las propiedades para las que tiene valores, igual que lo haría para cualquier colección, pero no enumera las propiedades que implican cálculos con un uso intensivo de memoria o solicitudes de red que podrían ralentizar su recuperación.

Al escribir un controlador de propiedades, normalmente debe tener en cuenta los dos conjuntos de propiedades siguientes.

-   Propiedades principales: propiedades que el tipo de archivo admite de forma nativa. Por ejemplo, un controlador de propiedades de foto para metadatos de archivo de imagen intercambiable (EXIF) admite de forma nativa `System.Photo.FNumber` .
-   Propiedades extendidas: propiedades que admite el tipo de archivo como parte de los metadatos abiertos.

Dado que el ejemplo usa la memoria caché en memoria, la implementación de métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) es simplemente una cuestión de delegar en esa memoria caché, como se muestra en el ejemplo de código siguiente.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Si decide no delegar en la memoria caché en memoria, debe implementar los métodos para proporcionar> el siguiente comportamiento esperado:

-   [**IPropertyStore::GetCount:**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))si no hay ninguna propiedad, este método devuelve **S \_ OK**.
-   [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): si *iProp* es mayor o igual que *cProps*, este método devuelve E INVALIDARG y la estructura a la que apunta el parámetro pkey se rellena con \_ ceros. 
-   [**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) [**e IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflejan el estado actual del controlador de propiedades. Si se agrega o quita [**un PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) del archivo a través de [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), estos dos métodos deben reflejar ese cambio la próxima vez que se llamen.
-   [**IPropertyStore::GetValue:**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))si se solicita a este método un valor que no existe, devuelve **S \_ OK** con el valor notificado como VT \_ EMPTY.

## <a name="writing-back-values"></a>Escritura de valores devueltos

Cuando el controlador de propiedades escribe el valor de una propiedad mediante [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), no escribe el valor en el archivo hasta que se llama a [**IPropertyStore::Commit.**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) La memoria caché en memoria puede ser útil para implementar este esquema. En el código de ejemplo, la implementación **de IPropertyStore::SetValue** simplemente establece el nuevo valor en la memoria caché en memoria y establece el estado de esa propiedad en PSC \_ DIRTY.


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



En cualquier [**implementación de IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) se espera el comportamiento siguiente de [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Si la propiedad ya existe, se establece el valor de la propiedad .
-   Si la propiedad no existe, se agrega la nueva propiedad y su valor establecido.
-   Si el valor de propiedad no se puede conservar con la misma precisión que se ha especificado (por ejemplo, truncamiento debido a limitaciones de tamaño en el formato de archivo), el valor se establece en la medida de lo posible y se devuelve INPLACE \_ S \_ TRUNCATED.
-   Si el controlador de propiedades no admite la propiedad, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` se devuelve .
-   Si hay otra razón por la que no se puede establecer el valor de propiedad, como el archivo bloqueado o la falta de derechos para editar mediante listas de control de acceso (ACL), se devuelve STG \_ E \_ ACCESSDENIED.

Una ventaja importante del uso de secuencias, como ejemplo, es la confiabilidad. Los controladores de propiedades siempre deben tener en cuenta que no pueden dejar un archivo en un estado incoherente en caso de error catastrófico. Obviamente, se debe evitar dañar los archivos de un usuario y la mejor manera de hacerlo es mediante un mecanismo de "copia en escritura". Si el controlador de propiedades usa una secuencia para acceder a un archivo, este comportamiento se obtiene automáticamente. el sistema escribe los cambios en la secuencia, reemplazando el archivo por la nueva copia solo durante la operación de confirmación.

Para invalidar este comportamiento y controlar manualmente el proceso de guardado de archivos, puede rechazar el comportamiento de guardado seguro estableciendo el valor ManualSafeSave en la entrada del Registro del controlador, como se muestra aquí.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Cuando un controlador especifica el valor ManualSafeSave, la secuencia con la que se inicializa no es una secuencia con transacciones (STGM \_ TRANSACTED). El propio controlador debe implementar la función de guardado seguro para asegurarse de que el archivo no está dañado si se interrumpe la operación de guardado. Si el controlador implementa la escritura local, escribirá en la secuencia que se le ha dado. Si el controlador no admite esta característica, debe recuperar una secuencia con la que escribir la copia actualizada del archivo mediante [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Una vez que el controlador haya terminado de escribir, debe llamar a [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) en la secuencia original para completar la operación y reemplazar el contenido de la secuencia original por la nueva copia del archivo.

ManualSafeSave también es la situación predeterminada si no inicializa el controlador con una secuencia. Sin una secuencia original para recibir el contenido de la secuencia temporal, debe usar [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) para realizar un reemplazo atómico del archivo de origen.

Los formatos de archivo de gran tamaño que se usarán de forma que produzcan archivos mayores de 1 MB deben implementar la compatibilidad con la escritura de propiedades locales. de lo contrario, el comportamiento de rendimiento no cumple las expectativas de los clientes del sistema de propiedades. En este escenario, el tiempo necesario para escribir propiedades no debe verse afectado por el tamaño del archivo.

Para archivos muy grandes, por ejemplo, un archivo de vídeo de 1 GB o más, se requiere una solución diferente. Si no hay suficiente espacio en el archivo para realizar la escritura local, el controlador puede producir un error en la actualización de la propiedad si se ha agotado la cantidad de espacio reservado para la escritura de propiedades en el lugar. Este error se produce para evitar un rendimiento deficiente derivado de 2 GB de E/S (1 para lectura y 1 para escritura). Debido a este posible error, estos formatos de archivo deben reservar espacio suficiente para la escritura de propiedades en el lugar.

Si el archivo tiene suficiente espacio en su encabezado para escribir metadatos y si la escritura de los metadatos no hace que el archivo crezca o se reduzca, podría ser seguro escribir en su lugar. Se recomiendan 64 KB como punto de partida. Escribir en el lugar es equivalente al controlador que solicita ManualSafeSave y llama a [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) en la implementación de [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))y tiene un rendimiento mucho mejor que copiar en escritura. Si el tamaño del archivo cambia debido a cambios en el valor de propiedad, no se debe intentar escribir en el lugar debido a la posibilidad de que haya un archivo dañado en caso de una terminación anómala.

> [!Note]  
> Por motivos de rendimiento, se recomienda usar la opción ManualSafeSave con controladores de propiedades que trabajen con archivos de 100 KB o más.

 

Como se muestra en la siguiente implementación de ejemplo de [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), el controlador de ManualSafeSave se registra para ilustrar la opción de guardado seguro manual. El **\_ método SaveCacheToDom** escribe los valores de propiedad almacenados en la memoria caché en el objeto XMLdocument.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



A continuación, pregunte si admite [**IDestinationStreamFactory.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



A continuación, confirme la secuencia original, que vuelve a escribir los datos en el archivo original de forma segura.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



A continuación, **\_ examine la implementación de SaveCacheToDom.**


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



A continuación, obtenga el número de propiedades almacenadas en la memoria caché en memoria.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Ahora, recorre en iteración las propiedades para determinar si el valor de una propiedad se ha cambiado desde que se cargó en la memoria.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



El [**método IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) obtiene el estado de la propiedad en la memoria caché. La marca PSC DIRTY, que se estableció en la implementación \_ [**de IPropertyStore::SetValue,**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) marca una propiedad como modificada.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Asigne la propiedad al nodo XML como se especifica en la **\_ matriz rgPropertyMap.**


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Si una propiedad no está en el mapa, es una nueva propiedad establecida por Windows Explorer. Dado que se admiten metadatos abiertos, guarde la nueva propiedad en la **sección ExtendedProperties** del XML.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Implementación de IPropertyStoreCapabilities

[**IPropertyStoreCapabilities informa**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) a la interfaz de usuario de Shell si se puede editar una propiedad determinada en la interfaz de usuario de Shell. Es importante tener en cuenta que esto solo se relaciona con la capacidad de editar la propiedad en la interfaz de usuario, no si se puede llamar correctamente a [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) en la propiedad . Una propiedad que provoca un valor devuelto de S FALSE de \_ [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) puede seguir siendo capaz de establecerse a través de una aplicación.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) devuelve **S \_ OK** para indicar que los usuarios finales deben tener permiso para editar la propiedad directamente; S \_ FALSE indica que no deben hacerlo. S \_ FALSE puede significar que las aplicaciones son responsables de escribir la propiedad, no de los usuarios. El Shell deshabilita los controles de edición según corresponda en función de los resultados de las llamadas a este método. Se supone que un controlador que no implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) admite metadatos abiertos mediante la compatibilidad con la escritura de cualquier propiedad.

Si está creando un controlador que controla solo las propiedades de solo lectura, debe implementar el método **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem o**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) para que devuelva STG E ACCESSDENIED cuando se llame con la marca \_ \_ \_ STGM READWRITE.

Algunas propiedades tienen su [atributo isInnate](./propdesc-schema-typeinfo.md) establecido en **true.** Las propiedades innate tienen las siguientes características:

-   La propiedad normalmente se calcula de alguna manera. Por ejemplo, `System.Image.BitDepth` se calcula a partir de la propia imagen.
-   Cambiar la propiedad no tendría sentido sin cambiar el archivo. Por ejemplo, cambiar no cambiaría el tamaño de la imagen, por lo que no tiene sentido permitir que `System.Image.Dimensions` el usuario la cambie.
-   En algunos casos, el sistema proporciona automáticamente estas propiedades. Algunos ejemplos son , que proporciona el sistema de archivos, y , que se basa en quién `System.DateModified` comparte el archivo el `System.SharedWith` usuario.

Debido a estas características, las propiedades marcadas como *IsInnate* se proporcionan al usuario en la interfaz de usuario de Shell solo como propiedades de solo lectura. Si una propiedad está marcada como *IsInnate,* el sistema de propiedades no almacena esa propiedad en el controlador de propiedades. Por lo tanto, los controladores de propiedades no necesitan código especial para tener en cuenta estas propiedades en sus implementaciones. Si el valor del *atributo IsInnate* no se indica explícitamente para una propiedad determinada, el valor predeterminado es **false.**

## <a name="registering-and-distributing-property-handlers"></a>Registro y distribución de controladores de propiedades

Con el controlador de propiedades implementado, se debe registrar y su extensión de nombre de archivo asociada al controlador. Para obtener más información, vea [Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registro y distribución de controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 

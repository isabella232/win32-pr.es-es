---
description: En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inicializar controladores de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277066"
---
# <a name="initializing-property-handlers"></a>Inicializar controladores de propiedades

En este tema se explica cómo crear y registrar controladores de propiedades para trabajar con el sistema de propiedades de Windows.

Este tema se organiza de la siguiente manera:

-   [Controladores de propiedades](#property-handlers)
-   [Antes de comenzar](#before-you-begin)
-   [Inicializar controladores de propiedades](#initializing-property-handlers)
-   [Almacén de propiedades en memoria](#in-memory-property-store)
-   [Trabajar con PROPVARIANT-Based valores](#dealing-with-propvariant-based-values)
-   [Compatibilidad con metadatos abiertos](#supporting-open-metadata)
-   [Contenido de texto completo](#full-text-contents)
-   [Proporcionar valores para las propiedades](#providing-values-for-properties)
-   [Escribir valores hacia atrás](#writing-back-values)
-   [Implementación de IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrar y distribuir controladores de propiedades](#registering-and-distributing-property-handlers)
-   [Temas relacionados](#related-topics)

## <a name="property-handlers"></a>Controladores de propiedades

Los controladores de propiedades son una parte fundamental del sistema de propiedades. El indexador los invoca en proceso para leer e indexar los valores de propiedad, y el explorador de Windows también los invoca en el proceso para leer y escribir los valores de propiedad directamente en los archivos. Estos controladores deben escribirse y probarse cuidadosamente para evitar el rendimiento degradado o la pérdida de datos en los archivos afectados. Para obtener más información sobre las consideraciones específicas del indexador que afectan a la implementación del controlador de propiedades, vea [desarrollar controladores de propiedades para Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

En este tema se describe un ejemplo de formato de archivo basado en XML que describe una receta con una extensión de nombre de archivo. receta. La extensión de nombre de archivo. Recipe se registra como su propio formato de archivo distinto en lugar de basarse en el formato de archivo. XML más genérico, cuyo controlador usa un flujo secundario para almacenar propiedades. Se recomienda registrar las extensiones de nombre de archivo únicas para los tipos de archivo.

## <a name="before-you-begin"></a>Antes de empezar

Los controladores de propiedades son objetos COM que crean la abstracción [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para un formato de archivo específico. Leen (analizan) y escriben este formato de archivo de forma que se ajuste a su especificación. Algunos controladores de propiedades realizan su trabajo en función de las API que abstraen el acceso a un formato de archivo específico. Antes de desarrollar un controlador de propiedades para el formato de archivo, debe comprender cómo el formato de archivo almacena las propiedades y cómo se asignan esas propiedades (nombres y valores) en la abstracción del almacén de propiedades.

Al planear la implementación, recuerde que los controladores de propiedades son componentes de bajo nivel que se cargan en el contexto de procesos como el explorador de Windows, el indizador de Windows Search y aplicaciones de terceros que utilizan el modelo de programación de elementos de Shell. Como resultado, los controladores de propiedades no se pueden implementar en código administrado y deben implementarse en C++. Si el controlador usa cualquier API o servicio para realizar su trabajo, debe asegurarse de que esos servicios pueden funcionar correctamente en los entornos en los que se carga el controlador de propiedades.

> [!Note]  
> Los controladores de propiedades siempre se asocian a tipos de archivo específicos; por lo tanto, si el formato de archivo contiene propiedades que requieren un controlador de propiedades personalizado, debe registrar siempre una extensión de nombre de archivo única para cada formato de archivo.

 

## <a name="initializing-property-handlers"></a>Inicializar controladores de propiedades

Antes de que el sistema use una propiedad, se inicializa llamando a una implementación de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). El controlador de propiedad debe inicializarse haciendo que el sistema lo asigne a una secuencia en lugar de dejar esa asignación a la implementación del controlador. Este método de inicialización garantiza lo siguiente:

-   El controlador de propiedades puede ejecutarse en un proceso restringido (una característica de seguridad importante) sin tener derechos de acceso para leer o escribir archivos directamente, en lugar de tener acceso a su contenido a través de la secuencia.
-   Se puede confiar en el sistema para controlar el archivo bloqueos oportunistas correctamente, que es una medida de confiabilidad importante.
-   El sistema de propiedades proporciona un servicio de almacenamiento seguro automático sin ninguna funcionalidad adicional requerida por la implementación del controlador de propiedad. Para obtener más información sobre las secuencias, consulte la sección [escritura de valores de reserva](#writing-back-values) .
-   El uso de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrae la implementación de los detalles del sistema de archivos. Esto permite al controlador admitir la inicialización a través de almacenamientos alternativos, como una carpeta de protocolo de transferencia de archivos (FTP) o un archivo comprimido con la extensión de nombre de archivo. zip.

Hay casos en los que no es posible la inicialización con secuencias. En esas situaciones, hay dos interfaces adicionales que los controladores de propiedades pueden implementar: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) y [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Si un controlador de propiedad no implementa [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), debe dejar de ejecutarse en el proceso aislado en el que el indexador del sistema la colocaría de forma predeterminada si se produjeron cambios en la secuencia. Para no participar en esta característica, establezca el siguiente valor del registro.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

Sin embargo, es mucho mejor implementar [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) y realizar una inicialización basada en streaming. El controlador de propiedades será más seguro y confiable como resultado. Generalmente, la deshabilitación del aislamiento de procesos está destinada únicamente a los controladores de propiedades heredadas y se debe evitar por cualquier nuevo código.

Para examinar la implementación de un controlador de propiedades en detalle, examine el siguiente ejemplo de código, que es una implementación de [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). El controlador se inicializa cargando un documento receta basado en XML a través de un puntero a la instancia de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) asociada de ese documento. La variable **\_ spDocEle** que se usa cerca del final del ejemplo de código se define anteriormente en el ejemplo como MSXML2:: IXMLDOMElementPtr.

> [!Note]  
> Lo siguiente y todos los ejemplos de código siguientes se han tomado del ejemplo de controlador de recetas incluido en el kit de desarrollo de software (SDK) de Windows. .

 


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



Ti 

Una vez cargado el propio documento, las propiedades que se van a mostrar en el explorador de Windows se cargan llamando al método **\_ LoadProperties** protegido, como se muestra en el ejemplo de código siguiente. Este proceso se examina en detalle en la sección siguiente.


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



Si el flujo es de solo lectura, pero el parámetro *grfMode* contiene la \_ marca ReadWrite de STGM, se debe producir un error en la inicialización y devolver STG \_ E \_ ACCESSDENIED. Sin esta comprobación, el explorador de Windows muestra los valores de propiedad como de escritura, aunque no lo hacen, lo que provoca una experiencia de usuario final confusa.

El controlador de propiedad se inicializa una sola vez en su duración. Si se solicita una segunda inicialización, el controlador debe devolver `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>In-Memory almacén de propiedades

Antes de examinar la implementación de **\_ LoadProperties**, debe comprender la matriz **PropertyMap** utilizada en el ejemplo para asignar las propiedades del documento XML a las propiedades existentes en el sistema de propiedades a través de sus valores PKEY.

No debe exponer todos los elementos y atributos del archivo XML como una propiedad. En su lugar, seleccione solo aquellos que cree que serán útiles para los usuarios finales de la organización de sus documentos (en este caso, recetas). Este es un concepto importante que hay que tener en cuenta al desarrollar los controladores de propiedades: la diferencia entre la información que es realmente útil para los escenarios de la organización y la información que pertenece a los detalles del archivo y se puede ver abriendo el propio archivo. Las propiedades no pretenden ser una duplicación completa de un archivo XML.


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



Esta es la implementación completa del método **\_ LoadProperties** llamado por [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


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



El método **\_ LoadProperties** llama a la función auxiliar de Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un almacén de propiedades en memoria (caché) para las propiedades controladas. Mediante el uso de una memoria caché, se realiza un seguimiento de los cambios. Esto le libera del seguimiento de si se ha cambiado un valor de propiedad en la memoria caché, pero aún no se ha guardado en el almacenamiento persistente. También le libera de la persistencia innecesaria de valores de propiedad que no han cambiado.

El método **\_ LoadProperties** también llama a **\_ LoadProperty** cuya implementación se muestra en el código siguiente) una vez para cada propiedad asignada. **\_ LoadProperty** obtiene el valor de la propiedad tal y como se especifica en el elemento **PROPERTYMAP** de la secuencia XML y lo asigna a la memoria caché en memoria a través de una llamada a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). La \_ marca de PSC normal en la llamada a **IPropertyStoreCache:: SetValueAndState** indica que el valor de propiedad no se ha modificado desde el momento en que entró en la memoria caché.


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



## <a name="dealing-with-propvariant-based-values"></a>Trabajar con PROPVARIANT-Based valores

En la implementación de **\_ LoadProperty**, se proporciona un valor de propiedad en forma de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Se proporciona un conjunto de API en el kit de desarrollo de software (SDK) para convertir tipos primitivos como **PWSTR** o **int** a o desde tipos **PROPVARIANT** . Estas API se encuentran en Propvarutil. h.

Por ejemplo, para convertir un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en una cadena, puede usar [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) como se muestra aquí.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Para inicializar un PROPVARIANT de una cadena, puede usar [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Como puede ver en cualquiera de los archivos de recetas incluidos en el ejemplo, puede haber más de una palabra clave en cada archivo. Para tener en cuenta esto, el sistema de propiedades admite cadenas de varios valores que se representan como un vector de cadenas (por ejemplo, "VT \_ Vector \| VT \_ LPWStr"). El método **\_ LoadVectorProperty** del ejemplo utiliza valores basados en vectores.


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



Si un valor no existe en el archivo, no devuelva un error. En su lugar, establezca el valor en VT \_ vacío y devuelva los valores **\_ correctos**. VT \_ vacío indica que el valor de la propiedad no existe.

## <a name="supporting-open-metadata"></a>Compatibilidad con metadatos abiertos

En este ejemplo se usa un formato de archivo basado en XML. Su esquema se puede extender para admitir propiedades que no se han considerado durante developmet, por ejemplo. Este sistema se conoce como metadatos abiertos. En este ejemplo se amplía el sistema de propiedades mediante la creación de un nodo bajo el elemento **Recipe** denominado **ExtendedProperties**, como se muestra en el ejemplo de código siguiente.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Para cargar propiedades extendidas persistentes durante la inicialización, implemente el método **\_ LoadExtendedProperties** , como se muestra en el ejemplo de código siguiente.


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



Las API de serialización declaradas en propsys. h se utilizan para serializar y deserializar los tipos de [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en blobs de datos y, a continuación, se usa la codificación base64 para serializar esos blobs en cadenas que se pueden guardar en el XML. Estas cadenas se almacenan en el atributo **EncodedValue** del elemento **ExtendedProperties** . El siguiente método de utilidad, implementado en el archivo util. cpp del ejemplo, realiza la serialización. Comienza con una llamada a la función [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) para realizar la serialización binaria, como se muestra en el ejemplo de código siguiente.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



A continuación, la función [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa), declarada en Wincrypt. h, realiza la conversión Base64.


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



La función **DeserializePropVariantFromString** , que también se encuentra en util. cpp, invierte la operación y deserializa los valores del archivo XML.

Para obtener información sobre la compatibilidad con los metadatos abiertos, vea "tipos de archivo que admiten metadatos abiertos" en [tipos de archivo](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Contenido de Full-Text

Los controladores de propiedades también pueden facilitar una búsqueda de texto completo del contenido del archivo, y son una manera sencilla de proporcionar esa funcionalidad si el formato del archivo no es demasiado complicado. Existe una forma alternativa y más eficaz de proporcionar el texto completo del archivo a través de la implementación de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

En la tabla siguiente se resumen las ventajas de cada enfoque mediante [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) o [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).



| Capacidad                                   | Imaging                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| ¿Permite la escritura de datos en archivos?                  | No                           | Sí            |
| ¿Proporciona una combinación de contenido y propiedades?      | Sí                          | Sí            |
| Entornos?                                | Sí                          | No             |
| ¿MIME/Embedded?                               | Sí                          | No             |
| ¿Límites de texto?                             | Oración, párrafo, capítulo | None           |
| ¿La implementación es compatible con SP/SQL Server? | Sí                          | No             |
| Implementación                               | Complex                      | Simple         |



 

En el ejemplo de controlador de recetas, el formato de archivo receta no tiene ningún requisito complejo, por lo que solo se ha implementado [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para la compatibilidad de texto completo. La búsqueda de texto completo se implementa para los nodos XML nombrados en la matriz siguiente.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



El sistema de propiedades contiene la `System.Search.Contents` propiedad (contenido de búsqueda de PKEY \_ \_ ), que se creó para proporcionar contenido de texto completo al indexador. El valor de esta propiedad nunca se muestra directamente en la interfaz de usuario; el texto de todos los nodos XML nombrados en la matriz anterior se concatena en una sola cadena. A continuación, esa cadena se proporciona al indexador como el contenido de texto completo del archivo receta a través de una llamada a [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) como se muestra en el ejemplo de código siguiente.


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



## <a name="providing-values-for-properties"></a>Proporcionar valores para las propiedades

Cuando se usa para leer valores, normalmente se invocan los controladores de propiedades por una de las razones siguientes:

-   Para enumerar todos los valores de propiedad.
-   Para obtener el valor de una propiedad específica.

Para la enumeración, se pide a un controlador de propiedades que Enumere sus propiedades durante la indización o cuando el cuadro de diálogo Propiedades pida que se muestren las propiedades en el **otro** grupo. La indexación se activa constantemente como una operación en segundo plano. Cada vez que un archivo cambia, se notifica al indexador y vuelve a indizar el archivo pidiendo al controlador de propiedades que Enumere sus propiedades. Por lo tanto, es fundamental que los controladores de propiedades se implementen de manera eficaz y devuelvan los valores de propiedad lo más rápido posible. Enumere todas las propiedades para las que tiene valores, del mismo modo que lo haría para cualquier colección, pero no enumere las propiedades que impliquen cálculos de uso intensivo de memoria o solicitudes de red que podrían ralentizar la recuperación.

Al escribir un controlador de propiedades, normalmente es necesario tener en cuenta los dos conjuntos de propiedades siguientes.

-   Propiedades principales: propiedades que el tipo de archivo admite de forma nativa. Por ejemplo, un controlador de propiedades de fotografía para metadatos de archivo de imagen intercambiable (EXIF) es compatible de forma nativa con `System.Photo.FNumber` .
-   Propiedades extendidas: propiedades que admite el tipo de archivo como parte de los metadatos abiertos.

Dado que el ejemplo usa la memoria caché en memoria, la implementación de métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) es simplemente una cuestión de delegar en esa caché, tal y como se muestra en el ejemplo de código siguiente.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Si decide no delegar en la memoria caché en memoria, debe implementar los métodos para proporcionar> el siguiente comportamiento esperado:

-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): Si no hay ninguna propiedad, este método devuelve **S \_ correcto**.
-   [**IPropertyStore:: getatt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): Si *iProp* es mayor o igual que *CProps*, este método devuelve e \_ INVALIDARG y la estructura a la que apunta el parámetro *PKEY* se rellena con ceros.
-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) y [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflejan el estado actual del controlador de propiedad. Si se agrega o se quita un [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) del archivo a través de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), estos dos métodos deben reflejar ese cambio la próxima vez que se llamen.
-   [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): si se solicita a este método un valor que no existe, devuelve **S \_ OK** con el valor que se indica como VT \_ vacío.

## <a name="writing-back-values"></a>Escribir valores hacia atrás

Cuando el controlador de propiedades escribe el valor de una propiedad mediante [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), no escribe el valor en el archivo hasta que se llama a [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) . La caché en memoria puede ser útil para implementar este esquema. En el código de ejemplo, la implementación **IPropertyStore:: SetValue** simplemente establece el nuevo valor en la memoria caché en memoria y establece el estado de esa propiedad en PSC \_ sucio.


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



En cualquier implementación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , se espera el siguiente comportamiento de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Si la propiedad ya existe, se establece el valor de la propiedad.
-   Si la propiedad no existe, se agrega la nueva propiedad y se establece su valor.
-   Si el valor de la propiedad no se puede conservar con la misma precisión que se indica (por ejemplo, truncamiento debido a las limitaciones de tamaño en el formato de archivo), el valor se establece en la medida de lo posible y se devuelve la InPlace \_ S \_ truncada.
-   Si el controlador de propiedad no admite la propiedad, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` se devuelve.
-   Si hay otro motivo por el que no se puede establecer el valor de la propiedad, como el archivo que se está bloqueando o la falta de derechos de edición a través de las listas de control de acceso (ACL), \_ \_ se devuelve STG E ACCESSDENIED.

Una ventaja importante del uso de secuencias, como el ejemplo, es la confiabilidad. Los controladores de propiedades siempre deben tener en cuenta que no pueden dejar un archivo en un estado incoherente en caso de que se produzca un error catastrófico. Obviamente, se deben evitar los daños en los archivos de un usuario y la mejor manera de hacerlo es con un mecanismo de "copia en escritura". Si el controlador de propiedad usa una secuencia para tener acceso a un archivo, este comportamiento se obtiene automáticamente. el sistema escribe cualquier cambio en la secuencia, reemplazando el archivo con la nueva copia solo durante la operación de confirmación.

Para invalidar este comportamiento y controlar el proceso de guardado de archivos manualmente, puede dejar de participar en el comportamiento de guardado seguro estableciendo el valor de ManualSafeSave en la entrada del registro del controlador, como se muestra aquí.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Cuando un controlador especifica el valor de ManualSafeSave, la secuencia con la que se inicializa no es una secuencia de transacción (STGM \_ ). El propio controlador debe implementar la función Safe Save para asegurarse de que el archivo no esté dañado si se interrumpe la operación de guardar. Si el controlador implementa la escritura en contexto, se escribirá en la secuencia que se proporciona. Si el controlador no admite esta característica, debe recuperar una secuencia con la que escribir la copia actualizada del archivo mediante [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Una vez que el controlador ha terminado de escribir, debe llamar a [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) en el flujo original para completar la operación y reemplazar el contenido de la secuencia original con la nueva copia del archivo.

ManualSafeSave es también la situación predeterminada si no inicializa el controlador con una secuencia. Sin un flujo original para recibir el contenido de la secuencia temporal, debe utilizar [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) para realizar una sustitución atómica del archivo de código fuente.

Los formatos de archivo de gran tamaño que se usarán de forma que generen archivos de más de 1 MB deben implementar la compatibilidad con la escritura de propiedades en contexto; de lo contrario, el comportamiento de rendimiento no cumple las expectativas de los clientes del sistema de propiedades. En este escenario, el tiempo necesario para escribir propiedades no debe verse afectado por el tamaño del archivo.

En el caso de archivos muy grandes, por ejemplo, un archivo de vídeo de 1 GB o más, se requiere una solución diferente. Si no hay espacio suficiente en el archivo para realizar la escritura en contexto, el controlador puede producir un error en la actualización de la propiedad si se ha agotado la cantidad de espacio reservado para la escritura de propiedades en contexto. Este error se produce para evitar un bajo rendimiento derivado de 2 GB de e/s (1 para leer, 1 para escribir). Debido a este posible error, estos formatos de archivo deben reservar suficiente espacio para la escritura de propiedades en contexto.

Si el archivo tiene espacio suficiente en el encabezado para escribir metadatos y la escritura de esos metadatos no hace que el archivo aumente o se reduzca, podría ser seguro escribir en contexto. Se recomienda 64 KB como punto de partida. Escribir en contexto es equivalente al controlador que solicita ManualSafeSave y llamar a [**IStream:: commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) en la implementación de [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), y tiene un rendimiento mucho mejor que la copia en escritura. Si cambia el tamaño del archivo debido a cambios en el valor de la propiedad, no se debe intentar escribir en contexto debido a la posibilidad de que un archivo esté dañado en caso de que se produzca una terminación anómala.

> [!Note]  
> Por motivos de rendimiento, se recomienda usar la opción ManualSafeSave con controladores de propiedades que trabajen con archivos de 100 KB o más.

 

Tal y como se muestra en la siguiente implementación de ejemplo de [**IPropertyStore:: commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), el controlador de ManualSafeSave se registra para ilustrar la opción de guardado Safe manual. El método **\_ SaveCacheToDom** escribe los valores de propiedad almacenados en la memoria caché en memoria en el objeto XMLdocument.


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



A continuación, pregunte si el especificada admite [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).


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



A continuación, confirme la secuencia original, que vuelve a escribir los datos en el archivo original de una manera segura.


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



A continuación, examine la implementación de **\_ SaveCacheToDom** .


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



Ahora recorra en iteración las propiedades para determinar si el valor de una propiedad ha cambiado desde que se cargó en la memoria.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



El método [**IPropertyStoreCache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) obtiene el estado de la propiedad en la memoria caché. La \_ marca de modificador de PSC, que se estableció en la implementación [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marca una propiedad como modificada.


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



Asigne la propiedad al nodo XML tal y como se especifica en la matriz de **\_ rgPropertyMap de ejemplo** .


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



Si una propiedad no está en el mapa, se trata de una nueva propiedad establecida por el explorador de Windows. Dado que se admiten los metadatos abiertos, guarde la nueva propiedad en la sección **ExtendedProperties** del XML.


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

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informa a la interfaz de usuario del shell de si se puede editar una propiedad determinada en la interfaz de usuario del shell. Es importante tener en cuenta que esto se refiere únicamente a la capacidad de editar la propiedad en la interfaz de usuario, no de si se puede llamar correctamente a [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) en la propiedad. Una propiedad que genera un valor devuelto de S \_ false desde [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) puede seguir siendo capaz de establecerse a través de una aplicación.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) devuelve **S \_ OK** para indicar que los usuarios finales deben tener permiso para editar la propiedad directamente. S \_ False indica que no deberían. S \_ false puede significar que las aplicaciones son responsables de escribir la propiedad, no de los usuarios. El shell deshabilita los controles de edición según corresponda en función de los resultados de las llamadas a este método. Se supone que un controlador que no implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) admite metadatos abiertos a través de la compatibilidad con la escritura de cualquier propiedad.

Si va a compilar un controlador que solo controla las propiedades de solo lectura, debe implementar el método **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) para que devuelva STG \_ E \_ ACCESSDENIED cuando se llame con la \_ marca ReadWrite STGM.

Algunas propiedades tienen el atributo [isInnate](./propdesc-schema-typeinfo.md) establecido en **true**. Las propiedades de INNATE tienen las siguientes características:

-   La propiedad se calcula normalmente de alguna manera. Por ejemplo, `System.Image.BitDepth` se calcula a partir de la propia imagen.
-   Cambiar la propiedad no tendría sentido sin cambiar el archivo. Por ejemplo, cambiar `System.Image.Dimensions` no cambia el tamaño de la imagen, por lo que no tiene sentido permitir que el usuario la cambie.
-   En algunos casos, el sistema proporciona automáticamente estas propiedades. Entre los ejemplos `System.DateModified` se incluyen, proporcionado por el sistema de archivos, y `System.SharedWith` , que se basa en la persona con la que el usuario comparte el archivo.

Debido a estas características, las propiedades marcadas como *IsInnate* se proporcionan al usuario en la interfaz de usuario de Shell solo como propiedades de solo lectura. Si una propiedad se marca como *IsInnate*, el sistema de propiedades no almacena esa propiedad en el controlador de propiedad. Por lo tanto, los controladores de propiedades no necesitan un código especial para tener en cuenta estas propiedades en sus implementaciones. Si el valor del atributo *IsInnate* no se especifica explícitamente para una propiedad determinada, el valor predeterminado es **false**.

## <a name="registering-and-distributing-property-handlers"></a>Registrar y distribuir controladores de propiedades

Con el controlador de propiedades implementado, debe estar registrado y su extensión de nombre de archivo asociada al controlador. Para obtener más información, vea [registrar y distribuir controladores de propiedades](./prophand-reg-dist.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los controladores de propiedades](./building-property-handlers-properties.md)
</dt> <dt>

[Usar nombres de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usar listas de propiedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registrar y distribuir controladores de propiedades](./prophand-reg-dist.md)
</dt> <dt>

[Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 

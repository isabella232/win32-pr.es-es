---
description: En este tema se presentan los requisitos para crear controladores de metadatos personalizados para el componente de creación de imágenes de Windows (WIC), incluidos los escritores y lectores de metadatos.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Información general sobre la extensibilidad de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277625"
---
# <a name="metadata-extensibility-overview"></a>Información general sobre la extensibilidad de metadatos

En este tema se presentan los requisitos para crear controladores de metadatos personalizados para el componente de creación de imágenes de Windows (WIC), incluidos los escritores y lectores de metadatos. También se describen los requisitos para extender la detección de componentes en tiempo de ejecución de WIC para incluir los controladores de metadatos personalizados.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Crear un lector de metadatos](#creating-a-metadata-reader)
    -   [Interfaz IWICMetadataReader](#iwicmetadatareader-interface)
    -   [Interfaz IWICPersistStream](#iwicpersiststream-interface)
    -   [Interfaz IWICStreamProvider](#iwicstreamprovider-interface)
-   [Creación de un escritor de metadatos](#creating-a-metadata-writer)
    -   [Interfaz IWICMetadataWriter](#iwicmetadatawriter-interface)
    -   [Interfaz IWICPersistStream](#iwicpersiststream-interface)
    -   [Interfaz IWICStreamProvider](#iwicstreamprovider-interface)
-   [Instalación y registro de un controlador de metadatos](#installing-and-registering-a-metadata-handler)
    -   [Claves del registro del controlador de metadatos](#metadata-handler-registry-keys)
    -   [Lectores de metadatos](#metadata-readers)
    -   [Escritores de metadatos](#metadata-writers)
    -   [Firmar un controlador de metadatos](#signing-a-metadata-handler)
-   [Consideraciones especiales](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Controladores 8BIM](#8bim-handlers)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe tener un conocimiento exhaustivo de WIC, sus componentes y metadatos para las imágenes. Para obtener más información sobre los metadatos de WIC, consulte [información general sobre metadatos de WIC](-wic-about-metadata.md). Para obtener más información sobre los componentes de WIC, consulte [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Introducción

Como se describe en [información general sobre los metadatos de WIC](-wic-about-metadata.md), a menudo hay varios bloques de metadatos en una imagen, cada uno de los cuales expone diferentes tipos de información en diferentes formatos de metadatos. Para interactuar con un formato de metadatos insertado en una imagen, una aplicación debe usar un controlador de metadatos adecuado. WIC proporciona varios controladores de metadatos (tanto lectores de metadatos como escritores) que le permiten leer y escribir tipos específicos de metadatos como Exif o XMP.

Además de los controladores nativos proporcionados, WIC proporciona API que permiten crear nuevos controladores de metadatos que participan en la detección de componentes en tiempo de ejecución de WIC. Esto permite que las aplicaciones que usan WIC lean y escriban los formatos de metadatos personalizados.

Los pasos siguientes permiten a los controladores de metadatos participar en la detección de metadatos en tiempo de ejecución de WIC.

-   Implemente una clase de controlador de lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) que exponga las interfaces WIC necesarias para leer el formato de metadatos personalizado. Esto permite a las aplicaciones basadas en WIC leer el formato de los metadatos de la misma manera que leen los formatos de metadatos nativos.
-   Implemente una clase de controlador de escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) que exponga las interfaces WIC necesarias para codificar el formato de metadatos personalizado. Esto permite a las aplicaciones basadas en WIC serializar el formato de los metadatos en formatos de imagen compatibles.
-   Firmar y registrar digitalmente los controladores de metadatos. Esto permite detectar los controladores de metadatos en tiempo de ejecución haciendo coincidir el patrón de identificación del registro con el patrón incrustado en el archivo de imagen.

## <a name="creating-a-metadata-reader"></a>Crear un lector de metadatos

El acceso principal a los bloques de metadatos dentro de un códec se realiza a través de la interfaz [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) que implementa cada códec WIC. Esta interfaz enumera cada uno de los bloques de metadatos incrustados en un formato de imagen para que se puedan detectar y crear instancias del controlador de metadatos adecuado para cada bloque. Los bloques de metadatos que no reconoce WIC se consideran desconocidos y se definen como GUID CLSID \_ WICUnknownMetadataReader. Para que WIC reconozca el formato de los metadatos, debe crear una clase que implemente tres interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)y [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Si el formato de los metadatos tiene restricciones que presentan inadecuadamente algunos métodos de las interfaces necesarias, estos métodos deben devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>Interfaz IWICMetadataReader

La interfaz [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) debe implementarse al crear un lector de metadatos. Esta interfaz proporciona acceso a los elementos de metadatos subordinado en el flujo de datos de un formato de metadatos.

En el código siguiente se muestra la definición de la interfaz del lector de metadatos tal y como se define en el archivo wincodecsdk. idl.

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

El método **GetMetadataFormat** devuelve el GUID del formato de metadatos.

El método **GetMetadataHandlerInfo** devuelve una interfaz [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) que proporciona información sobre el controlador de metadatos. Esto incluye información como qué formatos de imagen admiten el formato de metadatos y si el lector de metadatos requiere acceso a la secuencia de metadatos completa.

El método **getCount** devuelve el número de elementos de metadatos individuales (incluidos los bloques de metadatos incrustados) que se encuentran en la secuencia de metadatos.

El método **GetValueByIndex** devuelve un elemento de metadatos mediante un valor de índice. Este método permite a las aplicaciones recorrer cada elemento de metadatos en un bloque de metadatos. En el código siguiente se muestra cómo una aplicación puede utilizar este método para recuperar cada elemento de metadatos en un bloque de metadatos.


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



El método **GetValue** recupera un elemento de metadatos específico por esquema o identificador. Este método es similar al método **GetValueByIndex** , salvo que recupera un elemento de metadatos que tiene un esquema o un identificador específicos.

El método **GetEnumerator** devuelve un enumerador de cada elemento de metadatos en el bloque de metadatos. Esto permite a las aplicaciones usar un enumerador para navegar por el formato de los metadatos.

Si el formato de los metadatos no tiene un concepto de esquemas para los elementos de metadatos, el elemento GetValue... los métodos deben omitir esta propiedad. Sin embargo, si el formato admite nombres de esquema, debe prever un valor **null** .

Si un elemento de metadatos es un bloque de metadatos incrustado, cree un controlador de metadatos a partir del subflujo del contenido incrustado y devuelva el nuevo controlador de metadatos. Si no hay ningún lector de metadatos disponible para el bloque anidado, cree una instancia y devuelva un lector de metadatos desconocido. Para crear un nuevo lector de metadatos para el bloque incrustado, llame a los métodos **CreateMetadataReaderFromContainer** o **CreateMetadataReader** del generador de componentes, o llame a la función [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .

Si el flujo de metadatos contiene contenido big-endian, el lector de metadatos es responsable de intercambiar los valores de datos que procesa. También es responsable de informar a los lectores de metadatos anidados que están trabajando con el flujo de datos Big-Endian. Sin embargo, todos los valores se deben devolver en formato Little-Endian.

Implementar la compatibilidad con la navegación por espacios de nombres al admitir consultas en las que el identificador del elemento de metadatos es un `VT_CLSID` (GUID) que corresponde a un formato de metadatos. Si se identifica un lector de metadatos anidado para ese formato durante el análisis, se debe devolver. Esto permite a las aplicaciones usar un lector de consultas de metadatos para buscar en el formato de los metadatos.

Al obtener un elemento de metadatos por identificador, debe usar la [función PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) para convertir el identificador en el tipo esperado. Por ejemplo, el lector de IFD convertirá un identificador en un tipo `VT_UI2` para que coincida con el tipo de datos de un identificador de etiqueta de IFD USHORT. Para ello, el tipo de entrada y el tipo esperado deben ser [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Esto no es necesario, pero al realizar esta coerción se simplifica el código que llama al lector para consultar los elementos de metadatos.

### <a name="iwicpersiststream-interface"></a>Interfaz IWICPersistStream

La interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

En el código siguiente se muestra la definición de la interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

El método **LoadEx** proporciona el lector de metadatos con un flujo de datos que contiene el bloque de metadatos. El lector analiza este flujo para tener acceso a los elementos de metadatos subyacentes. El lector de metadatos se inicializa con un subflujo que se coloca al principio del contenido de metadatos sin formato. Si el lector no requiere el flujo completo, el subflujo está limitado en el intervalo solo al contenido del bloque de metadatos; de lo contrario, se proporciona la secuencia de metadatos completa con la posición establecida al principio del bloque de metadatos.

Los escritores de metadatos usan el método **SaveEx** para serializar el bloque de metadatos. Cuando se usa **SaveEx** en un lector de metadatos, debe devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>Interfaz IWICStreamProvider

La interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permite que el lector de metadatos proporcione referencias a su flujo de contenido, proporcione información sobre la secuencia y actualice las versiones en caché de la secuencia.

En el código siguiente se muestra la definición de la interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) tal como se define en el archivo wincodecsdk. idl.

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

El método **GetStream** recupera una referencia a la secuencia de metadatos. La secuencia que devuelva debe tener el puntero de secuencia restablecido a la posición inicial. Si el formato de los metadatos requiere acceso completo a secuencias, la posición inicial debe ser el inicio del bloque de metadatos.

El método **GetPersistOptions** devuelve las opciones actuales de la secuencia de la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

El método **GetPreferredVendorGUID** devuelve el GUID del proveedor del lector de metadatos.

El método **RefreshStream** actualiza la secuencia de metadatos. Este método debe llamar a **LoadEx** con una secuencia **null** para los bloques de metadatos anidados. Esto es necesario porque los bloques de metadatos anidados y sus elementos pueden dejar de existir, debido a la edición en contexto.

## <a name="creating-a-metadata-writer"></a>Creación de un escritor de metadatos

Un escritor de metadatos es un tipo de controlador de metadatos que proporciona una manera de serializar un bloque de metadatos en un marco de imagen o fuera de un fotograma individual si el formato de imagen lo admite. El acceso principal a los escritores de metadatos dentro de un códec es a través de la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que implementa cada codificador WIC. Esta interfaz permite a las aplicaciones enumerar cada uno de los bloques de metadatos insertados en una imagen para que se pueda detectar y crear una instancia del escritor de metadatos adecuado para cada bloque de metadatos. Los bloques de metadatos que no tienen un escritor de metadatos correspondiente se consideran desconocidos y se definen como GUID CLSID \_ WICUnknownMetadataReader. Para habilitar las aplicaciones habilitadas para WIC para serializar y escribir el formato de metadatos, debe crear una clase que implemente las interfaces siguientes: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)y [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Si el formato de los metadatos tiene restricciones que presentan inadecuadamente algunos métodos de las interfaces necesarias, estos métodos deben devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>Interfaz IWICMetadataWriter

El escritor de metadatos debe implementar la interfaz [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) . Además, dado que **IWICMetadataWriter** hereda de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), también debe implementar todos los métodos de **IWICMetadataReader**. Dado que ambos tipos de controlador requieren la misma herencia de interfaz, puede que desee crear una única clase que proporcione la funcionalidad de lectura y escritura.

En el código siguiente se muestra la definición de la interfaz del escritor de metadatos tal y como se define en el archivo wincodecsdk. idl.

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

El método **SetValue** escribe el elemento de metadatos especificado en la secuencia de metadatos.

El método **SetValueByIndex** escribe el elemento de metadatos especificado en el índice especificado en la secuencia de metadatos. El índice no hace referencia al identificador, sino a la posición del elemento en el bloque de metadatos.

El método **RemoveValue** quita el elemento de metadatos especificado de la secuencia de metadatos.

El método **RemoveValueByIndex** quita el elemento de metadatos en el índice especificado de la secuencia de metadatos. Después de quitar un elemento, se espera que los elementos de metadatos restantes ocupen el índice anulado si el índice no es el último índice. También se espera que el recuento cambie después de quitar el elemento.

Es responsabilidad del escritor de metadatos convertir los elementos [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en la estructura subyacente requerida por el formato. Sin embargo, a diferencia del lector de metadatos, los tipos de variante no se deben forzar normalmente a tipos diferentes, ya que el llamador está indicando específicamente qué tipo de datos se va a usar.

El escritor de metadatos debe confirmar todos los elementos de metadatos en el flujo de imagen, incluidos los valores ocultos o no reconocidos. Esto incluye bloques de metadatos anidados desconocidos. Sin embargo, es responsabilidad del codificador establecer los elementos de metadatos críticos antes de iniciar la operación de guardar.

Si la secuencia de metadatos contiene contenido big-endian, el escritor de metadatos es responsable de intercambiar los valores de datos que procesa. También es responsable de informar a los escritores de metadatos anidados que están trabajando con un flujo de datos Big-Endian cuando se guardan.

Implemente la compatibilidad con la creación y eliminación de espacios de nombres al admitir operaciones Set y Remove en elementos de metadatos con un tipo de `VT_CLSID` (un GUID) que se corresponda con un formato de metadatos. El escritor de metadatos llama a la función [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para insertar correctamente el contenido del escritor de metadatos anidados en el escritor de metadatos primario.

Si el formato de los metadatos admite la codificación en contexto, es responsable de administrar el relleno necesario. Para obtener más información sobre la codificación en contexto, consulte [información general sobre metadatos de WIC](-wic-about-metadata.md) e [información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).

### <a name="iwicpersiststream-interface"></a>Interfaz IWICPersistStream

La interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .

En el código siguiente se muestra la definición de la interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk. idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

El método **LoadEx** proporciona el controlador de metadatos con un flujo de datos que contiene el bloque de metadatos.

El método **SaveEx** serializa los metadatos en un flujo. Si el flujo proporcionado es el mismo que el de la secuencia de inicialización, debe realizar la codificación en contexto. Si se admite la codificación en contexto, este método debe devolver WINCODEC \_ Err \_ TOOMUCHMETADATA cuando no hay suficiente relleno para realizar la codificación en contexto. Si no se admite la codificación en contexto, este método debe devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

El método **IPersistStream:: GetSizeMax** debe implementarse y debe devolver el tamaño exacto del contenido de los metadatos que se escribiría en el almacenamiento posterior.

El método **IPersistStream:: IsDirty** debe implementarse si el escritor de metadatos se inicializa a través de una secuencia, para que una imagen pueda determinar de forma confiable si su contenido ha cambiado.

Si el formato de los metadatos admite bloques de metadatos anidados, el escritor de metadatos debe delegar en los escritores de metadatos anidados la serialización de su contenido al guardar en una secuencia.

### <a name="iwicstreamprovider-interface"></a>Interfaz IWICStreamProvider

La implementación de la interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) para un escritor de metadatos es la misma que la de un lector de metadatos. Para obtener más información, consulte la sección creación de un lector de metadatos en este documento.

## <a name="installing-and-registering-a-metadata-handler"></a>Instalación y registro de un controlador de metadatos

Para instalar un controlador de metadatos, debe proporcionar el ensamblado de controlador y registrarlo en el registro del sistema. Puede decidir cómo y cuándo se rellenan las claves del registro.

> [!Note]  
> Para facilitar la lectura, los GUID hexadecimales reales no se muestran en las claves del registro que se muestran en las siguientes secciones de este documento. Para buscar el valor hexadecimal de un nombre descriptivo especificado, vea los archivos wincodec. idl y wincodecsdk. idl.

 

### <a name="metadata-handler-registry-keys"></a>Claves del registro del controlador de metadatos

Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos. Cada identificador de categoría del tipo de controlador se define en wincodec. idl; el nombre de identificador de categoría para los lectores es CATId \_ WICMetadataReader y el nombre de identificador de categoría para escritores es CATID \_ WICMetadataWriter.

Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos. Cada identificador de categoría del tipo de controlador se define en wincodec. idl; el nombre de identificador de categoría para los lectores es CATId \_ WICMetadataReader y el nombre de identificador de categoría para escritores es CATID \_ WICMetadataWriter.

> [!Note]  
> En las siguientes listas de claves del registro, {Reader CLSID} hace referencia al CLSID único que se proporciona para el lector de metadatos. {Writer CLSID} hace referencia al CLSID único que se proporciona para el escritor de metadatos. {Handler CLSID} hace referencia al CLSID del lector, el CLSID del escritor o ambos, en función de los controladores que se proporcionen. {Container GUID} hace referencia al objeto contenedor (formato de imagen o formato de metadatos) que puede contener el bloque de metadatos.

 

Las siguientes claves del registro registran el controlador de metadatos con los demás controladores de metadatos disponibles:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Además de registrar los controladores en sus categorías respectivas, también debe registrar claves adicionales que proporcionen información específica del controlador. Los lectores y escritores comparten requisitos de clave del registro similares. En la sintaxis siguiente se muestra cómo registrar un controlador. Tanto el controlador de lector como el controlador del sistema de escritura deben registrarse de esta manera mediante sus respectivos CLSID:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>Lectores de metadatos

El registro del lector de metadatos también incluye claves que describen cómo se puede incrustar el lector en un formato de contenedor. Un formato de contenedor puede ser un formato de imagen como TIFF o JPEG; también puede ser otro formato de metadatos, como un bloque de metadatos de IFD. Los formatos de contenedor de imágenes compatibles de forma nativa se muestran en wincodec. idl; cada formato de contenedor de imágenes se define como un GUID con un nombre que comienza con el GUID \_ ContainerFormat. Los formatos de contenedor de metadatos admitidos de forma nativa se enumeran en wincodecsdk. idl; cada formato de contenedor de metadatos se define como un GUID con un nombre que comienza con el GUID \_ MetadataFormat.

Las claves siguientes registran un contenedor que admite el lector de metadatos y los datos necesarios para leer de ese contenedor. Cada contenedor que admite el lector debe estar registrado de esta manera.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

La clave de patrón describe el modelo binario que se usa para hacer coincidir el bloque de metadatos con el lector. Al definir un patrón para el lector de metadatos, debe ser lo suficientemente confiable como para que una coincidencia positiva signifique que el lector de metadatos puede comprender los metadatos en el bloque de metadatos que se está procesando.

La clave de desfase de datos describe el desplazamiento fijo de los metadatos a partir del encabezado de bloque. Esta clave es opcional y, si no se especifica, significa que los metadatos reales no pueden encontrarse con un desplazamiento fijo del encabezado de bloque.

### <a name="metadata-writers"></a>Escritores de metadatos

El registro del escritor de metadatos también incluye claves que describen cómo escribir el encabezado que precede al contenido de los metadatos incrustado en un formato de contenedor. Al igual que con el lector, un formato de contenedor puede ser un formato de imagen u otro bloque de metadatos.

Las claves siguientes registran un contenedor que admite el escritor de metadatos y los datos necesarios para escribir el encabezado y los metadatos. Cada contenedor que admite el sistema de escritura debe estar registrado de esta manera.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

La clave WriteHeader describe el patrón binario del encabezado de bloque de metadatos que se va a escribir. Este patrón binario coincide con la clave del patrón de lector del formato de metadatos.

La clave WriteOffset describe el desplazamiento fijo del encabezado de bloque en el que deben escribirse los metadatos. Esta clave es opcional y, si no se especifica, significa que los metadatos reales no deben escribirse con el encabezado.

### <a name="signing-a-metadata-handler"></a>Firmar un controlador de metadatos

Todos los controladores de metadatos deben estar firmados digitalmente para participar en el proceso de detección de WIC. WIC no cargará ningún controlador que no esté firmado por una entidad de certificación de confianza. Para obtener más información sobre la firma digital, vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="special-considerations"></a>Consideraciones especiales

En las secciones siguientes se incluye información adicional que debe tener en cuenta al crear sus propios controladores de metadatos.

### <a name="propvariants"></a>PROPVARIANTS

WIC usa un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para representar un elemento de metadatos para lectura y escritura. Un PROPVARIANT proporciona un tipo de datos y un valor de datos para un elemento de metadatos que se usa en un formato de metadatos. Como escritor de un controlador de metadatos, tiene mucha flexibilidad en cuanto a cómo se almacenan los datos en el formato de metadatos y cómo se representan los datos dentro de un bloque de metadatos. En la tabla siguiente se proporcionan instrucciones que le ayudarán a decidir el tipo de PROPVARIANT adecuado para usarlo en diferentes situaciones.



| El tipo de metadatos es...          | Uso del tipo PROPVARIANT      | Propiedad PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vacío o no existe.       | VT \_ vacío                 | No es aplicable.                                                                                                                                                                                                                                                                |
| Sin definir.                   | BLOB de VT \_                  | Use la propiedad BLOB para establecer el tamaño y el puntero en el objeto de BLOB asignado mediante CoTaskMemAlloc.                                                                                                                                                                           |
| Un bloque de metadatos.            | VT \_ desconocido               | Este tipo usa la propiedad punkVal.                                                                                                                                                                                                                                           |
| Matriz de tipos.           | VT \_ Vector \| VT \_ {Type}  | Use la propiedad CA {Type} para establecer el recuento y el puntero a la matriz asignada mediante CoTaskMemAlloc.                                                                                                                                                                            |
| Matriz de bloques de metadatos. | VT \_ Vector \| VT ( \_ variante) | Use la propiedad capropvar para establecer la matriz de variantes.                                                                                                                                                                                                                       |
| Valor racional con signo.     | VT \_ i8                    | Use la propiedad hVal para establecer el valor. Establezca la palabra alta en el denominador y la palabra inferior en el numerador.                                                                                                                                                                |
| Un valor racional.            | VT \_ UI8                   | Use la propiedad uhVal para establecer el valor. Establezca HighPart en el denominador y el LowPart en el numerador. Tenga en cuenta que LowPart es un int sin signo. El numerador se debe convertir de un int sin signo a un entero para asegurarse de que el bit de signo se conserva si está presente. |



 

Para evitar la redundancia en la representación de elementos de matriz, no utilice matrices seguras; Use solo matrices simples. Esto reduce el trabajo que una aplicación necesita realizar al interpretar los tipos de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Evite usar `VT_BYREF` y almacenar valores en línea siempre que sea posible. `VT_BYREF` no es eficaz para los tipos pequeños (comunes para los elementos de metadatos) y no proporciona información de tamaño.

Antes de usar [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), llame siempre a **PropVariantInit** para inicializar el valor. Cuando haya terminado con el PROPVARIANT, llame siempre a **PropVariantClear** para liberar cualquier memoria asignada a la variable.

### <a name="8bim-handlers"></a>Controladores 8BIM

Al escribir un controlador de metadatos para un bloque de metadatos de 8BIM, debe usar una firma que encapsule la firma 8BIM y el identificador. Por ejemplo, el lector de metadatos 8BIMIPTC nativo proporciona la siguiente información del registro para la detección del lector:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

El lector 8BIMIPTC tiene un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. Los primeros cuatro bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM y los dos últimos bytes (0x04, 0x04) son el identificador del registro IPTC.

Por lo tanto, para escribir un lector de metadatos de 8BIM para la información de resolución, necesitaría un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. De nuevo, los cuatro primeros bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM. Sin embargo, los dos últimos bytes (0x03, 0xED) son el identificador de la información de resolución tal y como se define en el formato PSD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general del lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Cómo volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 

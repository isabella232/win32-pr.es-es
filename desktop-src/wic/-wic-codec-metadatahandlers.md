---
description: En este tema se presentan los requisitos para crear controladores de metadatos personalizados para Windows Imaging Component (WIC), incluidos los lectores de metadatos y los escritores.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Información general sobre extensibilidad de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d38206fb02c47edbe9744deb6ceb0093277d8354f8717aa89c3f1976bdeb51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088177"
---
# <a name="metadata-extensibility-overview"></a>Información general sobre extensibilidad de metadatos

En este tema se presentan los requisitos para crear controladores de metadatos personalizados para Windows Imaging Component (WIC), incluidos los lectores de metadatos y los escritores. También se analizan los requisitos para extender la detección de componentes en tiempo de ejecución de WIC para incluir los controladores de metadatos personalizados.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Crear un lector de metadatos](#creating-a-metadata-reader)
    -   [IWICMetadataReader (interfaz)](#iwicmetadatareader-interface)
    -   [IWICPersistStream (interfaz)](#iwicpersiststream-interface)
    -   [IWICStreamProvider (interfaz)](#iwicstreamprovider-interface)
-   [Crear un escritor de metadatos](#creating-a-metadata-writer)
    -   [IWICMetadataWriter (Interfaz)](#iwicmetadatawriter-interface)
    -   [IWICPersistStream (interfaz)](#iwicpersiststream-interface)
    -   [IWICStreamProvider (interfaz)](#iwicstreamprovider-interface)
-   [Instalar y registrar un controlador de metadatos](#installing-and-registering-a-metadata-handler)
    -   [Claves del Registro del controlador de metadatos](#metadata-handler-registry-keys)
    -   [Lectores de metadatos](#metadata-readers)
    -   [Escritores de metadatos](#metadata-writers)
    -   [Firmar un controlador de metadatos](#signing-a-metadata-handler)
-   [Consideraciones especiales](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [Controladores de 8BIM](#8bim-handlers)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe tener una comprensión detallada de WIC, sus componentes y metadatos para imágenes. Para obtener más información sobre los metadatos de WIC, vea [Información general sobre los metadatos de WIC.](-wic-about-metadata.md) Para obtener más información sobre los componentes de WIC, vea Windows Imaging Component Overview (Información general sobre componentes de creación [de imágenes).](-wic-about-windows-imaging-codec.md)

## <a name="introduction"></a>Introducción

Como se describe en Información general de metadatos de [WIC,](-wic-about-metadata.md)a menudo hay varios bloques de metadatos dentro de una imagen, cada uno de los que expone diferentes tipos de información en diferentes formatos de metadatos. Para interactuar con un formato de metadatos insertado dentro de una imagen, una aplicación debe usar un controlador de metadatos adecuado. WIC proporciona varios controladores de metadatos (lectores y escritores de metadatos) que permiten leer y escribir tipos específicos de metadatos, como Exif o XMP.

Además de los controladores nativos proporcionados, WIC proporciona API que permiten crear nuevos controladores de metadatos que participan en la detección de componentes en tiempo de ejecución de WIC. Esto permite a las aplicaciones que usan WIC leer y escribir los formatos de metadatos personalizados.

Los pasos siguientes permiten a los controladores de metadatos participar en la detección de metadatos en tiempo de ejecución de WIC.

-   Implemente una clase de controlador de lector de metadatos [**(IWICMetadataReader)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)que exponga las interfaces WIC necesarias para leer el formato de metadatos personalizado. Esto permite a las aplicaciones basadas en WIC leer el formato de metadatos de la misma manera que leen los formatos de metadatos nativos.
-   Implemente una clase de controlador metadata-writer [**(IWICMetadataWriter)**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)que exponga las interfaces WIC necesarias para codificar el formato de metadatos personalizado. Esto permite a las aplicaciones basadas en WIC serializar el formato de metadatos en formatos de imagen admitidos.
-   Firmar digitalmente y registrar los controladores de metadatos. Esto permite detectar los controladores de metadatos en tiempo de ejecución mediante la coincidencia del patrón de identificación en el Registro con el patrón incrustado en el archivo de imagen.

## <a name="creating-a-metadata-reader"></a>Crear un lector de metadatos

El acceso principal a los bloques de metadatos dentro de un códec es a través de la [**interfaz IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) que implementa cada códec WIC. Esta interfaz enumera cada uno de los bloques de metadatos insertados en un formato de imagen para que se pueda detectar y crear una instancia del controlador de metadatos adecuado para cada bloque. Los bloques de metadatos que WIC no reconoce se consideran desconocidos y se definen como EL GUID CLSID \_ WICUnknownMetadataReader. Para que WIC reconozca el formato de metadatos, debe crear una clase que implemente tres interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)

> [!Note]  
> Si el formato de metadatos tiene restricciones que representan que algunos métodos de las interfaces necesarias son inadecuados, estos métodos deben devolver \_ WINCODEC ERR \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatareader-interface"></a>IWICMetadataReader (interfaz)

La [**interfaz IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) debe implementarse al crear un lector de metadatos. Esta interfaz proporciona acceso a los elementos de metadatos de subling dentro del flujo de datos de un formato de metadatos.

El código siguiente muestra la definición de la interfaz del lector de metadatos tal como se define en el archivo wincodecsdk.idl.

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

El **método GetMetadataFormat** devuelve el GUID del formato de metadatos.

El **método GetMetadataHandlerInfo** devuelve una [**interfaz IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) que proporciona información sobre el controlador de metadatos. Esto incluye información como qué formatos de imagen admiten el formato de metadatos y si el lector de metadatos requiere acceso al flujo de metadatos completo.

El **método GetCount** devuelve el número de elementos de metadatos individuales (incluidos los bloques de metadatos incrustados) que se encuentran en el flujo de metadatos.

El **método GetValueByIndex** devuelve un elemento de metadatos por un valor de índice. Este método permite a las aplicaciones recorrer en bucle cada elemento de metadatos de un bloque de metadatos. El código siguiente muestra cómo una aplicación puede usar este método para recuperar cada elemento de metadatos de un bloque de metadatos.


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



El **método GetValue** recupera un elemento de metadatos específico por esquema o identificador. Este método es similar al **método GetValueByIndex,** salvo que recupera un elemento de metadatos que tiene un esquema o identificador específicos.

El **método GetEnumerator** devuelve un enumerador de cada elemento de metadatos del bloque de metadatos. Esto permite a las aplicaciones usar un enumerador para navegar por el formato de metadatos.

Si el formato de metadatos no tiene una noción de esquemas para los elementos de metadatos, getValue... Los métodos deben omitir esta propiedad. Sin embargo, si el formato admite la nomenclatura de esquema, debe prever un **valor** NULL.

Si un elemento de metadatos es un bloque de metadatos incrustado, cree un controlador de metadatos a partir de la subtransmisión del contenido insertado y devuelva el nuevo controlador de metadatos. Si no hay ningún lector de metadatos disponible para el bloque anidado, cree una instancia y devuelva un lector de metadatos desconocido. Para crear un nuevo lector de metadatos para el bloque incrustado, llame a los métodos **CreateMetadataReaderFromContainer** o **CreateMetadataReader** del generador de componentes o llame a la función [**WICMatchMetadataContent.**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)

Si el flujo de metadatos contiene contenido big-endian, el lector de metadatos es responsable de intercambiar los valores de datos que procesa. También es responsable de informar a los lectores de metadatos anidados de que están trabajando con el flujo de datos big-endian. Sin embargo, todos los valores deben devolverse en formato little-endian.

Implemente la compatibilidad con la navegación del espacio de nombres mediante consultas en las que el identificador del elemento de metadatos sea `VT_CLSID` (un GUID) correspondiente a un formato de metadatos. Si se identifica un lector de metadatos anidado para ese formato durante el análisis, se debe devolver. Esto permite a las aplicaciones usar un lector de consultas de metadatos para buscar en el formato de metadatos.

Al obtener un elemento de metadatos por identificador, debe usar [propVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) para convertir el identificador en el tipo esperado. Por ejemplo, el lector IFD coercerá un identificador para que escriba para que coincida con el tipo de datos de un identificador de etiqueta `VT_UI2` IFD USHORT. Para ello, el tipo de entrada y el tipo esperado [deben ser PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Esto no es necesario, pero esta coerción simplifica el código que llama al lector para consultar elementos de metadatos.

### <a name="iwicpersiststream-interface"></a>IWICPersistStream (interfaz)

La [**interfaz IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la [**enumeración WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

El código siguiente muestra la definición de la [**interfaz IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk.idl.

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

El **método LoadEx** proporciona al lector de metadatos un flujo de datos que contiene el bloque de metadatos. El lector analiza esta secuencia para acceder a los elementos de metadatos subyacentes. El lector de metadatos se inicializa con una sub secuencia que se coloca al principio del contenido de metadatos sin formato. Si el lector no requiere la secuencia completa, la subtransmisión se limita en intervalo solo al contenido del bloque de metadatos. De lo contrario, el flujo de metadatos completo se proporciona con la posición establecida al principio del bloque de metadatos.

Los **escritores de** metadatos usan el método SaveEx para serializar el bloque de metadatos. Cuando **se usa SaveEx** en un lector de metadatos, debe devolver WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider (interfaz)

La [**interfaz IWICStreamProvider permite**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) que el lector de metadatos proporcione referencias a su flujo de contenido, proporcione información sobre la secuencia y actualice las versiones almacenadas en caché de la secuencia.

El código siguiente muestra la definición de la [**interfaz IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) tal como se define en el archivo wincodecsdk.idl.

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

El **método GetStream** recupera una referencia a la secuencia de metadatos. La secuencia que devuelve debe tener el puntero de secuencia restablecido a la posición inicial. Si el formato de metadatos requiere acceso completo a la secuencia, la posición inicial debe ser el inicio del bloque de metadatos.

El **método GetPersistOptions** devuelve las opciones actuales de la secuencia de la [**enumeración WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

El **método GetPreferredVendorGUID** devuelve el GUID del proveedor del lector de metadatos.

El **método RefreshStream** actualiza el flujo de metadatos. Este método debe llamar a **LoadEx con** un **flujo NULL** para los bloques de metadatos anidados. Esto es necesario porque es posible que los bloques de metadatos anidados y sus elementos ya no existan, debido a la edición en contexto.

## <a name="creating-a-metadata-writer"></a>Crear un escritor de metadatos

Un escritor de metadatos es un tipo de controlador de metadatos que proporciona una manera de serializar un bloque de metadatos en un marco de imagen o fuera de un marco individual si el formato de imagen lo admite. El acceso principal a los escritores de metadatos dentro de un códec es a través de la [**interfaz IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que implementa cada codificador WIC. Esta interfaz permite a las aplicaciones enumerar cada uno de los bloques de metadatos insertados en una imagen para que se puedan detectar y crear instancias del escritor de metadatos adecuado para cada bloque de metadatos. Los bloques de metadatos que no tienen un escritor de metadatos correspondiente se consideran desconocidos y se definen como EL GUID CLSID \_ WICUnknownMetadataReader. Para permitir que las aplicaciones habilitadas para WIC serialice y escriban el formato de metadatos, debe crear una clase que implemente las interfaces siguientes: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) [**IWICPersistStream e**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Si el formato de metadatos tiene restricciones que representan que algunos métodos de las interfaces necesarias son inadecuados, estos métodos deben devolver \_ WINCODEC ERR \_ UNSUPPORTEDOPERATION.

 

### <a name="iwicmetadatawriter-interface"></a>IWICMetadataWriter (Interfaz)

El escritor de metadatos debe implementar la interfaz [**IWICMetadataWriter.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) Además, dado que **IWICMetadataWriter** hereda de [**IWICMetadataReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)también debe implementar todos los métodos de **IWICMetadataReader**. Dado que ambos tipos de controlador requieren la misma herencia de interfaz, es posible que desee crear una sola clase que proporciona funcionalidad de lectura y escritura.

El código siguiente muestra la definición de la interfaz del escritor de metadatos tal como se define en el archivo wincodecsdk.idl.

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

El **método SetValue** escribe el elemento de metadatos especificado en el flujo de metadatos.

El **método SetValueByIndex** escribe el elemento de metadatos especificado en el índice especificado en el flujo de metadatos. El índice no hace referencia al identificador, sino a la posición del elemento dentro del bloque de metadatos.

El **método RemoveValue** quita el elemento de metadatos especificado del flujo de metadatos.

El **método RemoveValueByIndex** quita del flujo de metadatos el elemento de metadatos en el índice especificado. Después de quitar un elemento, se espera que los elementos de metadatos restantes ocupen el índice desocupado si el índice no es el último. También se espera que el recuento cambie después de quitar el elemento.

Es responsabilidad del escritor de metadatos convertir los elementos [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) a la estructura subyacente que requiere el formato. Sin embargo, a diferencia del lector de metadatos, los tipos VARIANT normalmente no se deben convertir en tipos diferentes, ya que el autor de la llamada indica específicamente qué tipo de datos usar.

El escritor de metadatos debe confirmar todos los elementos de metadatos en el flujo de imágenes, incluidos los valores ocultos o no reconocidos. Esto incluye bloques de metadatos anidados desconocidos. Sin embargo, es responsabilidad del codificador establecer los elementos de metadatos críticos antes de iniciar la operación de guardado.

Si el flujo de metadatos contiene contenido big-endian, el escritor de metadatos es responsable de intercambiar los valores de datos que procesa. También es responsable de informar a los escritores de metadatos anidados de que están trabajando con un flujo de datos big-endian cuando se guarda.

Implemente la compatibilidad con la creación y eliminación de espacios de nombres al admitir operaciones de conjunto y eliminación en elementos de metadatos con un tipo `VT_CLSID` de (un GUID) correspondiente a un formato de metadatos. El escritor de metadatos llama a la función [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para insertar correctamente el contenido del escritor de metadatos anidado en el escritor de metadatos primario.

Si el formato de metadatos admite la codificación local, usted es responsable de administrar el relleno necesario. Para obtener más información sobre la codificación local, vea Información general sobre metadatos [de WIC](-wic-about-metadata.md) e Información general sobre la lectura y escritura de [metadatos de imagen.](-wic-codec-readingwritingmetadata.md)

### <a name="iwicpersiststream-interface"></a>IWICPersistStream (interfaz)

La [**interfaz IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la [**enumeración WICPersistOptions.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)

El código siguiente muestra la definición de la [**interfaz IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk.idl.

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

El **método LoadEx** proporciona al controlador de metadatos un flujo de datos que contiene el bloque de metadatos.

El **método SaveEx** serializa los metadatos en una secuencia. Si la secuencia proporcionada es la misma que la secuencia de inicialización, debe realizar la codificación local. Si se admite la codificación in-place, este método debe devolver WINCODEC \_ ERR TOOMUCHMETADATA cuando no hay suficiente relleno para realizar la codificación \_ en su lugar. Si no se admite la codificación local, este método debe devolver WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

El **método IPersistStream::GetSizeMax** debe implementarse y debe devolver el tamaño exacto del contenido de metadatos que se escribiría en el guardado posterior.

El **método IPersistStream::IsDirty** debe implementarse si el escritor de metadatos se inicializa a través de una secuencia, de modo que una imagen pueda determinar de forma confiable si su contenido ha cambiado.

Si el formato de metadatos admite bloques de metadatos anidados, el escritor de metadatos debe delegar a los escritores de metadatos anidados la serialización de su contenido al guardar en una secuencia.

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider (interfaz)

La implementación de la [**interfaz IWICStreamProvider para**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) un escritor de metadatos es la misma que la de un lector de metadatos. Para obtener más información, vea la sección Creación de un lector de metadatos en este documento.

## <a name="installing-and-registering-a-metadata-handler"></a>Instalar y registrar un controlador de metadatos

Para instalar un controlador de metadatos, debe proporcionar el ensamblado del controlador y registrarlo en el registro del sistema. Puede decidir cómo y cuándo se rellenan las claves del Registro.

> [!Note]  
> Para mejorar la legibilidad, los GUID hexadecimales reales no se muestran en las claves del Registro que se muestran en las secciones siguientes de este documento. Para buscar el valor hexadecimal de un nombre descriptivo especificado, consulte los archivos wincodec.idl y wincodecsdk.idl.

 

### <a name="metadata-handler-registry-keys"></a>Claves del Registro del controlador de metadatos

Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos. El identificador de categoría de cada tipo de controlador se define en wincodec.idl; el nombre del identificador de categoría para los lectores es CATID WICMetadataReader y el nombre del identificador de categoría para los escritores \_ es CATID \_ WICMetadataWriter.

Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos. El identificador de categoría de cada tipo de controlador se define en wincodec.idl; el nombre del identificador de categoría para los lectores es CATID WICMetadataReader y el nombre del identificador de categoría para los escritores \_ es CATID \_ WICMetadataWriter.

> [!Note]  
> En las siguientes listas de claves del Registro, {Reader CLSID} hace referencia al CLSID único que se proporciona para el lector de metadatos. {WRITER CLSID} hace referencia al CLSID único que se proporciona para el escritor de metadatos. {CLSID del controlador} hace referencia al CLSID del lector, al CLSID del escritor o a ambos, en función de los controladores que proporcione. {GUID de contenedor} hace referencia al objeto contenedor (formato de imagen o formato de metadatos) que puede contener el bloque de metadatos.

 

Las siguientes claves del Registro registran el controlador de metadatos con los otros controladores de metadatos disponibles:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Además de registrar los controladores en sus respectivas categorías, también debe registrar claves adicionales que proporcionen información específica para el controlador. Los lectores y escritores comparten requisitos de clave del Registro similares. La sintaxis siguiente muestra cómo registrar un controlador. Tanto el controlador de lector como el controlador de escritor deben registrarse de esta manera, con sus CLID respectivos:

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

El registro del lector de metadatos también incluye claves que describen cómo se puede incrustar el lector en un formato de contenedor. Un formato de contenedor puede ser un formato de imagen como TIFF o JPEG; también puede ser otro formato de metadatos, como un bloque de metadatos IFD. Los formatos de contenedor de imágenes admitidos de forma nativa se muestran en wincodec.idl; cada formato de contenedor de imágenes se define como un GUID con un nombre que comienza por \_ GUID ContainerFormat. Los formatos de contenedor de metadatos admitidos de forma nativa se enumeran en wincodecsdk.idl; cada formato de contenedor de metadatos se define como un GUID con un nombre que comienza por GUID \_ MetadataFormat.

Las claves siguientes registran un contenedor compatible con el lector de metadatos y los datos necesarios para leer de ese contenedor. Cada contenedor admitido por el lector debe registrarse de esta manera.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

La clave pattern describe el patrón binario que se usa para hacer coincidir el bloque de metadatos con el lector. Al definir un patrón para el lector de metadatos, debe ser lo suficientemente confiable como para que una coincidencia positiva signifique que el lector de metadatos puede comprender los metadatos del bloque de metadatos que se está procesando.

La clave DataOffset describe el desplazamiento fijo de los metadatos del encabezado de bloque. Esta clave es opcional y, si no se especifica, significa que los metadatos reales no se pueden encontrar utilizando un desplazamiento fijo del encabezado de bloque.

### <a name="metadata-writers"></a>Escritores de metadatos

El registro del escritor de metadatos también incluye claves que describen cómo escribir el encabezado anterior al contenido de metadatos insertado en un formato de contenedor. Al igual que con el lector, un formato de contenedor puede ser un formato de imagen u otro bloque de metadatos.

Las claves siguientes registran un contenedor compatible con el escritor de metadatos y los datos necesarios para escribir el encabezado y los metadatos. Cada contenedor admitido por el escritor debe registrarse de esta manera.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

La clave WriteHeader describe el patrón binario del encabezado de bloque de metadatos que se va a escribir. Este patrón binario coincide con la clave de patrón del lector del formato de metadatos.

La clave WriteOffset describe el desplazamiento fijo del encabezado de bloque en el que se deben escribir los metadatos. Esta clave es opcional y, si no se especifica, significa que los metadatos reales no se deben escribir con el encabezado .

### <a name="signing-a-metadata-handler"></a>Firmar un controlador de metadatos

Todos los controladores de metadatos deben estar firmados digitalmente para participar en el proceso de detección de WIC. WIC no cargará ningún controlador que no esté firmado por una entidad de certificación de confianza. Para obtener más información sobre la firma digital, vea [Introducción a la firma de código.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))

## <a name="special-considerations"></a>Consideraciones especiales

En las secciones siguientes se incluye información adicional que debe tener en cuenta al crear sus propios controladores de metadatos.

### <a name="propvariants"></a>PROPVARIANTS

WIC usa [PROPVARIANT para representar](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) un elemento de metadatos para lectura y escritura. PROPVARIANT proporciona un tipo de datos y un valor de datos para un elemento de metadatos usado en un formato de metadatos. Como escritor de un controlador de metadatos, tiene mucha flexibilidad sobre cómo se almacenan los datos en el formato de metadatos y cómo se representan los datos dentro de un bloque de metadatos. En la tabla siguiente se proporcionan instrucciones que le ayudarán a decidir el tipo PROPVARIANT adecuado que se usará en situaciones diferentes.



| El tipo de metadatos es...          | Uso del tipo PROPVARIANT      | Propiedad PROPVARIANT                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vacío o inexistente.       | VT \_ EMPTY                 | No es aplicable.                                                                                                                                                                                                                                                                |
| Sin definir.                   | BLOB \_ DE VT                  | Use la propiedad blob para establecer el tamaño y el puntero al objeto BLOB asignado mediante CoTaskMemAlloc.                                                                                                                                                                           |
| Un bloque de metadatos.            | VT \_ UNKNOWN               | Este tipo usa la propiedad asínval.                                                                                                                                                                                                                                           |
| Matriz de tipos.           | VT \_ VECTOR \| VT \_ {type}  | Use la propiedad ca{type} para establecer el recuento y el puntero a la matriz asignada mediante CoTaskMemAlloc.                                                                                                                                                                            |
| Matriz de bloques de metadatos. | VT \_ VECTOR \| VT \_ VARIANT | Use la propiedad capropvar para establecer la matriz de variantes.                                                                                                                                                                                                                       |
| Valor racionalizado con firma.     | VT \_ I8                    | Use la propiedad hVal para establecer el valor. Establezca la palabra alta en el denominador y la palabra baja en el numerador.                                                                                                                                                                |
| Valor racionalizado.            | VT \_ UI8                   | Use la propiedad uhVal para establecer el valor. Establezca HighPart en el denominador y LowPart en el numerador. Tenga en cuenta que LowPart es un valor int sin signo. El numerador debe convertirse de int sin signo a int para asegurarse de que el bit de signo se conserva si está presente. |



 

Para evitar redundancia al representar elementos de matriz, no use matrices seguras; usar solo matrices simples. Esto reduce el trabajo que debe realizar una aplicación al interpretar tipos [PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Evite usar `VT_BYREF` y almacenar valores en línea siempre que sea posible. `VT_BYREF` es ineficaz para tipos pequeños (comunes para los elementos de metadatos) y no proporciona información de tamaño.

Antes de usar [PROPVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)llame siempre a **PropVariantInit** para inicializar el valor. Cuando haya terminado con PROPVARIANT, llame siempre a **PropVariantClear** para liberar cualquier memoria asignada para la variable.

### <a name="8bim-handlers"></a>8Bim Handlers (Controladores de 8BIM)

Al escribir un controlador de metadatos para un bloque de metadatos de 8BIM, debe usar una firma que encapsula tanto la firma 8BIM como el identificador. Por ejemplo, el lector de metadatos nativo 8BIMIPTC proporciona la siguiente información del Registro para la detección de lectores:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

El lector 8BIMIPTC tiene un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. Los cuatro primeros bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM y los dos últimos bytes (0x04, 0x04) son el identificador del registro IPTC.

Por lo tanto, para escribir un lector de metadatos de 8BIM para obtener información de resolución, necesitará un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. De nuevo, los cuatro primeros bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM. Los dos últimos bytes (0x03, 0xED), sin embargo, son el identificador de información de resolución definido por el formato PSD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Cómo: Volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 

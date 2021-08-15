---
title: Conjuntos de fuentes personalizadas
description: En este tema se describen varias maneras de usar fuentes personalizadas en la aplicación.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b8b9c49895c2b137aaa33cf0788d9518a1d53834c74eb27feb6b44fa045d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650289"
---
# <a name="custom-font-sets"></a>Conjuntos de fuentes personalizadas

En este tema se describen varias maneras de usar fuentes personalizadas en la aplicación.

-   [Introducción ](#introduction)
-   [Resumen de API](#summary-of-apis)
-   [Conceptos clave](#key-concepts)
-   [Fuentes y formatos de archivo de fuente](#fonts-and-font-file-formats)
-   [Conjuntos de fuentes y colecciones de fuentes](#font-sets-and-font-collections)
-   [Escenarios comunes](#common-scenarios)
    -   [Creación de un conjunto de fuentes mediante fuentes arbitrarias en el sistema de archivos local](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Creación de un conjunto de fuentes mediante fuentes conocidas en el sistema de archivos local](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Creación de un conjunto de fuentes personalizado mediante fuentes remotas conocidas en la Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Creación de un conjunto de fuentes personalizado con datos de fuente cargados en memoria](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Escenarios avanzados](#advanced-scenarios)
    -   [Combinación de conjuntos de fuentes](#combining-font-sets)
    -   [Uso de datos de fuente WOFF o WOFF2 locales ](#using-local-woff-or-woff2-font-data)
    -   [Uso DirectWrite de fuentes remotas con una implementación de red personalizada de bajo nivel](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Escenarios de compatibilidad en versiones Windows anteriores](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introducción

La mayoría de las veces, las aplicaciones usan las fuentes que se instalan localmente en el sistema. DirectWrite proporciona acceso a estas fuentes mediante los métodos [**IDWriteFactory3::GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) [**o IDWriteFactory::GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) En algunos casos, es posible que las aplicaciones también quieran usar fuentes que se incluyen como parte de Windows 10 pero que no están instaladas actualmente en el sistema actual. Se puede acceder a estas fuentes desde el servicio de fuentes Windows mediante el método **GetSystemFontSet** o llamando a [**IDWriteFactory3::GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) con includeDownloadableFonts establecido en TRUE. 

Sin embargo, en algunos escenarios de aplicación, las aplicaciones deben usar fuentes que no están instaladas en el sistema y que no se proporcionan mediante el servicio de fuentes Windows de aplicaciones. A continuación se muestran ejemplos de estos escenarios:

-   Las fuentes se incrustan como recursos dentro de un binario de aplicación.
-   Los archivos de fuente se agrupan en un paquete de aplicación y se almacenan en el disco en la carpeta de instalación de la aplicación.
-   La aplicación es una herramienta de desarrollo de fuentes que necesita cargar archivos de fuente especificados por el usuario. 
-   Las fuentes se incrustan en archivos de documento que se pueden ver o editar en la aplicación. 
-   La aplicación usa fuentes obtenidas de un servicio de fuentes web público. 
-   La aplicación usa datos de fuente transmitidos a través de un protocolo de red privada. 

DirectWrite proporciona API para trabajar con fuentes personalizadas en estos y otros escenarios similares. Los datos de fuente personalizados pueden provienen de archivos del sistema de archivos local. desde orígenes remotos basados en la nube a los que se accede mediante HTTP; o de orígenes arbitrarios después de haber cargado en un búfer de memoria. 

> [!Note]  
> Aunque DirectWrite ha proporcionado API para trabajar con fuentes personalizadas desde Windows 7, las API más recientes se agregaron en Windows 10 y de nuevo en Windows 10 Creators Update (versión preliminar 15021 o posterior) que facilitan la implementación de varios de los escenarios mencionados. Este tema se centra en las API disponibles en Windows 10. Para las aplicaciones que necesitan trabajar en versiones anteriores Windows, vea Colecciones de fuentes [personalizadas (Windows 7/8).](custom-font-collections.md) 

 

## <a name="summary-of-apis"></a>Resumen de API

Este tema se centra en la funcionalidad proporcionada por las siguientes API: 

-   [**Interfaz IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**Interfaz IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**Interfaz IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   [**Interfaz IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   [**Interfaz IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   [**Método IDWriteFactory::CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   [**Método IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   [**Métodos IDWriteFactory3::CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**DWRITE \_ FONT \_ PROPERTY (estructura)**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ Font \_ PROPERTY \_ ID (enumeración)**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   [**Interfaz IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   [**Método IDWriteFactory::RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 
-   [**Método IDWriteFactory::UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 
-   [**Método IDWriteFactory5::CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 
-   [**Interfaz IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   [**Método IDWriteFactory5::CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 
-   [**Interfaz IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   [**Interfaz IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   [**Interfaz IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   [**Interfaz IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   [**Interfaz IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   [**Interfaz IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   [**Método IDWriteFactory5::AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 
-   [**IdWriteFactory5::UnpackFontFile (método)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 

 

## <a name="key-concepts"></a>Conceptos clave

Para comprender el DirectWrite API para trabajar con fuentes personalizadas, puede ser útil comprender el modelo conceptual que subyace a estas API. Aquí se describen los conceptos clave. 

Cuando DirectWrite diseño o representación de texto real, debe tener acceso a los datos de fuente reales. Un objeto de cara de fuente contiene datos de fuente reales, que deben existir en el sistema local. Pero para otras operaciones, como comprobar la disponibilidad de una fuente determinada o presentar opciones de fuente a un usuario, todo lo que se necesita es una referencia a una fuente determinada, no a los propios datos de fuente reales. En DirectWrite, un objeto de referencia de la cara de fuente contiene solo la información necesaria para buscar y crear instancias de una fuente. Dado que la referencia de la cara de fuente no contiene datos reales, DirectWrite puede tratar con referencias de caras de fuente para las que los datos reales están en una ubicación de red remota, así como cuando los datos reales son locales.

Un conjunto de fuentes es un conjunto de referencias de caras de fuente, junto con ciertas propiedades básicas e informativos que se pueden usar para hacer referencia a la fuente o para compararla con otras fuentes, como el nombre de familia o un valor de peso de fuente. Los datos reales de las distintas fuentes pueden ser locales, o pueden ser remotos o una mezcla.

Se puede usar un conjunto de fuentes para obtener un objeto de colección de fuentes correspondiente. Consulte Conjuntos de fuentes y colecciones de fuentes a continuación para obtener más detalles. 

La interfaz IDWriteFontSet proporciona métodos que permiten consultar valores de propiedad, como el nombre de familia o el peso de la fuente, o para referencias de caras de fuente que coincidan con valores de propiedad determinados. Después de filtrar a una selección determinada, se puede obtener una instancia de la interfaz [**IDWriteFontFaceReference,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) con métodos para descargar (si los datos de fuente reales son actualmente remotos), para obtener el objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) correspondiente que se puede usar para el diseño y la representación. 

La interfaz IDWriteFontFile subyace a cada referencia de cara de fuente o de fuente. Representa la ubicación de un archivo de fuente y tiene dos componentes: un cargador de archivos de fuentes y una clave de archivo de fuente. El cargador de archivos de fuente ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) se usa para abrir un archivo si es necesario y devuelve una secuencia con los datos ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Dependiendo del cargador, los datos pueden encontrarse en una ruta de acceso de archivo local, una dirección URL remota o en un búfer de memoria. La clave es un valor definido por el cargador que identifica de forma única el archivo dentro del contexto del cargador, lo que permite al cargador localizar los datos y crear una secuencia para él. 

Las fuentes personalizadas se pueden agregar fácilmente a un conjunto de fuentes personalizado, que a su vez se puede usar para filtrar u organizar la información de fuente con fines como la creación de una interfaz de usuario del selector de fuentes. El conjunto de fuentes también se puede usar para crear una colección de fuentes para su uso en API de nivel superior, como [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) La [**interfaz IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) se puede usar para crear un conjunto de fuentes personalizado que incluya varias fuentes personalizadas. También se puede usar para crear un conjunto de fuentes personalizado que combine fuentes personalizadas y fuentes proporcionadas por el sistema; o que combina fuentes con orígenes diferentes para los datos reales: almacenamiento local, direcciones URL remotas y memoria. 

Como se mencionó, una referencia de la cara de fuente puede hacer referencia a los datos de fuente en un origen remoto, pero los datos deben ser locales para obtener un objeto de cara de fuente que se pueda usar para el diseño y la representación. La descarga de datos remotos se controla mediante una cola de descarga de fuentes. Las aplicaciones pueden usar la interfaz [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) para poner en cola las solicitudes para descargar fuentes remotas para iniciar el proceso de descarga y para registrar un objeto [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) para tomar medidas cuando se haya completado el proceso de descarga. 

Para la mayoría de las interfaces descritas aquí, DirectWrite implementaciones del sistema. La única excepción es la interfaz [**IDWriteFontDownloadListener,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) que una aplicación implementa para realizar acciones específicas de la aplicación cuando las fuentes remotas se han descargado localmente. Las aplicaciones pueden tener motivos para proporcionar sus propias implementaciones personalizadas para determinadas otras interfaces, aunque esto solo sería necesario en escenarios específicos y más avanzados. Por ejemplo, una aplicación tendría que proporcionar una implementación personalizada de la interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) para controlar los archivos de fuente en el almacenamiento local que usan el formato de contenedor WOFF2. A continuación se proporcionan detalles adicionales. 

## <a name="fonts-and-font-file-formats"></a>Fuentes y formatos de archivo de fuente

Otro concepto clave que resulta útil comprender es la relación entre las caras de fuente individuales y los archivos de fuente que los contienen. La idea de un archivo de fuente OpenType (.ttf o .otf) que contiene una sola fuente es familiar. Pero el formato de fuente OpenType también permite una colección de fuentes OpenType (.ttc o .otc), que es un único archivo que contiene varias fuentes. Los archivos de colección OpenType se suelen usar para fuentes de gran tamaño que están estrechamente relacionadas y tienen valores idénticos para determinados datos de fuente: al combinar las fuentes en un solo archivo, los datos comunes se pueden desduplicar. Por esta razón, una referencia de fuente o de fuente debe hacer referencia no solo a un archivo de fuente (o origen de datos equivalente), sino que también debe especificar un índice de fuente dentro de ese archivo, para el caso general en el que el archivo puede ser un archivo de colección. 

En el caso de las fuentes usadas en la Web, los datos de fuente a menudo se empaquetan en determinados formatos de contenedor, WOFF o WOFF2, que proporcionan cierta compresión de los datos de fuente y algún nivel de protección frente a la infracción de licencias de fuente. Funcionalmente, un archivo WOFF o WOFF2 es equivalente a una fuente OpenType o un archivo de colección de fuentes, pero los datos se codifican en un formato diferente que requiere desempaquetar antes de poder usarse. 

Algunas DIRECTWRITE API pueden tratar con caras de fuente individuales, mientras que otras API pueden controlar archivos que pueden incluir archivos de colección OpenType que contienen varias caras. Del mismo modo, algunas API solo tratan con datos sin formato OpenType, mientras que otras API pueden controlar los formatos de contenedor empaquetados, WOFF y WOFF2. Estos detalles se proporcionan en la explicación siguiente. 

## <a name="font-sets-and-font-collections"></a>Conjuntos de fuentes y colecciones de fuentes

Algunas aplicaciones se pueden implementar para trabajar con fuentes mediante la [**interfaz IDWriteFontCollection.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) Hay una correspondencia directa entre una colección de fuentes y un conjunto de fuentes. Cada una puede contener las mismas fuentes, pero las presentan con una organización diferente. Desde cualquier colección de fuentes, se puede obtener un conjunto de fuentes correspondiente y viceversa.

Cuando se trabaja con una serie de fuentes personalizadas, es más fácil usar una interfaz de generador de conjunto de fuentes para crear un conjunto de fuentes personalizado y, a continuación, obtener una colección de fuentes después de crear el conjunto de fuentes. El proceso para crear un conjunto de fuentes personalizado se describirá con detalle a continuación. Para obtener una [**interfaz IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) de un conjunto de fuentes, se usa el método [**IDWriteFactory3::CreateFontCollectionFromFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset)

Si la aplicación tiene un objeto de colección y necesita obtener un conjunto de fuentes correspondiente, puede hacerlo mediante el [**método IDWriteFontCollection1::GetFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) 

## <a name="common-scenarios"></a>Escenarios frecuentes

En esta sección se describen algunos de los escenarios más comunes que implican conjuntos de fuentes personalizados:

-   Crear un conjunto de fuentes personalizado mediante fuentes arbitrarias en las rutas de acceso del sistema de archivos local.
-   Crear un conjunto de fuentes personalizado mediante fuentes conocidas (quizás agrupadas con la aplicación) que se almacenan en el sistema de archivos local.
-   Crear un conjunto de fuentes personalizado mediante fuentes conocidas y remotas en la Web.
-   Crear un conjunto de fuentes personalizado con datos de fuente cargados en la memoria.

Las implementaciones completas para estos escenarios se proporcionan en el ejemplo DirectWrite de conjuntos de fuentes [personalizados](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). En este ejemplo también se muestra un escenario más avanzado para controlar los datos de fuente empaquetados en formatos de contenedor WOFF o WOFF2, que se tratarán a continuación. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Creación de un conjunto de fuentes mediante fuentes arbitrarias en el sistema de archivos local

Cuando se trabaja con un conjunto arbitrario de archivos de fuente en el almacenamiento local, el método [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) es conveniente, ya que, en una sola llamada, puede controlar todas las caras de fuente dentro de un archivo de colección de fuentes OpenType, así como todas las instancias de una fuente de variable OpenType. Está disponible en la versión Windows 10 Creators Update (versión preliminar 15021 o posterior) y se recomienda siempre que esté disponible. 

Para usar este método, use el siguiente proceso.

<dl> 1.Empiece por crear la <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">interfaz IDWriteFactory5:</a> 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Use el generador para obtener la <a href=""></a> [**interfaz IDWriteFontSetBuilder1:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Para cada archivo de fuente del sistema de archivos local, cree un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) que haga referencia a él: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Agregue el [**objeto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generador de conjunto de fuentes mediante el [**método AddFontFile:**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Si la ruta de acceso del archivo especificada en la llamada a [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) hace referencia a algo distinto de un archivo OpenType compatible, la llamada a [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) devolverá un error, DWRITE \_ E \_ FILEFORMAT.

5. Una vez que se han agregado todos los archivos al generador de conjunto de fuentes, se puede crear el conjunto de fuentes personalizado: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Si la aplicación debe ejecutarse en Windows 10 versiones anteriores a Windows 10 Creators Update, el método AddFontFile no estará disponible. La disponibilidad se puede detectar mediante la creación de una interfaz [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) y, a continuación, mediante QueryInterface para intentar obtener una interfaz [**IDWriteFactory5:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) si esto se realiza correctamente, también estarán disponibles la interfaz [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) y el método [**AddFontFile.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile)

Si el método AddFontFile no está disponible, se debe usar el método [**IDWriteFontSetBuilder::AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) para agregar caras de fuente individuales. Para permitir archivos de colección de fuentes OpenType que contienen varias caras, se puede usar el método [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para determinar el número de caras contenidas en el archivo. El proceso es el siguiente.

<dl> 1.Empiece por crear la <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">interfaz IDWriteFactory3:</a> 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Use el generador para obtener la [**interfaz IDWriteFontSetBuilder:**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Para cada archivo de fuente, cree [**un IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), como se ha indicado anteriormente: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



En lugar de agregar el archivo directamente al generador de conjunto de fuentes, es necesario determinar el número de caras y crear objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuales.   
4. Use el [**método Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para obtener el número de caras del archivo. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



El [**método Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) también establecerá valores para los parámetros isSupported y fileType. Si el archivo no es un formato compatible, isSupported será FALSE y se puede realizar la acción adecuada, como omitir el archivo.   
5. Recorrer en bucle el número de fuentes establecidas en el parámetro numberOfFonts. Dentro del bucle , cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) para cada par de archivo/índice y agrégalo al generador de conjunto de fuentes. 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. Una vez que se hayan agregado todas las caras al generador de conjunto de fuentes, cree el conjunto de fuentes personalizado, como se mostró anteriormente.  
</dl>

Una aplicación se puede diseñar para que use el método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) preferido al ejecutarse en el Windows 10 Creators Update, pero se reserva para usar el método [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) cuando se ejecuta en versiones anteriores de Windows 10. Pruebe la disponibilidad de la [**interfaz IDWriteFactory5,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) como se describió anteriormente, y, a continuación, la rama en consecuencia. Este enfoque se ilustra en el ejemplo DirectWrite de conjuntos de fuentes [personalizados](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Creación de un conjunto de fuentes mediante fuentes conocidas en el sistema de archivos local

Como se mencionó anteriormente, cada referencia de la cara de fuente de un conjunto de fuentes está asociada a determinadas propiedades informativos, como el nombre de familia y el peso de la fuente. Cuando se agregan fuentes personalizadas a un generador de conjunto de fuentes mediante las llamadas API enumeradas anteriormente, estas propiedades informativos se obtienen directamente de los datos de fuente reales, que se leen a medida que se agrega la fuente. Sin embargo, en algunas situaciones, si una aplicación tiene otra fuente de información sobre una fuente, es posible que desee proporcionar sus propios valores personalizados para estas propiedades. 

Como ejemplo de cómo esto podría ser útil, supongamos que una aplicación agrupa algunas fuentes que se usan para presentar elementos de interfaz de usuario determinados dentro de la aplicación. En ocasiones, como con una nueva versión de la aplicación, es posible que sea necesario cambiar las fuentes específicas que la aplicación usa para estos elementos. Si la aplicación tiene referencias codificadas a las fuentes específicas, el reemplazo de una fuente por otra requerirá cambiar cada una de esas referencias. En su lugar, si la aplicación usa propiedades personalizadas para asignar alias funcionales en función del tipo de elemento o texto que se representa, asigna cada alias a una fuente específica en un lugar y, a continuación, usa los alias en todos los contextos en los que se crean y manipulan fuentes, reemplazar una fuente por otra solo requiere cambiar el único lugar en el que el alias se asigna a una fuente específica. 

Se pueden asignar valores personalizados para propiedades de información cuando se llama al método [**IDWriteFontSetBuilder::AddFontFaceReference.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) El método para hacerlo es el siguiente; se puede usar en cualquier Windows 10 versión. 

Como se mostró anteriormente, empiece por obtener las interfaces [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e [**IDWriteFontSet.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) Para cada cara de fuente personalizada que se va a agregar, cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), como se muestra anteriormente. Sin embargo, antes de agregarlo al generador de conjunto de fuentes (dentro del bucle del paso 5, mostrado anteriormente), la aplicación define los valores de propiedad personalizados que se van a usar. 

Un conjunto de valores de propiedad personalizados se define mediante una matriz de estructuras [**\_ DWRITE FONT \_ PROPERTY.**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) Cada una de ellas identifica una propiedad determinada de la enumeración [**\_ DWRITE FONT \_ PROPERTY \_ ID**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) y el valor de propiedad correspondiente que se va a usar.  

Tenga en cuenta que todos los valores de propiedad se asignan como cadenas. Si posteriormente se pueden mostrar a los usuarios, se pueden establecer valores alternativos para una propiedad determinada para distintos idiomas, pero esto no es necesario. Tenga en cuenta también que si la aplicación establece valores de propiedad personalizados, solo se usarán los valores especificados dentro del conjunto de fuentes. DirectWrite no derivará ningún valor directamente de la fuente para las propiedades de información usadas en un conjunto de fuentes. 

En el ejemplo siguiente se definen valores personalizados para tres propiedades informativos: nombre de familia, nombre completo y peso de fuente. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Después de definir la matriz deseada de valores de propiedad para una fuente, realice una llamada a AddFontFaceRefence, pasando la matriz de propiedades, así como la referencia de la cara de fuente. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Una vez que se han agregado todas las caras de fuente personalizadas al generador de conjunto de fuentes, junto con sus propiedades personalizadas, cree el conjunto de fuentes personalizado, como se muestra anteriormente. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Creación de un conjunto de fuentes personalizado mediante fuentes conocidas y remotas en la Web

Las propiedades personalizadas son importantes para trabajar con fuentes remotas. Cada referencia de la cara de fuente debe tener algunas propiedades de información para caracterizar la fuente y distinguirla de otras fuentes. Puesto que los datos de fuente de las fuentes remotas no son locales, DirectWrite pueden derivar propiedades directamente de los datos de fuente. Por lo tanto, las propiedades deben proporcionarse explícitamente al agregar una fuente remota al generador de conjunto de fuentes.

La secuencia de llamadas API para agregar fuentes remotas a un conjunto de fuentes es similar a la secuencia descrita en el escenario anterior. Sin embargo, dado que los datos de fuente son remotos, las operaciones implicadas para leer los datos de fuente reales serán diferentes de cuando se trabaja con archivos en el almacenamiento local. En esta situación, se ha agregado una nueva interfaz de nivel inferior, [**IDWriteRemoteFontFileLoader,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader)en el Windows 10 Creators Update. 

Para usar el cargador de archivos de fuente remoto, primero debe registrarse con un generador DirectWrite fuente. La aplicación tendrá que retenido el cargador siempre y cuando se estén utilizando las fuentes asociadas a él. Una vez que las fuentes ya no estén en uso y en algún momento antes de que se destruya la fábrica, el cargador debe anular el registro. Esto se puede hacer en el destructor de la clase propietaria del objeto de cargador. Estos pasos se mostrarán a continuación. 

El método para crear un conjunto de fuentes personalizado mediante fuentes remotas es el siguiente; esto requiere el Windows 10 Creators Update.  

<dl> 1. Cree una interfaz IDWriteFactory5, como se mostró anteriormente.   
2. Cree una <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">interfaz IDWriteFontSetBuilder,</a> como se mostró anteriormente.   
3. Use el generador para obtener un <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>. 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



Esto devuelve una implementación proporcionada por el sistema de la interfaz del cargador de archivos de fuentes remota que es capaz de controlar las interacciones HTTP para descargar datos de fuente en nombre de la aplicación. Si es necesario, el servicio de fuentes o los servicios que son el origen de las fuentes pueden especificar una dirección URL de referencia o encabezados adicionales.    

> [!IMPORTANT]
> Nota de seguridad: Cuando se intenta capturar una fuente remota, existe la posibilidad de que un atacante suplante el servidor previsto al que se llamará. En ese caso, las direcciones URL de destino y de referencia y los detalles del encabezado se revelarán al atacante. Los desarrolladores de aplicaciones son responsables de mitigar este riesgo. Se recomienda el uso del protocolo HTTPS, en lugar de HTTP. 

 

Se puede usar un único cargador de archivos de fuente remoto para varias fuentes, aunque se pueden usar cargadores diferentes si las fuentes se obtienen de varios servicios que tienen requisitos diferentes para la dirección URL del referenciador o encabezados adicionales.   
4. Registre el cargador de archivos de fuente remoto con el generador. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Desde este punto, los pasos para crear el conjunto de fuentes personalizado son similares a los descritos para los archivos de fuentes locales conocidos, con dos excepciones importantes. En primer lugar, [**el objeto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) se crea mediante la interfaz del cargador de archivos de fuentes remotas en lugar de usar el generador. En segundo lugar, no se puede usar el método Analyze, ya que los datos de fuente no son locales. En su lugar, la aplicación debe saber si el archivo de fuente remoto es un archivo de colección de fuentes OpenType y, si es así, debe saber cuál de las fuentes de la colección usará y el índice de cada una. Por lo tanto, los pasos restantes son los siguientes.   
5. Para cada archivo de fuente remoto, use la interfaz del cargador de archivos de fuentes remotas para crear un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)y especifique la dirección URL necesaria para acceder al archivo de fuente. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Tenga en cuenta que la dirección URL completa se puede especificar en el parámetro fontFileUrl o se puede dividir en partes base y relativas. Si se especifica una dirección URL base, la concatenación de los valores baseUrl y fontFileUrl debe proporcionar la dirección URL completa DirectWrite no proporcionará ningún delimitador adicional.  

> [!IMPORTANT]
> Nota de seguridad y rendimiento: Cuando se intenta capturar una fuente remota, no hay ninguna garantía de que Windows recibirá una respuesta del servidor. En algunos casos, un servidor puede responder con un error de archivo no encontrado para una dirección URL relativa no válida, pero dejar de responder si recibe varias solicitudes no válidas. Si el servidor no responde, Windows tiempo de espera, aunque esto puede tardar varios minutos si se inician varias recuperaciones. Debe hacer lo posible para asegurarse de que las direcciones URL serán válidas cuando se realicen llamadas. 

 

Tenga en cuenta también que la dirección URL puede apuntar a un archivo de fuente OpenType sin formato (.ttf, .otf, .ttc, .otc), pero también puede apuntar a fuentes de un archivo contenedor WOFF o WOFF2. Si se hace referencia a un archivo WOFF o WOFF2, la implementación de DirectWrite del cargador de archivos de fuente remoto desempaquetará automáticamente los datos de fuente del archivo contenedor.   
6. Para cada índice de la cara de fuente dentro del archivo de fuente remoto que se va a usar, cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference). 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Defina propiedades personalizadas para la cara de fuente, como se muestra anteriormente.   
8. Agregue la referencia de la cara de fuente junto con las propiedades personalizadas al generador de conjunto de fuentes, como se ha mostrado anteriormente.   
9. Una vez que se hayan agregado todas las fuentes al generador del conjunto de fuentes, cree el conjunto de fuentes, como se muestra anteriormente.   
10. En algún momento en el que ya no se usarán las fuentes remotas, anula el registro del cargador de archivos de fuentes remotas. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Una vez creado un conjunto de fuentes personalizado con fuentes remotas personalizadas, el conjunto de fuentes contiene referencias y propiedades de información para las fuentes remotas, pero los datos reales siguen siendo remotos. DirectWrite compatibilidad con fuentes remotas permite mantener una referencia de la cara de fuente en el conjunto de fuentes y seleccionar una fuente para su uso en el diseño y la representación, pero que los datos reales no se descarguen hasta que haya una necesidad real de usarla, como cuando se realizará el diseño de texto.  

Una aplicación puede realizar un enfoque por adelantado solicitando que DirectWrite los datos de fuente y, a continuación, esperando la confirmación de una descarga correcta antes de que se haya iniciado cualquier procesamiento con la fuente. Pero una descarga de red implica cierta latencia de duración imprevisible y el éxito también es incierto. Por esta razón, normalmente será mejor tomar un enfoque diferente, lo que permite que el diseño y la representación se realizan inicialmente mediante fuentes alternativas o de reserva que ya son locales, al tiempo que se solicita la descarga de la fuente remota deseada en paralelo y, a continuación, se actualizan los resultados una vez que se ha descargado la fuente deseada. 

Para solicitar que se descargue toda la fuente antes de que se use, se puede usar el método [**IDWriteFontFaceReference::EnqueueFontDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) Si la fuente es muy grande, solo se puede necesitar una parte de los datos para procesar cadenas concretas. DirectWrite proporciona métodos adicionales que se pueden usar para solicitar partes de los datos de fuente necesarios para contenido determinado, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) y [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest).  

Supongamos que el enfoque que se va a adoptar en la aplicación es permitir que el procesamiento se haga inicialmente mediante fuentes locales, alternativas o de reserva. El método IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) se puede usar para identificar fuentes de reserva locales y también pondrá en cola automáticamente una solicitud para descargar la fuente preferida. Además, si se usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y se aplica formato a parte o a todo el texto del diseño mediante una referencia de fuente remota, DirectWrite usará automáticamente el método **MapCharacters** para obtener fuentes de reserva locales y poner en cola una solicitud para descargar los datos de fuente remotos. 

DirectWrite mantiene una cola de descarga de fuentes para cada generador y las solicitudes realizadas con los métodos mencionados anteriormente se agregan a esa cola. La cola de descarga de fuentes se puede obtener mediante el [**método IDWriteFactory3::GetFontDownloadQueue.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) 

Si se realiza una solicitud de descarga pero los datos de fuente ya son locales, esto dará lugar a una operación no op: No se agregará nada a la cola de descarga. Una aplicación puede comprobar si la cola está vacía o si hay solicitudes de descarga pendientes llamando al [**método IDWriteFontDownloadQueue::IsEmpty.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 

Una vez agregadas las solicitudes de fuente remotas a la cola, se debe iniciar el proceso de descarga. Cuando se usan fuentes remotas en [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)la descarga se iniciará automáticamente cuando la aplicación llame a **métodos IDWriteTextLayout** que fuerzan las operaciones de diseño o representación, como los métodos GetLineMetrics o Draw. En otros escenarios, la aplicación debe iniciar la descarga directamente mediante una llamada a [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Cuando se complete una descarga, será la aplicación la que tome las medidas adecuadas: continuar con las operaciones pendientes o repetir las operaciones que se realizaron inicialmente con fuentes de reserva. (Si DirectWrite diseño de texto de DirectWrite, se puede usar [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) para borrar los resultados temporales calculados mediante fuentes de reserva). Para que la aplicación se notifique cuando se haya completado el proceso de descarga y se tomen las medidas adecuadas, la aplicación debe proporcionar una implementación de la interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) y pasarla a la llamada BeginDownload. 

> [!IMPORTANT]
> Nota de seguridad y rendimiento: Cuando se intenta capturar una fuente remota, no hay ninguna garantía de que Windows recibirá una respuesta del servidor. Si el servidor no responde, Windows tiempo de espera, aunque esto puede tardar varios minutos si se capturan varias fuentes remotas pero se da error. La llamada BeginDownload se devolverá inmediatamente. Las aplicaciones no deben bloquear la interfaz de usuario mientras esperan a que se llame a [**IDWriteFontDownloadListener::D ownloadCompleted.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) 

 

Las implementaciones de ejemplo de estas interacciones con la cola de descarga de fuentes de DirectWrite y la interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) se pueden ver en el ejemplo de conjuntos de fuentes personalizados de [DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)y también en el ejemplo de fuentes descargables de [DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Creación de un conjunto de fuentes personalizado con datos de fuente cargados en memoria

Del mismo modo que las operaciones de bajo nivel para leer datos de un archivo de fuente son diferentes para los archivos de un disco local frente a los archivos remotos en la Web, también ocurre lo mismo con los datos de fuente cargados en un búfer de memoria. Se ha agregado una nueva interfaz de bajo nivel para controlar los datos de fuente en memoria en el Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader.**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 

Al igual que con un cargador de archivos de fuente remoto, primero se debe registrar un cargador de archivos de fuente en memoria con un generador DirectWrite fuente. La aplicación deberá tener el cargador mientras se estén utilizando las fuentes asociadas a él. Una vez que las fuentes ya no estén en uso y en algún momento antes de que se destruya la fábrica, el cargador debe anular el registro. Esto se puede hacer en el destructor de la clase que posee el objeto de cargador. Estos pasos se mostrarán a continuación. 

Si la aplicación tiene información independiente sobre las caras de fuente representadas por los datos, puede agregar referencias de caras de fuente individuales a un generador de conjunto de fuentes con propiedades personalizadas especificadas. Sin embargo, dado que los datos de fuente están en la memoria local, esto no es necesario; DirectWrite podrá leer los datos directamente para derivar los valores de propiedad. 

DirectWrite da por supuesto que los datos de fuente están en formato OpenType sin formato, equivalente a un archivo OpenType (.ttf, .otf, .ttc, .otc), pero en memoria en lugar de en disco. Los datos no pueden estar en un formato de contenedor WOFF o WOFF2. Los datos pueden representar una colección de fuentes OpenType. Si no se usan propiedades personalizadas, se puede usar el método [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) para agregar todas las caras de fuente en los datos en una sola llamada. 

Una consideración importante para el escenario en memoria es la duración de los datos. Si se proporciona un puntero al búfer para DirectWrite sin una indicación clara de que hay un propietario, DirectWrite realizará una copia de los datos en un nuevo búfer de memoria de su propiedad. Para evitar la copia de datos y la asignación de memoria adicional, la aplicación puede pasar un objeto de propietario de datos que implementa IUnknown y que posee el búfer de memoria que contiene los datos de fuente. Al implementar esta interfaz, DirectWrite agregar al recuento de referencias del objeto, lo que garantiza la duración de los datos en propiedad. 

El método para crear un conjunto de fuentes personalizado con datos de fuente en memoria es el siguiente: esto requiere el Windows 10 Creators Update. Esto supondrá un objeto de propietario de datos implementado por la aplicación, que implementa IUnknown y también tiene métodos que devuelven un puntero al búfer de memoria y el tamaño del búfer. 

<dl> 1. Cree una interfaz IDWriteFactory5, como se muestra anteriormente.  
2. Cree una [**interfaz IDWriteFontSetBuilder1,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) como se muestra anteriormente.  
3. Use el generador para obtener un IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Esto devuelve una implementación proporcionada por el sistema de la interfaz del cargador de archivos de fuentes en memoria.   
4. Registre el cargador de archivos de fuente en memoria con el generador. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Para cada archivo de fuente en memoria, use el cargador de archivos de fuente en memoria para crear un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile). 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. Agregue el [**objeto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generador de conjunto de fuentes mediante el [**método AddFontFile,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) como se muestra anteriormente.  Si es necesario, la aplicación puede crear en su lugar objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuales basados en **IDWriteFontFile,** definir opcionalmente propiedades personalizadas para cada referencia de la cara de fuente y, a continuación, agregar la referencia de la cara de fuente con propiedades personalizadas al conjunto de fuentes mediante el método [**AddFontFaceReference,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) como se muestra anteriormente.   
7. Una vez que se hayan agregado todas las fuentes al generador del conjunto de fuentes, cree el conjunto de fuentes personalizado, como se ha mostrado anteriormente.   
8. En algún momento en el que ya no se usarán las fuentes en memoria, anula el registro del cargador de archivos de fuentes en memoria. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Escenarios avanzados

Algunas aplicaciones pueden tener requisitos especiales que requieren un procesamiento más avanzado del descrito anteriormente. 

### <a name="combining-font-sets"></a>Combinación de conjuntos de fuentes

Es posible que algunas aplicaciones necesiten crear un conjunto de fuentes que conste de alguna combinación de elementos de otros conjuntos de fuentes. Por ejemplo, una aplicación puede querer crear un conjunto de fuentes que combine todas las fuentes instaladas en el sistema con una selección de fuentes personalizadas, o que combine fuentes instaladas que coincidan con determinados criterios con otras fuentes. DirectWrite API para admitir la manipulación y la combinación de conjuntos de fuentes. 

Para combinar dos o más conjuntos de fuentes, el método [**IDWriteFontSetBuilder::AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) agrega todas las fuentes de un conjunto de fuentes determinado para agregarlas a un generador de conjuntos de fuentes en una sola llamada. Si solo se quieren ciertas fuentes de un conjunto de fuentes existente en el nuevo conjunto de fuentes, el método [**IDWriteFontSet::GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) se puede usar para derivar un nuevo objeto de conjunto de fuentes que se ha filtrado para incluir solo fuentes que coincidan con las propiedades especificadas. Estos métodos proporcionan una manera sencilla de crear un conjunto de fuentes personalizado que combina fuentes a partir de dos o más conjuntos de fuentes existentes. 

### <a name="using-local-woff-or-woff2-font-data"></a>Uso de datos de fuente WOFF o WOFF2 locales

Si una aplicación tiene archivos de fuente en el sistema de archivos local o en un búfer de memoria, pero usan los formatos de contenedor WOFF o WOFF2, DirectWrite (Windows 10 Creator Update o posterior) proporciona un método para desempaquetar el formato del [**contenedor, IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), que devuelve [**un IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream). 

Sin embargo, la aplicación necesitará una manera de obtener [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) en un objeto de cargador de archivos de fuente. Una manera de hacerlo es crear una implementación [**personalizada de IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) que encapsula la secuencia. Al igual que con otros cargadores de archivos de fuente, debe registrarse antes de su uso y anular el registro antes de que el generador salga del ámbito.  

Si el cargador personalizado también se usará con archivos de fuente sin procesar (no empaquetados), la aplicación también tendría que proporcionar una implementación personalizada de la interfaz [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) para controlar esos archivos. Sin embargo, hay maneras más sencillas de usar las API descritas anteriormente para controlar archivos de fuente sin formato. La necesidad de una implementación de secuencia personalizada podría evitarse mediante el uso de rutas de acceso de código independientes para los archivos de fuente empaquetados frente a los archivos de fuente sin formato. 

Después de crear un objeto de cargador de archivos de fuentes personalizado, los datos del archivo de fuente empaquetado se agregan al cargador por medios específicos de la aplicación. El cargador puede controlar varios archivos de fuente, cada uno de los cuales se identifica mediante una clave definida por la aplicación que es opaca para DirectWrite. Después de agregar un archivo de fuente empaquetado al cargador, el método [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) se usa para obtener un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basado en ese cargador para los datos de fuente identificados por una clave determinada.  

El desempaquete real de los datos de fuente se puede realizar a medida que se agregan fuentes al cargador, pero también se puede controlar en el método [**IDWriteFontFileLoader::CreateStreamFromKey,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) al que llamará DirectWrite la primera vez que necesite leer los datos de fuente. 

Una vez creado un objeto IDWriteFontFile, los pasos restantes para agregar las fuentes a un conjunto de fuentes personalizado serán los descritos anteriormente. 

Una implementación que usa este enfoque se muestra en el ejemplo DirectWrite de conjuntos de fuentes [personalizados](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Uso DirectWrite de fuentes remotas con implementación de red de bajo nivel personalizada

Los mecanismos de DirectWrite para controlar las fuentes remotas se pueden dividir en mecanismos de nivel superior ( tener conjuntos de fuentes que incluyan referencias de caras de fuente para fuentes remotas, comprobar la localidad de los datos de fuente y administrar la cola para las solicitudes de descarga de fuentes) y los mecanismos de nivel inferior que controlan la descarga real. Es posible que algunas aplicaciones quieran usar los mecanismos de fuente remota de nivel superior, pero también requieren interacciones de red personalizadas, como la comunicación con servidores mediante protocolos distintos de HTTP. 

En esta situación, una aplicación deberá crear una implementación personalizada de la interfaz [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) que interactúe con otras interfaces de nivel inferior de las maneras necesarias. La aplicación también tendrá que proporcionar implementaciones personalizadas de estas interfaces de nivel inferior: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)e [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Estas tres interfaces tienen métodos de devolución de llamada que DirectWrite llamarán durante las operaciones de descarga. 

Cuando se llama a [**IDWriteFontDownloadQueue::BeginDownload,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) DirectWrite realizará consultas al cargador de archivos de fuente remoto sobre la localidad de los datos y solicitará la secuencia remota. Si los datos no son locales, llamarán al método BeginDownload de la secuencia. La implementación del flujo no debe bloquearse en esa llamada, pero debe devolverse inmediatamente, devolviendo un objeto [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) que proporciona el identificador de espera DirectWrite usará para esperar en la operación de descarga asincrónica. La implementación de secuencia personalizada es responsable de controlar la comunicación remota. Cuando se haya producido el evento de finalización, DirectWrite llamará a [**IDWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) para determinar el resultado de la operación. Si el resultado es correcto, se espera que las llamadas de ReadFragment subsiguientes a la secuencia de los intervalos descargados se completarán correctamente. 

> [!IMPORTANT]
> Nota de seguridad y rendimiento: Cuando se intenta capturar una fuente remota, existe la posibilidad en general de que un atacante suplante el servidor previsto al que se llama o que el servidor no responda. Si va a implementar interacciones de red personalizadas, puede tener un mayor control sobre las mitigaciones que cuando se trabaja con servidores de terceros. Sin embargo, es el usuario el que debe tener en cuenta las mitigaciones adecuadas para evitar la divulgación de información o la denegación de servicio. Se recomiendan protocolos seguros como HTTPS. Además, debe compilar en algún tiempo de espera para que el identificador de evento se devuelva a DirectWrite finalmente se establezca. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Escenarios de compatibilidad en versiones Windows anteriores

Los escenarios que se han descrito se pueden admiten en DirectWrite en versiones anteriores de Windows, pero requerirían una implementación mucho más personalizada por parte de la aplicación mediante las API más limitadas que estaban disponibles antes de Windows 10. Para obtener más información, vea Colecciones de fuentes [personalizadas (Windows 7/8).](custom-font-collections.md)

 

 
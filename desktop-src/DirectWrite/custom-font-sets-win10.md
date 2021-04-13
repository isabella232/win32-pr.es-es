---
title: Conjuntos de fuentes personalizadas
description: En este tema se describen varias maneras en las que puede usar fuentes personalizadas en la aplicación.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79f1ccfcb1dadd355c5f582417aacb5041ecf8b
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421601"
---
# <a name="custom-font-sets"></a>Conjuntos de fuentes personalizadas

En este tema se describen varias maneras en las que puede usar fuentes personalizadas en la aplicación.

-   [Aparición ](#introduction)
-   [Resumen de API](#summary-of-apis)
-   [Conceptos clave](#key-concepts)
-   [Fuentes y formatos de archivo de fuentes](#fonts-and-font-file-formats)
-   [Conjuntos de fuentes y colecciones de fuentes](#font-sets-and-font-collections)
-   [Escenarios comunes](#common-scenarios)
    -   [Crear un conjunto de fuentes usando fuentes arbitrarias en el sistema de archivos local](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Crear un conjunto de fuentes usando fuentes conocidas en el sistema de archivos local](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Crear un conjunto de fuentes personalizado mediante fuentes conocidas y remotas en la web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Crear un conjunto de fuentes personalizado con datos de fuente cargados en la memoria](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Escenarios avanzados](#advanced-scenarios)
    -   [Combinación de conjuntos de fuentes](#combining-font-sets)
    -   [Uso de datos de fuente WOFF o WOFF2 local ](#using-local-woff-or-woff2-font-data)
    -   [Usar los mecanismos de fuentes remotas de DirectWrite con implementación de red de bajo nivel personalizada ](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [Escenarios de compatibilidad con versiones anteriores de Windows ](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introducción

La mayoría de las veces, las aplicaciones usan las fuentes que se instalan localmente en el sistema. DirectWrite proporciona acceso a estas fuentes mediante los métodos [**IDWriteFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) o [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . En algunos casos, las aplicaciones también pueden querer usar fuentes que se incluyen como parte de Windows 10, pero que no están instaladas actualmente en el sistema actual. Se puede tener acceso a estas fuentes desde el servicio de fuentes de Windows mediante el método **GetSystemFontSet** o llamando a [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) con includeDownloadableFonts establecido en true. 

Sin embargo, en algunos escenarios de aplicación, las aplicaciones deben usar fuentes que no están instaladas en el sistema y que el servicio de fuentes de Windows no las proporciona. Estos son algunos ejemplos de estos escenarios:

-   Las fuentes se incrustan como recursos en un archivo binario de la aplicación.
-   Los archivos de fuentes se incluyen en un paquete de la aplicación y se almacenan en el disco en la carpeta de instalación de la aplicación.
-   La aplicación es una herramienta de desarrollo de fuentes que necesita cargar archivos de fuentes especificados por el usuario. 
-   Las fuentes se incrustan en archivos de documento que se pueden ver o editar en la aplicación. 
-   La aplicación usa fuentes obtenidas de un servicio de fuentes web público. 
-   La aplicación usa datos de fuente transmitidos a través de un protocolo de red privada. 

DirectWrite proporciona las API para trabajar con fuentes personalizadas en estos y otros escenarios similares. Los datos de fuentes personalizadas pueden provienen de archivos del sistema de archivos local; desde orígenes remotos basados en la nube a los que se tiene acceso mediante HTTP; o de orígenes arbitrarios después de haberse cargado en un búfer de memoria. 

> [!Note]  
> Aunque DirectWrite ha proporcionado API para trabajar con fuentes personalizadas desde Windows 7, las API más recientes se agregaron en Windows 10 y de nuevo en Windows 10 Creators Update (versión preliminar 15021 o posterior) que facilitan la implementación de varios de los escenarios mencionados. Este tema se centra en las API disponibles en Windows 10. Para las aplicaciones que necesitan trabajar en versiones anteriores de Windows, consulte [colecciones de fuentes personalizadas (Windows 7/8)](custom-font-collections.md). 

 

## <a name="summary-of-apis"></a>Resumen de API

Este tema se centra en la funcionalidad proporcionada por las siguientes API: 

-   Interfaz [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interfaz [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   Interfaz [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   Interfaz [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   Interfaz [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   [**IDWriteFactory:: CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) (método) 
-   [**IDWriteFactory:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) (método) 
-   [**IDWriteFactory3:: CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) (métodos) 
-   [**DWRITE \_ Estructura de la \_ propiedad Font**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ Enumeración de \_ \_ ID. de propiedad de fuente**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   Interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   [**IDWriteFactory:: RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) (método) 
-   [**IDWriteFactory:: UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) (método) 
-   [**IDWriteFactory5:: CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) (método) 
-   Interfaz [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   [**IDWriteFactory5:: CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) (método) 
-   Interfaz [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   Interfaz [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   Interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   Interfaz [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   Interfaz [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   Interfaz [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   [**IDWriteFactory5:: AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) (método) 
-   [**IDWriteFactory5:: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) (método) 

 

## <a name="key-concepts"></a>Conceptos clave

Para comprender las API de DirectWrite para trabajar con fuentes personalizadas, puede ser útil comprender el modelo conceptual subyacente a estas API. Aquí se describen los conceptos clave. 

Cuando DirectWrite realiza el diseño de texto real o la representación, necesita tener acceso a los datos de la fuente real. Un objeto de fuente de fuentes contiene datos de fuentes reales, que deben existir en el sistema local. Pero para otras operaciones, como la comprobación de la disponibilidad de una fuente determinada o la presentación de opciones de fuente para un usuario, todo lo que se necesita es una referencia a una fuente determinada, no los propios datos de la fuente. En DirectWrite, un objeto de referencia de tipo Font contiene solo la información necesaria para buscar y crear una instancia de una fuente. Dado que la referencia de la fuente de fuentes no contiene datos reales, DirectWrite puede tratar las referencias de la fuente para los datos reales que se encuentran en una ubicación de red remota, así como cuando los datos reales son locales.

Un conjunto de fuentes es un conjunto de referencias de la fuente de fuentes, junto con ciertas propiedades básicas e informativas que se pueden usar para hacer referencia a la fuente o para compararla con otras fuentes, como el nombre de familia o un valor de fuente-peso. Los datos reales de las distintas fuentes pueden ser locales o bien pueden ser remotos o una mezcla.

Se puede utilizar un conjunto de fuentes para obtener un objeto de colección de fuentes correspondiente. Para obtener más información, vea conjuntos de fuentes y colecciones de fuentes. 

La interfaz IDWriteFontSet proporciona métodos que permiten consultar valores de propiedad como el nombre de la familia o el espesor de fuente, o las referencias de la fuente que coinciden con valores de propiedad concretos. Después de filtrar hasta una selección determinada, se puede obtener una instancia de la interfaz [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) , con métodos para descargar (si los datos de fuentes reales actualmente son remotos), para obtener el objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) correspondiente que se puede usar para el diseño y la representación. 

La interfaz IDWriteFontFile se basa en cada tipo de fuente o referencia de fuente. Representa la ubicación de un archivo de fuentes y tiene dos componentes: un cargador de archivos de fuentes y una clave de archivo de fuente. El cargador de archivos de fuentes ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) se usa para abrir un archivo si es necesario y devuelve una secuencia con los datos ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Dependiendo del cargador, los datos pueden estar ubicados en una ruta de acceso de archivo local, una dirección URL remota o en un búfer de memoria. La clave es un valor definido por el cargador que identifica de forma única el archivo en el contexto del cargador, lo que permite al cargador buscar los datos y crear un flujo para él. 

Las fuentes personalizadas se pueden agregar fácilmente a un conjunto de fuentes personalizado, que a su vez se puede usar para filtrar u organizar la información de fuente para propósitos como la creación de una interfaz de usuario del selector de fuentes. El conjunto de fuentes también puede usarse para crear una colección de fuentes para su uso en API de nivel superior como [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). La interfaz [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) se puede usar para crear un conjunto de fuentes personalizado que incluya varias fuentes personalizadas. También se puede usar para crear un conjunto de fuentes personalizado que mezcla fuentes personalizadas y fuentes proporcionadas por el sistema; o que mezcla las fuentes con distintos orígenes para los datos reales: el almacenamiento local, las direcciones URL remotas y la memoria. 

Como se mencionó, una referencia de fuente puede hacer referencia a los datos de fuente de un origen remoto, pero los datos deben ser locales para obtener un objeto de fuente de fuentes que se pueda usar para el diseño y la representación. La descarga de datos remotos se controla mediante una cola de descarga de fuentes. Las aplicaciones pueden usar la interfaz [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) para poner en cola las solicitudes para descargar fuentes remotas con el fin de iniciar el proceso de descarga y registrar un objeto [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) para que realice una acción cuando se complete el proceso de descarga. 

Para la mayoría de las interfaces que se describen aquí, DirectWrite proporciona implementaciones del sistema. La única excepción es la interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) , que una aplicación implementa para realizar acciones específicas de la aplicación cuando se han descargado localmente fuentes remotas. Las aplicaciones pueden tener razones para proporcionar sus propias implementaciones personalizadas para algunas otras interfaces, aunque esto solo se necesita en escenarios específicos y más avanzados. Por ejemplo, una aplicación necesitaría proporcionar una implementación personalizada de la interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) para controlar los archivos de fuente en el almacenamiento local que usan el formato de contenedor WOFF2. A continuación se proporcionan detalles adicionales. 

## <a name="fonts-and-font-file-formats"></a>Fuentes y formatos de archivo de fuentes

Otro concepto clave que resulta útil comprender es la relación entre las caras de fuente individuales y los archivos de fuente que los contienen. La idea de un archivo de fuentes OpenType (. ttf o. otf) que contiene una sola fuente resulta familiar. Sin embargo, el formato de fuente OpenType también permite una colección de fuentes OpenType (. TTC o. OTC), que es un único archivo que contiene varias fuentes. Los archivos de colección OpenType se suelen usar para fuentes grandes que están estrechamente relacionadas y tienen valores idénticos para determinados datos de fuente: al combinar las fuentes en un solo archivo, se pueden desduplicar los datos comunes. Por esta razón, una referencia de fuente o fuente de fuente debe hacer referencia no solo a un archivo de fuente (o a un origen de datos equivalente), pero también debe especificar un índice de fuente dentro de ese archivo, para el caso general en el que el archivo puede ser un archivo de colección. 

En el caso de las fuentes usadas en la web, los datos de la fuente se suelen empaquetar en ciertos formatos de contenedor, WOFF o WOFF2, que proporcionan cierta compresión de los datos de la fuente y cierto nivel de protección contra la piratería y la infracción de las licencias de fuentes. Funcionalmente, un archivo WOFF o WOFF2 es equivalente a una fuente OpenType o un archivo de colección de fuentes, pero los datos se codifican en un formato diferente que requiere desempaquetar antes de que se pueda usar. 

Ciertas API de DirectWrite pueden tratar con caras de fuente individuales, mientras que otras API pueden controlar archivos que podrían incluir archivos de colección OpenType que contienen varias caras. Del mismo modo, algunas API solo tratan los datos sin formato de OpenType, mientras que otras API pueden administrar los formatos de contenedor empaquetado, WOFF y WOFF2. Estos detalles se proporcionan en la siguiente discusión. 

## <a name="font-sets-and-font-collections"></a>Conjuntos de fuentes y colecciones de fuentes

Algunas aplicaciones pueden implementarse para trabajar con fuentes mediante la interfaz [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) . Existe una correspondencia directa entre una colección de fuentes y un conjunto de fuentes. Cada una de ellas puede contener las mismas fuentes, pero presentarlas con otra organización. Desde cualquier colección de fuentes, se puede obtener un conjunto de fuentes correspondiente y viceversa.

Cuando se trabaja con varias fuentes personalizadas, es más fácil utilizar una interfaz de generador de conjuntos de fuentes para crear un conjunto de fuentes personalizado y, a continuación, obtener una colección de fuentes una vez creado el conjunto de fuentes. El proceso para crear un conjunto de fuentes personalizado se describe en detalle a continuación. Para obtener una interfaz [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) a partir de un conjunto de fuentes, se usa el método [**IDWriteFactory3:: CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) .

Si la aplicación tiene un objeto de colección y necesita obtener un conjunto de fuentes correspondiente, puede hacerlo mediante el método [**IDWriteFontCollection1:: GetFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) . 

## <a name="common-scenarios"></a>Escenarios frecuentes

En esta sección se describen algunos de los escenarios más comunes que implican conjuntos de fuentes personalizados:

-   Crear un conjunto de fuentes personalizado mediante fuentes arbitrarias en las rutas de acceso del sistema de archivos local.
-   Creación de un conjunto de fuentes personalizado mediante fuentes conocidas (tal vez que se incluyen con la aplicación) que se almacenan en el sistema de archivos local.
-   Crear un conjunto de fuentes personalizado mediante fuentes conocidas y remotas en la Web.
-   Crear un conjunto de fuentes personalizado utilizando los datos de fuente cargados en la memoria.

Las implementaciones completas de estos escenarios se proporcionan en el [ejemplo de conjuntos de fuentes personalizadas de DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). En ese ejemplo también se muestra un escenario más avanzado para controlar los datos de fuente empaquetados en los formatos de contenedor WOFF o WOFF2, que se tratarán a continuación. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Crear un conjunto de fuentes usando fuentes arbitrarias en el sistema de archivos local

Cuando se trabaja con un conjunto arbitrario de archivos de fuentes en el almacenamiento local, el método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) es conveniente ya que, en una sola llamada, puede controlar todos los rostros de fuente de un archivo de colección de fuentes OpenType, así como todas las instancias de una fuente de variable OpenType. Está disponible en Windows 10 Creators Update (versión preliminar 15021 o posterior) y se recomienda siempre que esté disponible. 

Para usar este método, utilice el siguiente proceso.

<dl> 1. Empiece por crear la interfaz <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> : 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Use el generador para obtener la <a href=""></a> interfaz [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) : 


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



   
4. Agregue el objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generador de conjuntos de fuentes con el método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) : 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Si la ruta de acceso al archivo especificada en la llamada a [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) hace referencia a otro archivo compatible con OpenType, la llamada a [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) devolverá un error, DWRITE \_ E \_ FILEFORMAT.

5. Una vez que se han agregado todos los archivos al generador de conjuntos de fuentes, se puede crear el conjunto de fuentes personalizado: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

Si la aplicación necesita ejecutarse en versiones de Windows 10 anteriores a Windows 10 Creators Update, el método AddFontFile no estará disponible. La disponibilidad se puede detectar mediante la creación de una interfaz [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) y el uso de QueryInterface para intentar obtener una interfaz [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) : Si esto se realiza correctamente, la interfaz [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) y el método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) también estarán disponibles.

Si el método AddFontFile no está disponible, se debe usar el método [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) para agregar caras de fuente individuales. Para permitir archivos de colección de fuentes OpenType que contengan varias caras, el método [**IDWriteFontFile:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) se puede usar para determinar el número de caras incluidas en el archivo. El proceso es el siguiente.

<dl> 1. Empiece por crear la interfaz <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> : 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Use el generador para obtener la interfaz [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) : 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Para cada archivo de fuente, cree un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), como se indica a continuación: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



En lugar de agregar el archivo directamente al generador de conjuntos de fuentes, es necesario determinar el número de caras y crear objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuales.   
4. Use el método [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para obtener el número de caras del archivo. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



El método [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) también establecerá los valores para los parámetros IsSupported y filetype. Si el archivo no es un formato admitido, isSupported será FALSE y se puede tomar la acción adecuada, como omitir el archivo.   
5. Recorra el número de fuentes establecidas en el parámetro numberOfFonts. Dentro del bucle, cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) para cada par de archivo/índice y agréguelo al generador de conjuntos de fuentes. 


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



  
6. Una vez que se hayan agregado todas las caras al generador de conjuntos de fuentes, cree el conjunto de fuentes personalizado, como se muestra anteriormente.  
</dl>

Una aplicación se puede diseñar para que use el método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) preferido cuando se ejecuta en Windows 10 Creators Update, pero revertir para usar el método [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) cuando se ejecuta en versiones anteriores de Windows 10. Compruebe la disponibilidad de la interfaz [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) , como se describió anteriormente y, a continuación, haga una bifurcación en consecuencia. Este enfoque se ilustra en el [ejemplo de conjuntos de fuentes personalizadas de DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Crear un conjunto de fuentes usando fuentes conocidas en el sistema de archivos local

Tal y como se mencionó anteriormente, cada referencia de fuente de un conjunto de fuentes está asociada con determinadas propiedades informativas, como el nombre de familia y el espesor de fuente. Cuando se agregan fuentes personalizadas a un generador de conjuntos de fuentes mediante las llamadas a la API mencionadas anteriormente, estas propiedades informativas se obtienen directamente de los datos reales de la fuente, que se leen cuando se agrega la fuente. En algunas situaciones, sin embargo, si una aplicación tiene otro origen de información sobre una fuente, es posible que desee proporcionar sus propios valores personalizados para estas propiedades. 

Como ejemplo de cómo podría ser útil, supongamos que una aplicación agrupa algunas fuentes que se usan para presentar determinados elementos de la interfaz de usuario dentro de la aplicación. En ocasiones, como en el caso de una nueva versión de la aplicación, puede que sea necesario cambiar las fuentes específicas que usa la aplicación para estos elementos. Si la aplicación tiene referencias codificadas a fuentes específicas, el reemplazo de una fuente con otra tendrá que cambiar cada una de esas referencias. En su lugar, si la aplicación usa propiedades personalizadas para asignar alias funcionales en función del tipo de elemento o texto que se va a representar, asigna cada alias a una fuente específica en un lugar y, a continuación, usa los alias en todos los contextos donde se crean y manipulan las fuentes, y después reemplaza una fuente por otra, solo es necesario cambiar el único lugar en el que se 

Se pueden asignar valores personalizados para propiedades informativas cuando se llama al método [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) . El método para hacerlo es el siguiente: se puede usar en cualquier versión de Windows 10. 

Como se mostró anteriormente, empiece por obtener las interfaces [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) y [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) . Para cada fuente personalizada que se va a agregar, cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), como se mostró anteriormente. Antes de que se agregue al generador de conjuntos de fuentes (dentro del bucle en el paso 5, mostrado anteriormente), la aplicación define los valores de propiedad personalizados que se usarán. 

Un conjunto de valores de propiedad personalizados se define mediante una matriz de estructuras de [**\_ \_ propiedades de fuente DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) . Cada uno de ellos identifica una propiedad determinada de la enumeración de identificador de la [**\_ propiedad de fuente \_ \_ DWRITE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) y el valor de propiedad correspondiente que se va a usar.  

Tenga en cuenta que todos los valores de propiedad se asignan como cadenas. Si posteriormente se pueden mostrar a los usuarios, se pueden establecer valores alternativos para una propiedad determinada para distintos idiomas, pero esto no es necesario. Tenga en cuenta también que si la aplicación establece cualquier valor de propiedad personalizada, solo se usarán en el conjunto de fuentes los valores especificados. DirectWrite no derivará ningún valor directamente de la fuente para las propiedades informativas usadas en un conjunto de fuentes. 

En el ejemplo siguiente se definen los valores personalizados para tres propiedades informativas: nombre de familia, nombre completo y espesor de fuente. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Después de definir la matriz deseada de valores de propiedad para una fuente, realice una llamada a AddFontFaceRefence, pasando la matriz de propiedades, así como la referencia de la fuente. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Una vez que se han agregado todos los rostros de fuente personalizados al generador de conjuntos de fuentes, junto con sus propiedades personalizadas, cree el conjunto de fuentes personalizado, como se mostró anteriormente. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Crear un conjunto de fuentes personalizado mediante fuentes conocidas y remotas en la web

Las propiedades personalizadas son importantes para trabajar con fuentes remotas. Cada referencia de fuente debe tener algunas propiedades informativas para caracterizar la fuente y diferenciarla de otras fuentes. Dado que los datos de fuente para fuentes remotas no son locales, DirectWrite no puede derivar propiedades directamente de los datos de fuente. Por lo tanto, las propiedades se deben proporcionar explícitamente al agregar una fuente remota al generador de conjuntos de fuentes.

La secuencia de llamadas API para agregar fuentes remotas a un conjunto de fuentes es similar a la secuencia descrita para el escenario anterior. Dado que los datos de fuente son remotos, sin embargo, las operaciones que se realizan para leer los datos de la fuente real serán diferentes a cuando se trabaja con archivos en el almacenamiento local. En esta situación, se ha agregado una nueva interfaz de nivel inferior, [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader), a Windows 10 Creators Update. 

Para usar el cargador de archivos de fuentes remotos, primero se debe registrar con un generador de DirectWrite. El cargador deberá ser mantenido por la aplicación mientras se utilicen las fuentes asociadas a él. Una vez que las fuentes ya no estén en uso y, en algún momento antes de que se destruya el generador, se debe anular el registro del cargador. Esto puede hacerse en el destructor de la clase que posee el objeto Loader. Estos pasos se mostrarán a continuación. 

El método para crear un conjunto de fuentes personalizado mediante fuentes remotas es el siguiente: Esto requiere Windows 10 Creators Update.  

<dl> 1. Cree una interfaz IDWriteFactory5, como se mostró anteriormente.   
2. Cree una interfaz <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> , como se mostró anteriormente.   
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



Esto devuelve una implementación proporcionada por el sistema de la interfaz del cargador de archivos de fuentes remotos que puede controlar las interacciones HTTP para descargar datos de fuentes en nombre de la aplicación. Se puede especificar una dirección URL de referencia o encabezados adicionales si es necesario para el servicio de fuente o los servicios que son el origen de las fuentes.    

> [!IMPORTANT]
> Nota de seguridad: cuando se realiza un intento de capturar una fuente remota, existe la posibilidad de que un atacante suplante el servidor previsto al que se llamará. En ese caso, las direcciones URL de destino y de referencia y los detalles del encabezado se divulgarán al atacante. Los desarrolladores de aplicaciones son responsables de mitigar este riesgo. Se recomienda el uso del protocolo HTTPS en lugar de HTTP. 

 

Se puede usar un cargador de archivos de fuente remoto único para varias fuentes, aunque se pueden usar diferentes cargadores Si se obtienen fuentes de varios servicios que tienen requisitos diferentes para la URL de referencia o encabezados adicionales.   
4. Registre el cargador de archivos de fuentes remotos con el generador. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



Desde este punto, los pasos para crear el conjunto de fuentes personalizado son similares a los descritos para los archivos de fuentes locales conocidos, con dos excepciones importantes. En primer lugar, el objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) se crea con la interfaz del cargador de archivos de fuentes remoto en lugar de usar el generador. En segundo lugar, no se puede usar el método Analyze, ya que los datos de fuente no son locales. En su lugar, la aplicación debe saber si el archivo de fuente remoto es un archivo de colección de fuentes OpenType y, en ese caso, debe saber cuál de las fuentes de la colección usará y el índice de cada uno. Por lo tanto, los pasos restantes son los siguientes.   
5. Para cada archivo de fuente remota, utilice la interfaz del cargador de archivos de fuentes remotos para crear un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), especificando la dirección URL necesaria para obtener acceso al archivo de fuente. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Tenga en cuenta que se puede especificar la dirección URL completa en el parámetro fontFileUrl, o bien se puede dividir en partes base y relativas. Si se especifica una dirección URL base, la concatenación de los valores baseUrl y fontFileUrl debe proporcionar la dirección URL completa; DirectWrite no proporcionará ningún delimitador adicional.  

> [!IMPORTANT]
> Seguridad y rendimiento NOTA: cuando se realiza un intento de capturar una fuente remota, no hay ninguna garantía de que Windows reciba una respuesta del servidor. En algunos casos, un servidor puede responder con un error de archivo no encontrado para una dirección URL relativa no válida, pero dejar de responder si recibe varias solicitudes no válidas. Si el servidor no responde, se agotará el tiempo de espera de Windows, aunque esto puede tardar varios minutos si se inician varias capturas. Debe hacer lo que pueda para asegurarse de que las direcciones URL serán válidas cuando se realicen las llamadas. 

 

Además, tenga en cuenta que la dirección URL puede apuntar a un archivo de fuente OpenType sin formato (. ttf,. OTF,. TTC,. OTC), pero también puede apuntar a fuentes de un archivo contenedor WOFF o WOFF2. Si se hace referencia a un archivo WOFF o WOFF2, la implementación de DirectWrite del cargador de archivos de fuente remoto desempaquetará automáticamente los datos de fuente del archivo contenedor.   
6. Cree un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)para cada índice de fuente del archivo de fuentes remoto que se va a usar. 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Defina las propiedades personalizadas para el tipo de fuente, como se muestra anteriormente.   
8. Agregue la referencia de fuente junto con propiedades personalizadas al generador de conjuntos de fuentes, como se mostró anteriormente.   
9. Una vez que se hayan agregado todas las fuentes al generador de conjuntos de fuentes, cree el conjunto de fuentes, como se mostró anteriormente.   
10. En algún momento en el que ya no se usarán las fuentes remotas, anule el registro del cargador de archivos de fuentes remotos. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Una vez que se crea un conjunto de fuentes personalizadas con fuentes remotas personalizadas, el conjunto de fuentes contiene referencias y propiedades informativas para las fuentes remotas, pero los datos reales siguen siendo remotos. La compatibilidad con DirectWrite para fuentes remotas permite mantener una referencia de fuente de fuentes en el conjunto de fuentes y seleccionar una fuente para su uso en el diseño y la representación, pero no se descargan los datos reales hasta que haya una necesidad real de utilizarlos, como cuando se realiza el diseño de texto.  

Una aplicación puede adoptar un enfoque inicial solicitando que DirectWrite Descargue los datos de la fuente y, a continuación, esperando la confirmación de una descarga correcta antes de que se inicie cualquier procesamiento con la fuente. Pero una descarga de red implica cierta latencia de duración imprevisible y el éxito también es incierto. Por esta razón, normalmente será mejor adoptar un enfoque diferente, lo que permite que el diseño y la representación se realicen inicialmente con fuentes alternativas o de reserva que ya son locales, al tiempo que se solicita la descarga de la fuente remota deseada en paralelo y, a continuación, se actualizan los resultados una vez que se ha descargado la fuente deseada. 

Para solicitar que se descargue toda la fuente antes de su uso, se puede usar el método [**IDWriteFontFaceReference:: EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) . Si la fuente es muy grande, solo puede ser necesaria una parte de los datos para procesar cadenas determinadas. DirectWrite proporciona métodos adicionales que se pueden usar para solicitar partes de los datos de fuentes necesarios para el contenido determinado, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) y [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest).  

Supongamos que el enfoque que se va a realizar en la aplicación es permitir que el procesamiento se realice inicialmente usando fuentes locales, alternativas o de reserva. El método IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) se puede usar para identificar fuentes de reserva locales y también pone en cola automáticamente una solicitud para descargar la fuente preferida. Además, si se usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y parte o todo el texto del diseño está formateado mediante una referencia de fuente remota, DirectWrite usará automáticamente el método **MapCharacters** para obtener las fuentes de reserva locales y poner en cola una solicitud para descargar los datos de fuentes remotas. 

DirectWrite mantiene una cola de descarga de fuentes para cada generador y las solicitudes realizadas con los métodos mencionados anteriormente se agregan a esa cola. La cola de descarga de fuentes se puede obtener mediante el método [**IDWriteFactory3:: GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) . 

Si se realiza una solicitud de descarga pero los datos de la fuente ya son locales, se producirá una operación no operativa: no se agregará nada a la cola de descarga. Una aplicación puede comprobar si la cola está vacía o si hay solicitudes de descarga pendientes llamando al método [**IDWriteFontDownloadQueue:: IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) . 

Una vez agregadas las solicitudes de fuentes remotas a la cola, se debe iniciar el proceso de descarga. Cuando se usan fuentes remotas en [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout), la descarga se inicia automáticamente cuando la aplicación llama a los métodos **IDWriteTextLayout** que fuerzan las operaciones de diseño o representación, como los métodos GetLineMetrics o Draw. En otros escenarios, la aplicación debe iniciar la descarga directamente llamando a [**IDWriteFontDownloadQueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Una vez completada la descarga, la aplicación puede tomar las medidas adecuadas: continuar con las operaciones pendientes o repetir las operaciones que se realizaron inicialmente con fuentes de reserva. (Si se usa el diseño de texto de DirectWrite, se puede usar [**IDWriteTextLayout3:: InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) para borrar los resultados temporales calculados mediante fuentes de reserva). Para que la aplicación reciba una notificación cuando se complete el proceso de descarga y tome las medidas oportunas, la aplicación debe proporcionar una implementación de la interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) y pasarla a la llamada a BeginDownload. 

> [!IMPORTANT]
> Seguridad y rendimiento NOTA: cuando se realiza un intento de capturar una fuente remota, no hay ninguna garantía de que Windows reciba una respuesta del servidor. Si el servidor no responde, se agotará el tiempo de espera de Windows, aunque esto puede tardar varios minutos si se capturan varias fuentes remotas pero se produce un error. La llamada a BeginDownload se devolverá inmediatamente. Las aplicaciones no deben bloquear la interfaz de usuario mientras esperan a que se llame a [**IDWriteFontDownloadListener::D ownloadcompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) . 

 

Las implementaciones de ejemplo de estas interacciones con la cola de descarga de fuentes de DirectWrite y la interfaz [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) se pueden visualizar en el [ejemplo de conjuntos de fuentes personalizadas](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)de directwrite y también en el ejemplo de [fuentes descargables de directwrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Crear un conjunto de fuentes personalizado con datos de fuente cargados en la memoria

Del mismo modo que las operaciones de bajo nivel para leer los datos de un archivo de fuente son diferentes para los archivos de un disco local en lugar de los archivos remotos en la web, también se cumple lo mismo con los datos de fuente cargados en un búfer de memoria. Se ha agregado una nueva interfaz de bajo nivel para controlar los datos de fuentes en memoria en Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader). 

Al igual que con un cargador de archivos de fuentes remoto, primero se debe registrar un cargador de archivos de fuentes en memoria con un generador de DirectWrite. El cargador deberá ser mantenido por la aplicación mientras se utilicen las fuentes asociadas a él. Una vez que las fuentes ya no estén en uso y, en algún momento antes de que se destruya el generador, se debe anular el registro del cargador. Esto puede hacerse en el destructor de la clase que posee el objeto Loader. Estos pasos se mostrarán a continuación. 

Si la aplicación tiene información independiente sobre los rostros de fuente representados por los datos, puede Agregar referencias de rostro de fuente individuales a un generador de conjuntos de fuentes con propiedades personalizadas especificadas. Sin embargo, dado que los datos de fuente están en la memoria local, esto no es necesario; DirectWrite podrá leer los datos directamente para derivar los valores de propiedad. 

DirectWrite supone que los datos de la fuente están en formato OpenType sin formato, equivalente a un archivo OpenType (. ttf,. OTF,. TTC,. OTC), pero en memoria en lugar de en disco. Los datos no pueden estar en un formato de contenedor WOFF o WOFF2. Los datos pueden representar una colección de fuentes OpenType. Si no se utilizan propiedades personalizadas, el método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) se puede usar para agregar todos los rostros de fuente de los datos en una sola llamada. 

Una consideración importante para el escenario en memoria es la duración de los datos. Si se proporciona un puntero al búfer en DirectWrite sin una indicación clara de que hay un propietario, DirectWrite realizará una copia de los datos en un nuevo búfer de memoria que será de su propiedad. Para evitar la copia de datos y la asignación de memoria adicional, la aplicación puede pasar un objeto de propietario de datos que implementa IUnknown y que posee el búfer de memoria que contiene los datos de la fuente. Mediante la implementación de esta interfaz, DirectWrite puede Agregar al recuento de referencias del objeto, lo que garantiza la duración de los datos de propiedad. 

El método para crear un conjunto de fuentes personalizado mediante datos de fuentes en memoria es el siguiente: Esto requiere Windows 10 Creators Update. Esto supondrá un objeto de propietario de datos implementado por la aplicación, que implementa IUnknown y que también tiene métodos que devuelven un puntero al búfer de memoria y el tamaño del búfer. 

<dl> 1. Cree una interfaz IDWriteFactory5, como se mostró anteriormente.  
2. Cree una interfaz [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) , como se mostró anteriormente.  
3. Use el generador para obtener un IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Esto devuelve una implementación proporcionada por el sistema de la interfaz del cargador de archivos de fuentes en memoria.   
4. Registre el cargador de archivos de fuentes en memoria con el generador. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Para cada archivo de fuente en memoria, use el cargador de archivos de fuentes en memoria para crear un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile). 


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



   
6. Agregue el objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) al generador de conjuntos de fuentes con el método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) , como se mostró anteriormente.  En cambio, si es necesario, la aplicación puede crear objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuales basados en **IDWriteFontFile**, definir opcionalmente las propiedades personalizadas de cada referencia de fuente y, a continuación, agregar la referencia de la fuente con las propiedades personalizadas al conjunto de fuentes mediante el método [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , como se mostró anteriormente.   
7. Una vez que se hayan agregado todas las fuentes al generador de conjuntos de fuentes, cree el conjunto de fuentes personalizado, como se muestra anteriormente.   
8. En algún momento en el que ya no se usarán las fuentes en memoria, anule el registro del cargador de archivos de fuentes en memoria. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Escenarios avanzados

Algunas aplicaciones pueden tener requisitos especiales que requieren un procesamiento más avanzado del descrito anteriormente. 

### <a name="combining-font-sets"></a>Combinación de conjuntos de fuentes

Es posible que algunas aplicaciones necesiten crear un conjunto de fuentes que incluya una combinación de elementos de otros conjuntos de fuentes. Por ejemplo, es posible que una aplicación desee crear un conjunto de fuentes que combine todas las fuentes instaladas en el sistema con una selección de fuentes personalizadas, o que combine las fuentes instaladas que coincidan con ciertos criterios con otras fuentes. DirectWrite tiene API para admitir la manipulación y la combinación de conjuntos de fuentes. 

Para combinar dos o más conjuntos de fuentes, el método [**IDWriteFontSetBuilder:: AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) agrega todas las fuentes del conjunto de fuentes dado que se van a agregar a un generador de conjuntos de fuentes en una sola llamada. Si solo se desean ciertas fuentes de un conjunto de fuentes existente en el nuevo conjunto de fuentes, el método [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) se puede usar para derivar un nuevo objeto de conjunto de fuentes que se ha filtrado para incluir solo las fuentes que coinciden con las propiedades especificadas. Estos métodos proporcionan una manera sencilla de crear un conjunto de fuentes personalizado combinando fuentes a partir de dos o más conjuntos de fuentes existentes 

### <a name="using-local-woff-or-woff2-font-data"></a>Uso de datos de fuente WOFF o WOFF2 local

Si una aplicación tiene archivos de fuentes en el sistema de archivos local o en un búfer de memoria, pero usan los formatos de contenedor WOFF o WOFF2, DirectWrite (Windows 10 Creator Update o posterior) proporciona un método para desempaquetar el formato del contenedor, [**IDWriteFactory5:: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), que devuelve una [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream). 

Sin embargo, la aplicación necesitará una manera de obtener el [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) en un objeto de cargador de archivos de fuentes. Una manera de hacerlo es crear una implementación de [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) personalizada que incluya la secuencia. Al igual que con otros cargadores de archivos de fuentes, se debe registrar antes de usar y anular el registro antes de que el generador salga del ámbito.  

Si el cargador personalizado también se va a usar con archivos de fuente sin procesar (no empaquetados), la aplicación también debe proporcionar una implementación personalizada de la interfaz [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) para administrar esos archivos. Sin embargo, hay maneras más fáciles de usar las API descritas anteriormente para administrar archivos de fuentes sin procesar. La necesidad de una implementación de secuencia personalizada podría evitarse mediante rutas de acceso de código independientes para los archivos de fuente empaquetados frente a los archivos de fuentes sin formato. 

Después de crear un objeto cargador de archivos de fuentes personalizado, los datos del archivo de fuentes empaquetados se agregan al cargador mediante medios específicos de la aplicación. El cargador puede controlar varios archivos de fuente, cada uno de los cuales se identifica mediante una clave definida por la aplicación que es opaca para DirectWrite. Una vez que se ha agregado un archivo de fuente empaquetado al cargador, se usa el método [**IDWriteFactory:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) para obtener un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basado en ese cargador para los datos de fuente identificados por una clave determinada.  

El desempaquetado real de los datos de fuente se puede realizar a medida que se agregan fuentes al cargador, pero también se pueden controlar en el método [**IDWriteFontFileLoader:: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) , al que DirectWrite llamará cuando necesite leer los datos de la fuente por primera vez. 

Después de crear un objeto IDWriteFontFile, los pasos restantes para agregar las fuentes a un conjunto de fuentes personalizado serán como se describió anteriormente. 

Una implementación que usa este enfoque se ilustra en el [ejemplo de conjuntos de fuentes personalizadas de DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Usar los mecanismos de fuentes remotas de DirectWrite con implementación de red de bajo nivel personalizada

Los mecanismos de DirectWrite para administrar fuentes remotas se pueden dividir en mecanismos de nivel superior, con conjuntos de fuentes que incluyen referencias de fuentes de fuentes para fuentes remotas, comprobando la localidad de los datos de fuentes y administrando la cola para las solicitudes de descarga de fuentes, y los mecanismos de nivel inferior que controlan la descarga real. Es posible que algunas aplicaciones deseen usar los mecanismos de fuentes remotas de nivel superior, pero también requieren interacciones de red personalizadas, como la comunicación con servidores que usan protocolos distintos de HTTP. 

En esta situación, una aplicación tendrá que crear una implementación personalizada de la interfaz [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) que interactúe con otras interfaces de nivel inferior de las maneras necesarias. La aplicación también tendrá que proporcionar implementaciones personalizadas de estas interfaces de nivel inferior: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)y [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Estas tres interfaces tienen métodos de devolución de llamada a los que DirectWrite llamará durante las operaciones de descarga. 

Cuando se llama a [**IDWriteFontDownloadQueue:: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) , DirectWrite realizará consultas en el cargador del archivo de fuentes remoto sobre la localidad de los datos y solicitará la secuencia remota. Si los datos no son locales, llamará al método BeginDownload de la secuencia. La implementación de la secuencia no debe bloquearse en esa llamada, pero debe devolver inmediatamente, devolviendo un objeto [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) que proporciona el identificador de espera que DirectWrite usará para esperar en la operación de descarga asincrónica. La implementación de secuencia personalizada es responsable de controlar la comunicación remota. Cuando se ha producido el evento de finalización, DirectWrite llamará a [**IDWriteAsyncResult:: GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) para determinar el resultado de la operación. Si el resultado es correcto, se espera que las llamadas posteriores a ReadFragment a la secuencia de los intervalos descargados se realicen correctamente. 

> [!IMPORTANT]
> Seguridad/Nota de rendimiento: cuando se realiza un intento de obtener una fuente remota, existe la posibilidad de que un atacante suplante el servidor previsto al que se está llamando o que el servidor no responda. Si va a implementar interacciones de red personalizadas, puede tener un mayor control sobre las mitigaciones que cuando se trabaja con servidores de terceros. Sin embargo, depende de usted tener en cuenta las mitigaciones adecuadas para evitar la divulgación de información o la denegación de servicio. Se recomiendan protocolos seguros, como HTTPS. Además, debe compilar en algún tiempo de espera para que el controlador de eventos devuelto a DirectWrite se establezca finalmente. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Escenarios de compatibilidad con versiones anteriores de Windows

Los escenarios que se han descrito pueden admitirse en DirectWrite en versiones anteriores de Windows, pero necesitarían una implementación más personalizada en la parte de la aplicación con las API más limitadas que estaban disponibles antes de Windows 10. Para obtener más información, vea [colecciones de fuentes personalizadas (Windows 7/8)](custom-font-collections.md).

 

 
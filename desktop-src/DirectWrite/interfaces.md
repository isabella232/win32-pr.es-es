---
title: Interfaces de DirectWrite
description: Enumera las interfaces definidas por DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0297875bfe4b5f0a0610091f7330a427ed51b822
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105670049"
---
# <a name="directwrite-interfaces"></a>Interfaces de DirectWrite

DirectWrite define las interfaces siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Representa el resultado de una operación asincrónica. Un cliente puede utilizar la interfaz para esperar a que se complete la operación y para obtener el resultado.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y un contexto de dispositivo, que se puede usar para representar glifos. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y un contexto de dispositivo, que se puede usar para representar glifos. |
| [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y un contexto de dispositivo, que se puede usar para representar glifos. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Esta interfaz permite a la aplicación enumerar a través de las ejecuciones del glifo de color. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumerador para una colección ordenada de ejecuciones de glifo de color. |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Se usa para crear todos los objetos de DirectWrite subsiguientes. Esta interfaz es la interfaz de fábrica raíz para todos los objetos de DirectWrite. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | La interfaz de fábrica raíz para todos los objetos de [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory2**](idwritefactory2.md) | La interfaz de fábrica raíz para todos los objetos de [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | La interfaz de fábrica raíz para todos los objetos de [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | La interfaz de fábrica raíz para todos los objetos de DirectWrite. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | La interfaz de fábrica raíz para todos los objetos de DirectWrite. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Representa un objeto de generador del que se crean todos los objetos de DirectWrite. **IDWriteFactory6** agrega nuevas instalaciones para trabajar con fuentes y recursos de fuentes. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Esta interfaz representa un objeto de generador del que se crean todos los objetos de DirectWrite. **IDWriteFactory7** agrega nuevas instalaciones para trabajar con fuentes del sistema. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Representa una fuente física en una colección de fuentes. Esta interfaz se usa para crear caras de fuente a partir de fuentes físicas o para recuperar información como las métricas de la fuente o los nombres de fuente de las fuentes existentes. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Representa una fuente física en una colección de fuentes. |
| [**IDWriteFont2**](idwritefont2.md) | Representa una fuente física en una colección de fuentes. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Representa una fuente de una colección de fuentes. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Objeto que encapsula un conjunto de fuentes, como el conjunto de fuentes instaladas en el sistema o el conjunto de fuentes de un directorio determinado. La API de colección de fuentes se puede usar para detectar qué familias y fuentes de fuentes están disponibles y para obtener algunos metadatos sobre las fuentes. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Objeto que encapsula un conjunto de fuentes, como el conjunto de fuentes instaladas en el sistema o el conjunto de fuentes de un directorio determinado. La API de colección de fuentes se puede usar para detectar qué familias y fuentes de fuentes están disponibles y para obtener algunos metadatos sobre las fuentes. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Esta interfaz encapsula un conjunto de fuentes, como el conjunto de fuentes instaladas en el sistema o el conjunto de fuentes de un directorio determinado. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Esta interfaz encapsula un conjunto de fuentes, como el conjunto de fuentes instaladas en el sistema o el conjunto de fuentes de un directorio determinado. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Se utiliza para construir una colección de fuentes a partir de un tipo de clave determinado.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Interfaz de devolución de llamada definida por la aplicación que recibe notificaciones de la cola de descarga de fuentes (interfaz [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) ). Las devoluciones de llamada se producirán en el subproceso de descarga y los objetos deben estar preparados para controlar llamadas en sus métodos desde otros subprocesos en cualquier momento. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Interfaz que pone en cola las solicitudes de descarga de fuentes, caracteres, glifos y fragmentos de fuentes remotos.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Esta interfaz expone diversos datos de fuentes, como las métricas, los nombres y los contornos del glifo. Contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Esta interfaz contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial. Agrega la capacidad de comprobar si es posible que una ruta de representación de color sea necesaria.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Esta interfaz contiene el tipo de fuente Font, las referencias de archivo apropiadas y los datos de identificación facial. Agrega nuevos recursos, como comparar dos caras de fuente, recuperar los valores del eje de fuentes y recuperar el recurso de fuente subyacente. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Representa una referencia a un tipo de fuente. Una referencia que identifica de forma única a una fuente, desde la que puede crear una fuente para consultar las métricas de fuente y utilizar para la representación. Una referencia de fuente se compone de un archivo de fuente, un índice de la fuente y una simulación de la fuente. Es posible que los datos del archivo no estén físicamente presentes en el equipo local.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Representa una referencia a un tipo de fuente. Una referencia que identifica de forma única a una fuente, desde la que puede crear una fuente para consultar las métricas de fuente y utilizar para la representación. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Permite tener acceso a las fuentes de reserva de la lista fuente. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reversión de fuente a partir de esas asignaciones. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Representa una familia de fuentes relacionadas. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Representa una familia de fuentes relacionadas. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Representa una familia de fuentes relacionadas. **IDWriteFontFamily2** agrega nuevas instalaciones, incluida la recuperación de fuentes por los valores del eje de fuentes. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Representa un archivo de fuente. Las aplicaciones como administradores de fuentes o visores de fuentes pueden llamar a [**IDWriteFontFile:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para averiguar si un archivo determinado es un archivo de fuente y si es un tipo de fuente compatible con el sistema de fuentes. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Encapsula una colección de archivos de fuentes. El sistema de fuentes utiliza esta interfaz para enumerar los archivos de fuentes al compilar una colección de fuentes. |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Controla la carga de los recursos de archivo de fuente de un tipo determinado a partir de una clave de referencia de archivo de fuente en un objeto de flujo de archivo de fuente.  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Carga los datos de archivo de fuente desde un cargador de archivos de fuentes personalizado.  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Representa una lista de fuentes. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Representa una lista de fuentes. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Representa una lista de fuentes. **IDWriteFontList2** agrega nuevas instalaciones, incluida la recuperación del conjunto de fuentes subyacente que usa la lista. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | NN-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Representa un conjunto de fuentes. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Contiene métodos para generar un conjunto de fuentes. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Contiene métodos para generar un conjunto de fuentes. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Contiene métodos para generar un conjunto de fuentes. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Proporciona interoperabilidad con GDI, como los métodos para convertir un tipo de fuente en una estructura LOGFONT, o para convertir una descripción de fuente GDI en un tipo de fuente. También se usa para crear objetos de destino de representación de mapas de bits. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Proporciona interoperabilidad con GDI, como los métodos para convertir un tipo de fuente en una estructura LOGFONT, o para convertir una descripción de fuente GDI en un tipo de fuente. También se usa para crear objetos de destino de representación de mapas de bits. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md) es una **definición** de tipo de la interfaz [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . Consulte la página de referencia de [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) para obtener más información. |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Contiene información de bajo nivel que se usa para representar una ejecución de glifo. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Ajusta un gráfico insertado definido por la aplicación, lo que permite a DWrite consultar las métricas como si el gráfico fuera un glifo insertado con el texto. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Representa un cargador de archivos de fuente que puede tener acceso a las fuentes en memoria. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Implementación integrada de la interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , que funciona en archivos de fuentes locales y expone información del archivo de fuentes local a partir de la clave de referencia del archivo de fuente. Las referencias de archivo de fuentes creadas con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usan este cargador de archivos de fuentes. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Representa una colección de cadenas indizadas por el nombre de la configuración regional. |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | Contiene los dígitos y puntuación numérica adecuados para una configuración regional especificada. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Define las propiedades de ajuste de píxeles, como los píxeles por DIP (píxel independiente del dispositivo) y la matriz de transformación actual de un representador de texto. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Representa un cargador de archivos de fuente que puede tener acceso a fuentes remotas (es decir, descargables).  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Representa una secuencia de archivo de fuente, partes de las cuales puede ser no local.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Representa valores de representación de texto como el nivel ClearType, el contraste mejorado y la corrección gamma para la rasterización y el filtrado de glifos. Normalmente, una aplicación obtiene un objeto de parámetros de representación llamando al método [**IDWriteFactory:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) . |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Representa una colección de cadenas indizadas por número. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | El cliente del analizador de texto implementa esta interfaz para recibir la salida de un análisis de texto determinado.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | La interfaz que se implementa para recibir el resultado de los analizadores de texto. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Lo implementa el cliente del analizador de texto para proporcionar texto al analizador. Permite la separación entre la vista lógica del texto como una secuencia continua de caracteres identificables por posiciones de texto únicas y el diseño de memoria real de bloques de texto potencialmente discretos en la memoria auxiliar del cliente.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | La interfaz que se implementa para proporcionar la información necesaria al analizador de texto, como el texto y las propiedades de texto asociadas. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analiza varias propiedades de texto para el procesamiento de scripts complejos, como la compatibilidad bidireccional (bidi) para idiomas como el árabe, la determinación de las oportunidades de salto de línea, la posición del glifo y la sustitución de números. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analiza varias propiedades de texto para el procesamiento complejo de scripts. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analiza varias propiedades de texto para el procesamiento complejo de scripts. |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | La interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional. |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | La interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) representa un bloque de texto una vez que se ha analizado y formateado por completo. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Representa un bloque de texto una vez que se ha analizado y formateado por completo. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Representa un bloque de texto una vez que se ha analizado y formateado por completo. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Representa un bloque de texto una vez que se ha analizado y formateado por completo.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Representa un conjunto de devoluciones de llamada definidas por la aplicación que realizan la representación de texto, objetos insertados y decoraciones como subrayados. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Representa un conjunto de devoluciones de llamada definidas por la aplicación que realizan la representación de texto, objetos insertados y decoraciones como subrayados.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Representa una configuración de tipografía de fuentes. |
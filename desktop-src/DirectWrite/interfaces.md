---
title: Interfaces de DirectWrite
description: Enumera las interfaces definidas por DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite,interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff423289eb76a3506edb3537875a99a364be457
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588040"
---
# <a name="directwrite-interfaces"></a>Interfaces de DirectWrite

DirectWrite define las interfaces siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Representa el resultado de una operación asincrónica. Un cliente puede usar la interfaz para esperar a que se complete la operación y obtener el resultado.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que puede usar para representar glifos. |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | Encapsula un mapa de bits independiente del dispositivo de 32 bits y el contexto del dispositivo, que se puede usar para representar glifos. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Esta interfaz permite a la aplicación enumerar a través de las ejecuciones de glifo de color. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumerador para una colección ordenada de ejecuciones de glifo de color. |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Se usa para crear todos los objetos de DirectWrite posteriores. Esta interfaz es la interfaz de generador raíz para todos los objetos de DirectWrite. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | Interfaz de generador raíz para todos los [objetos DirectWrite.](direct-write-portal.md) |
| [**IDWriteFactory2**](idwritefactory2.md) | Interfaz de generador raíz para todos los [objetos DirectWrite.](direct-write-portal.md) |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | Interfaz de generador raíz para todos los [objetos DirectWrite.](direct-write-portal.md) |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | Interfaz de generador raíz para todos los objetos DirectWrite. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | Interfaz de generador raíz para todos los objetos DirectWrite. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Representa un objeto de generador a partir del cual se crean todos los objetos de DirectWrite. **IDWriteFactory6 agrega** nuevas características para trabajar con fuentes y recursos de fuente. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Esta interfaz representa un objeto de generador a partir del cual se crean todos los objetos de DirectWrite. **IDWriteFactory7 agrega** nuevas características para trabajar con fuentes del sistema. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Representa una fuente física en una colección de fuentes. Esta interfaz se usa para crear caras de fuente a partir de fuentes físicas o para recuperar información como métricas de caras de fuente o nombres de caras a partir de caras de fuentes existentes. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Representa una fuente física en una colección de fuentes. |
| [**IDWriteFont2**](idwritefont2.md) | Representa una fuente física en una colección de fuentes. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Representa una fuente de una colección de fuentes. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Objeto que encapsula un conjunto de fuentes, como el conjunto de fuentes instalado en el sistema o el conjunto de fuentes de un directorio determinado. La API de colección de fuentes se puede usar para detectar qué familias de fuentes y fuentes están disponibles, y para obtener algunos metadatos sobre las fuentes. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Objeto que encapsula un conjunto de fuentes, como el conjunto de fuentes instalado en el sistema o el conjunto de fuentes de un directorio determinado. La API de colección de fuentes se puede usar para detectar qué familias de fuentes y fuentes están disponibles, y para obtener algunos metadatos sobre las fuentes. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Esta interfaz encapsula un conjunto de fuentes, como el conjunto de fuentes instalado en el sistema o el conjunto de fuentes de un directorio determinado. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Esta interfaz encapsula un conjunto de fuentes, como el conjunto de fuentes instalado en el sistema o el conjunto de fuentes de un directorio determinado. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Se usa para construir una colección de fuentes dado un tipo determinado de clave.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Interfaz de devolución de llamada definida por la aplicación que recibe notificaciones de la cola de descarga de fuentes [**(interfaz IDWriteFontDownloadQueue).**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) Las devoluciones de llamada se producirán en el subproceso de descarga y los objetos deben estar preparados para controlar las llamadas en sus métodos desde otros subprocesos en cualquier momento. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Interfaz que coloca en cola las solicitudes de descarga de fuentes remotas, caracteres, glifos y fragmentos de fuente.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Esta interfaz expone varios datos de fuente, como métricas, nombres y contornos de glifo. Contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Esta interfaz contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial. Agrega la capacidad de comprobar si una ruta de representación de color es potencialmente necesaria.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Esta interfaz contiene el tipo de cara de fuente, las referencias de archivo adecuadas y los datos de identificación facial. Agrega nuevas características, como la comparación de dos caras de fuente, la recuperación de valores del eje de fuente y la recuperación del recurso de fuente subyacente. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Representa una referencia a una cara de fuente. Referencia que identifica de forma única una fuente, a partir de la cual puede crear una cara de fuente para consultar las métricas de fuente y usarla para la representación. Una referencia de la cara de fuente consta de un archivo de fuente, un índice de la cara de fuente y una simulación de cara de fuente. Los datos de archivo pueden o no estar físicamente presentes en la máquina local todavía.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Representa una referencia a una cara de fuente. Referencia que identifica de forma única una fuente, a partir de la cual puede crear una cara de fuente para consultar las métricas de fuente y usarla para la representación. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Permite acceder a fuentes de reserva desde la lista de fuentes. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reserva de fuente a partir de esas asignaciones. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Representa una familia de fuentes relacionadas. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Representa una familia de fuentes relacionadas. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Representa una familia de fuentes relacionadas. **IDWriteFontFamily2** agrega nuevas características, incluida la recuperación de fuentes por valores de eje de fuente. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Representa un archivo de fuente. Las aplicaciones como los administradores de fuentes o los visores de fuentes pueden llamar a [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para averiguar si un archivo determinado es un archivo de fuente y si es un tipo de fuente compatible con el sistema de fuentes. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Encapsula una colección de archivos de fuente. El sistema de fuentes usa esta interfaz para enumerar los archivos de fuente al compilar una colección de fuentes. |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Controla la carga de recursos de archivo de fuente de un tipo determinado desde una clave de referencia de archivo de fuente en un objeto de flujo de archivo de fuente.  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Carga los datos del archivo de fuente desde un cargador de archivos de fuente personalizado.  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Representa una lista de fuentes. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Representa una lista de fuentes. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Representa una lista de fuentes. **IDWriteFontList2** agrega nuevas instalaciones, incluida la recuperación del conjunto de fuentes subyacente usado por la lista. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Representa un conjunto de fuentes. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Representa un conjunto de fuentes. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Contiene métodos para crear un conjunto de fuentes. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Contiene métodos para crear un conjunto de fuentes. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Contiene métodos para crear un conjunto de fuentes. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Proporciona interoperabilidad con GDI, como métodos para convertir una cara de fuente en una estructura LOGFONT o para convertir una descripción de fuente GDI en una cara de fuente. También se usa para crear objetos de destino de representación de mapa de bits. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Proporciona interoperabilidad con GDI, como métodos para convertir una cara de fuente en una estructura LOGFONT o para convertir una descripción de fuente GDI en una cara de fuente. También se usa para crear objetos de destino de representación de mapa de bits. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink es**](idwritegeometrysink.md) una **definición de tipo** de la interfaz [**ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) Consulte la página [**de referencia ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) para obtener más información. |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Contiene información de bajo nivel que se usa para representar una ejecución de glifo. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Encapsula un gráfico en línea definido por la aplicación, lo que permite a DWrite consultar métricas como si el gráfico fuera un glifo en línea con el texto. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Representa un cargador de archivos de fuentes que puede acceder a fuentes en memoria. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Una implementación integrada de la interfaz [**IDWriteFontFileLoader,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) que funciona en archivos de fuentes locales y expone información del archivo de fuente local de la clave de referencia del archivo de fuente. Las referencias de archivo de fuente [**creadas con CreateFontFileReference usan**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) este cargador de archivos de fuente. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Representa una colección de cadenas indizadas por nombre de configuración regional. |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | Contiene los dígitos adecuados y la puntuación numérica para una configuración regional especificada. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Define las propiedades de ajuste de píxeles, como píxeles por DIP (píxel independiente del dispositivo) y la matriz de transformación actual de un representador de texto. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Representa un cargador de archivos de fuentes que puede acceder a fuentes remotas (es decir, descargables).  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Representa un flujo de archivo de fuente, partes de las cuales pueden no ser locales.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Representa la configuración de representación de texto, como el nivel ClearType, el contraste mejorado y la corrección gamma para la rasterización y el filtrado de glifos. Normalmente, una aplicación obtiene un objeto de parámetros de representación llamando al [**método IDWriteFactory::CreateMonitorRenderingParams.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Representa la configuración de representación de texto para la rasterización y el filtrado de glifos. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Representa una colección de cadenas indizadas por número. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | El cliente del analizador de texto implementa esta interfaz para recibir la salida de un análisis de texto determinado.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Interfaz que implementa para recibir la salida de los analizadores de texto. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Implementado por el cliente del analizador de texto para proporcionar texto al analizador. Permite la separación entre la vista lógica del texto como una secuencia continua de caracteres identificable por posiciones de texto únicas y el diseño de memoria real de bloques de texto potencialmente discretos en el almacén de respaldo del cliente.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | Interfaz que implementa para proporcionar la información necesaria al analizador de texto, como el texto y las propiedades de texto asociadas. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analiza varias propiedades de texto para el procesamiento complejo de scripts, como la compatibilidad bidireccional (bidi) con idiomas como el árabe, la determinación de oportunidades de salto de línea, la colocación de glifos y la sustitución de números. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analiza varias propiedades de texto para el procesamiento de scripts complejos. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analiza varias propiedades de texto para el procesamiento de scripts complejos. |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | La [**interfaz IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) describe las propiedades de fuente y párrafo usadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional. |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | La [**interfaz IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) representa un bloque de texto después de que se haya analizado y dado formato por completo. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Representa un bloque de texto después de que se haya analizado y dado formato por completo. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Representa un bloque de texto después de que se haya analizado y dado formato por completo. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Representa un bloque de texto después de que se haya analizado y dado formato por completo.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Representa un conjunto de devoluciones de llamada definidas por la aplicación que realizan la representación de texto, objetos en línea y decoración como subrayados. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Representa un conjunto de devoluciones de llamada definidas por la aplicación que realizan la representación de texto, objetos en línea y decoración como subrayados.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Representa una configuración de tipografía de fuente. |
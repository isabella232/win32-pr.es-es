---
description: En este tema se presenta el lenguaje de consulta de metadatos para Windows Imaging Component (WIC).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Información general del lenguaje de consulta de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b55bdc7079565f98411e28977d3d8c41e191f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554815"
---
# <a name="metadata-query-language-overview"></a>Información general del lenguaje de consulta de metadatos

En este tema se presenta el lenguaje de consulta de metadatos para Windows Imaging Component (WIC). El lenguaje de consulta de metadatos se usa para crear expresiones que busquen datos específicos (elementos de metadatos) y ubicaciones (bloques de metadatos) dentro de los metadatos de una imagen.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Anatomía de una expresión de ruta de acceso](#anatomy-of-a-path-expression)
    -   [Selección de bloques](#block-selection)
    -   [Selección de elementos](#item-selection)
    -   [Carácter de escape](#escape-character)
    -   [Ejemplos de expresiones](#sample-expressions)
-   [Expresiones de la Directiva de metadatos de fotos](#photo-metadata-policy-expressions)
-   [Resumen del lenguaje de consulta de metadatos](#metadata-query-language-summary)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con el sistema de metadatos de WIC tal y como se describe en [información general sobre metadatos de WIC](-wic-about-metadata.md) y acceso a los metadatos, como se describe en [información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).

## <a name="introduction"></a>Introducción

Interactúe con la plataforma de metadatos principalmente a través de dos componentes del modelo de objetos componentes (COM): un lector de consultas, representado por la interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) y un escritor de consultas, representado por la interfaz [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Estos componentes permiten leer o escribir metadatos mediante el lenguaje de consulta de metadatos. El lenguaje de consulta describe la sintaxis de una expresión de ruta de acceso y los componentes de la consulta usan esta expresión de ruta de acceso para acceder a los metadatos deseados. Esta expresión de ruta de acceso describe la ubicación de un bloque o elemento de metadatos.

Un bloque de metadatos es un grupo con nombre de metadatos en un formato específico. Un bloque de metadatos puede contener elementos de metadatos individuales, como un autor o una hora de creación y bloques de metadatos adicionales. El nombre de un bloque de metadatos se determina por su formato. Por ejemplo, un bloque de metadatos que contiene los metadatos de app1 se denominará "app1". Los formatos de metadatos comunes incluyen app1, EXIF, IFD y XMP.

Un elemento de metadatos es un par nombre-valor que describe características como autor, título y clasificación.

Una expresión de ruta de acceso contiene uno o varios nombres de bloques de metadatos. También puede especificar un elemento de metadatos dentro de un bloque de metadatos. La siguiente expresión de ruta de acceso representa un bloque app1 que contiene un bloque IFD que contiene el elemento de metadatos:

-   /app1/IFD/{ushort = 18249}

En el diagrama siguiente se muestra la composición de una imagen JPEG de ejemplo con cuatro bloques de metadatos raíz: App0, app1, XMP y un bloque desconocido. Cada elemento resaltado anota el tipo de metadatos (bloque o elemento) y la expresión de consulta utilizada para recuperar los datos.

![imagen JPEG con llamadas de metadatos](graphics/jpegwithcallouts.png)

> [!Note]  
> El contenido de este diagrama se hace referencia en este documento y se usa en muchos de los ejemplos.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomía de una expresión de ruta de acceso

Para tener acceso a los metadatos mediante las API de WIC, en la mayoría de los casos se debe usar una expresión de consulta completa. En este tema se describen las expresiones completas para tener acceso a los metadatos. Si necesita información sobre los casos en los que se usan expresiones no completas, consulte la sección expresión de la Directiva de metadatos de fotos más adelante en este documento.

¿Qué es una expresión de consulta completa? En WIC, una expresión completa es una cadena que comienza con la barra diagonal de caracteres de ruta de acceso (/), seguida de una ruta de navegación a un bloque de metadatos o a un elemento de metadatos específico. Cada paso dentro de la ruta de navegación está separado por una barra diagonal, formando una expresión para tener acceso a un bloque de metadatos o a un elemento de metadatos. Por ejemplo, la siguiente es una expresión de consulta completa que tiene acceso a la clasificación de fotos de Microsoft en un bloque de IFD que está anidado en un bloque app1:

-   /app1/IFD/{ushort = 18249}

Cuando WIC analiza esta expresión, busca primero el bloque de metadatos de app1 dentro de los metadatos de la imagen. Si se encuentra el bloque app1, continúa buscando el bloque de metadatos IFD anidado. Si se encuentra el bloque IFD, busca el elemento de metadatos específico, en este caso, la clasificación MicrosoftPhoto en la etiqueta 18249, dentro del bloque de metadatos de IFD. Si en algún momento WIC no encuentra un elemento o bloque de metadatos, anula la consulta.

### <a name="block-selection"></a>Selección de bloques

La expresión de consulta de metadatos de WIC más sencilla es una expresión para obtener un lector/escritor de consultas para un bloque de metadatos específico. Obtener un lector/escritor de consultas permite dirigir las consultas posteriores directamente a un bloque de metadatos anidado sin tratar con su bloque primario. Una expresión de consulta de selección de bloques es una ruta de navegación al bloque de metadatos deseado. Por ejemplo, en la ilustración anterior hay cinco bloques de metadatos, dos de los cuales están anidados en otros bloques de metadatos. A continuación se muestran las expresiones de ruta de acceso a cada bloque de metadatos del ejemplo JPEG:

-   /app0
-   /app1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Cuando se usa un lector/escritor de consultas para ejecutar una consulta, devuelve un nuevo lector/escritor de consultas que da servicio a las consultas dentro del ámbito del bloque de metadatos especificado. Por ejemplo, si ejecuta la consulta "/app1", se obtiene un nuevo lector de consultas y las consultas al nuevo lector son relativas al bloque app1. Esto significa que la consulta "/IFD" es válida para el nuevo lector porque el bloque app1 contiene un bloque IFD. Sin embargo, "/XMP" no funcionaría porque este bloque app1 no contiene un bloque de metadatos XMP.

El lenguaje de consulta también admite una notación de índice. La notación de índice proporciona acceso a un bloque de metadatos específico cuando existen varios bloques del mismo tipo. En el ejemplo JPEG, se puede usar la siguiente expresión de ruta de acceso indizada:

-   /\[0 \] app1/ \[ 0 \] IFD

En el lenguaje de consulta, todos los índices comienzan en cero. En la expresión anterior, las primeras cero consultas del primer bloque app1 y el segundo cero consultan el primer bloque IFD anidado. Aún se puede usar la notación de índice aunque no existan varios bloques del mismo tipo. Si el ejemplo JPEG incluía un segundo bloque app1 con un bloque IFD incrustado, se utilizaría la expresión "/ \[ 1 \] app1/IFD" para tener acceso al segundo bloque app1.

La notación de índice es más común cuando se trabaja con fragmentos de texto PNG, ya que es probable que la imagen PNG tenga más de un fragmento de texto.

> [!Note]  
> No se admiten índices de matriz multidimensionales.

 

### <a name="item-selection"></a>Selección de elementos

Puede acceder a los elementos de metadatos en un bloque de metadatos mediante la generación de expresiones de selección de bloques. Considere las propiedades XMP y Microsoft Photo rating en el ejemplo JPEG. Estos metadatos existen en dos bloques de metadatos: los bloques app1/IFD y XMP. Por lo tanto, se puede utilizar más de una expresión para tener acceso a los mismos datos. La siguiente expresión tiene acceso a la clasificación MicrosoftPhoto en el bloque XMP:

-   /XMP/XMP: clasificación

La parte "XMP:" de la expresión es un identificador descriptivo del esquema. XMP es un estándar extensible que permite a las entidades de terceros publicar sus propios esquemas, que definen cómo almacenar determinados elementos de metadatos. Un esquema XMP se identifica por completo mediante una dirección URL, pero WIC proporciona un conjunto de identificadores descriptivos para los esquemas conocidos. Para obtener más información, vea el tema [consultas de metadatos de formato de imagen nativa](-wic-native-image-format-metadata-queries.md) .

En el caso de las imágenes JPEG, la información de clasificación también puede almacenarse en el bloque IFD anidado de app1. Sin embargo, a diferencia del ejemplo de clasificación XMP, el bloque IFD no usa un nombre de esquema para tener acceso a la información de clasificación. En su lugar, se usa una expresión de datos. La siguiente expresión se usa para acceder a la clasificación MicrosoftPhoto en el bloque IFD anidado de app1:

-   /app1/IFD/{ushort = 18249}

En esta expresión, la parte "/app1/IFD" de la expresión es la ruta de navegación al bloque IFD (como se explicó anteriormente en la sección selección de bloques). La segunda parte de la expresión "/{ushort = 18249}" tiene acceso a los datos. Esta parte de la expresión indica al analizador de consultas que busque los datos incrustados en la etiqueta corta sin signo que tiene el identificador de etiqueta 18249.

> [!Note]  
> Para obtener una lista de formatos de metadatos comunes admitidos por cada formato de imagen en, vea el tema [consultas de metadatos de formato de imagen nativa](-wic-native-image-format-metadata-queries.md) .

 

{Ushort = 18249} es una expresión de datos y puede adoptar varias formas. Una expresión de datos es una expresión de dos partes que contiene la etiqueta o la clave de metadatos solicitada, en este caso "18249", y el tipo de datos de la clave, en este caso "ushort". Las dos partes se separan con un signo igual (=). WICsupports la mayoría de los tipos de datos comunes de C/C++. El lenguaje de consulta acepta los siguientes tipos de datos:

-   char
-   uchar
-   short
-   ushort
-   long
-   ulong
-   int
-   uint
-   longlong
-   FLOAT
-   double
-   str
-   wstr
-   guid
-   bool

> [!Note]  
> En esta lista solo se especifican los tipos de datos admitidos por el lenguaje de consulta de metadatos. Use estos tipos de datos al crear una expresión de datos de consulta de metadatos, como {ushort = 18249}. WIC devuelve el valor del elemento de metadatos en forma de PROPVARIANT, que define su propio sistema de tipos.

 

"18249" en el ejemplo es la etiqueta de datos. Microsoft define este número concreto para que contenga la clasificación MicrosoftPhoto. La etiqueta de datos puede ser cualquier número, cadena o GUID según el elemento de datos que esté buscando.

A diferencia del ejemplo de clasificación XMP, no hay ningún conflicto de nombres para el valor de clasificación en el bloque app1/IFD. Esto se debe a que el valor de clasificación XMP se almacena realmente en una etiqueta ushort diferente, 18246. Por lo tanto, la expresión para tener acceso a la clasificación XMP en el bloque app1/IFD es:

-   /app1/IFD/{ushort = 18246}

> [!Note]  
> Para obtener una descripción formal del lenguaje de consulta de metadatos, vea la sección Resumen del lenguaje de consulta de metadatos más adelante en este documento.

 

### <a name="escape-character"></a>Carácter de escape

El lenguaje de consulta no distingue entre mayúsculas y minúsculas y trata todos los caracteres en minúsculas. Sin embargo, algunos formatos de metadatos (como XMP) distinguen mayúsculas de minúsculas. Cuando trabaje con un formato de metadatos que distinga entre mayúsculas y minúsculas, utilice el carácter de barra diagonal inversa ( \\ ) Si desea especificar un carácter en mayúsculas.

El analizador de lenguaje usa el carácter de escape y el siguiente carácter se interpreta directamente. Por ejemplo, la expresión {char = \\ \\ } se resuelve como ' \\ ' y {char = \\ C} se resuelve como una C en mayúsculas. Sin el carácter de escape, {Char = \\ } sería una expresión no válida y {char = C} se interpretaría como C minúscula. Asegúrese de usar el carácter de escape de barra diagonal inversa delante de todas las letras mayúsculas en formatos de metadatos que distinguen mayúsculas de minúsculas.

### <a name="sample-expressions"></a>Ejemplos de expresiones

En la tabla siguiente se proporcionan algunas expresiones de ejemplo y descripciones de sus interpretaciones por parte del analizador del lenguaje de consulta. 

| Expression                     | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IFD/XMP/Exif: autor            | Corresponde a la siguiente ruta de navegación: IFD Block-> XMP Block-> la propiedad "author" del esquema "EXIF".                                                                                                                                                                                                                                            |
| /\[1 \] IFD/ \[ 0 \] XMP/Exif: autor | Igual que el primer elemento de esta tabla, salvo que el \[ \# \] prefijo describe el elemento al que se debe navegar en caso de que se produzca un conflicto de nombres.                                                                                                                                                                                                                                |
| /IFD/{ushort = 700}/Author       | Igual que el primer elemento de esta tabla, salvo que usa una expresión de datos para hacer referencia al bloque XMP en lugar del nombre de bloque "XMP" (el bloque XMP se inserta en el identificador de etiqueta corto sin signo 700). Además, la propiedad "author" no especifica un esquema. El analizador de consultas intentará hacer coincidir la propiedad en todos los esquemas y devolverá la primera coincidencia. |
| /ifd/xmp                       | Proporciona una ruta de navegación a un bloque de metadatos. Si se encuentra el bloque, se devuelve un nuevo lector/escritor de metadatos.                                                                                                                                                                                                                                                 |
| /\[\*\]Texto/palabra clave            | Obtiene o establece la propiedad de palabra clave para un fragmento PNG. Dado que la especificación de metadatos PNG permite varios fragmentos de un tipo determinado, la \[ \* \] notación obtiene o establece el fragmento PNG de datos con la propiedad adecuada. Según la especificación PNG, dos fragmentos no pueden tener las mismas propiedades.                                                                |



 

Cada bloque de metadatos también se identifica de forma única mediante el GUID de metadatos que se puede utilizar en lugar del nombre descriptivo del bloque. Se puede usar la sintaxis siguiente en lugar de proporcionar nombres de bloque: "/{GUID = GUID}/ \[ n \] {GUID = GUID}/Schema: tagidentifier"

En la tabla siguiente se proporcionan algunos ejemplos no válidos y los motivos por los que se rechazarán. 

| Expresión no válida         | Descripción de rechazo                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /IFD/ \[ 0 \] \[ 2 \] EXIF/       | Rechazado porque no se admiten índices de matriz multidimensionales.                                                                                                    |
| /IFD/{ushort = 1}/{ushort = 2} | Rechazado a menos que el IFD tenga un tagID = 1 que sea un controlador de metadatos que contenga un elemento de metadatos con tagID = 2.                                                        |
| /{ushort = 1}                | Se rechaza si el procesamiento de la consulta es relativo a un nivel superior de la jerarquía de metadatos. Esto se debe a que el nivel superior solo contiene bloques de metadatos y no elementos de datos. |



 

## <a name="photo-metadata-policy-expressions"></a>Expresiones de la Directiva de metadatos de fotos

Como se indicó anteriormente, una expresión de consulta completa se inicia con una barra diagonal (/). Las expresiones que no comienzan con la barra diagonal se evalúan como expresiones de directiva. Una expresión de directiva le permite consultar los metadatos de la fotografía para [las propiedades del shell](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)de Windows relacionadas con la imagen. En la sección de selección de datos anteriormente en este documento, se usó la expresión "/XMP/XMP: rating" para tener acceso a la propiedad de clasificación XMP. Esta propiedad también se puede consultar mediante la siguiente expresión de directiva:

-   System. SimpleRating

Para tener acceso a la propiedad rating del esquema MicrosoftPhoto, se puede usar la siguiente expresión de consulta:

-   System. Rating

Las expresiones de directiva de metadatos de fotos se comportan de manera diferente a las consultas de metadatos completas de algunas maneras importantes.

En primer lugar, al tener acceso a los metadatos mediante una expresión de Directiva, WIC realiza el arbitraje y la resolución de conflictos en caso de que la misma propiedad esté disponible en varios bloques de metadatos. Por ejemplo, los valores de clasificación MicrosoftPhoto y XMP se almacenan en el bloque app1/IFD y en el bloque XMP. La Directiva de metadatos de fotos determina la prioridad para la que se devuelve el valor de bloque al leer los metadatos. Cuando se escriben metadatos, la Directiva de metadatos de fotos garantiza que las mismas propiedades en diferentes bloques sean coherentes. Si usa una consulta de metadatos como "/XMP/XMP: rating", es responsabilidad suya arbitrar entre las distintas ubicaciones de los metadatos.

> [!Note]  
> Para obtener una lista de las expresiones de directiva admitidas y sus directivas de asignación, consulte el tema sobre las [directivas de metadatos de fotos](photo-metadata-policies.md) .

 

En segundo lugar, las expresiones de directiva de metadatos de fotos son independientes del formato de imagen, mientras que las consultas de metadatos completas no lo son. Por ejemplo, la consulta "/XMP/XMP: rating" es específica del formato JPEG. Las imágenes TIFF también admiten metadatos XMP, pero se almacenan de forma diferente en comparación con JPEG, por lo que la consulta TIFF sería "/IFD/XMP/XMP: rating". Sin embargo, en ambos casos la expresión de directiva sería "System. SimpleRating".

Las expresiones de las directivas de metadatos de fotos proporcionan un nivel más alto de abstracción y simplicidad cuando se comparan con las consultas de metadatos completas, por lo que es preferible en los casos en los que no se necesita acceso a los metadatos de bajo nivel. Sin embargo, las expresiones de directiva solo proporcionan acceso a un conjunto limitado de metadatos de imagen, mientras que el lenguaje de consulta de metadatos proporciona acceso a casi todos los metadatos almacenados en un archivo de imagen.

## <a name="metadata-query-language-summary"></a>Resumen del lenguaje de consulta de metadatos

La tabla siguiente es una definición formal del lenguaje de consulta de metadatos de WIC. Cada símbolo de gramática representa una expresión formada por otros símbolos. La expresión puede ser otro símbolo o una secuencia de otros símbolos separados por la barra vertical ( \| ), lo que indica una opción "or". Toda la expresión de la derecha es una sustitución posible para el símbolo especificado de la izquierda. 

| Símbolo                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | ' < ' \<name> ' > '                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | ' char ' \| ' uchar ' \| ' Short ' \| ' ushort ' \| ' Long ' ' \| ULong ' \| ' int ' \| ' uint ' \| ' LongLong ' ' \| ulonglong ' \| ' Float ' \| ' Double ' \| ' str ' \| ' wstr ' \| ' GUID ' \| ' bool ' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | number                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre la extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 




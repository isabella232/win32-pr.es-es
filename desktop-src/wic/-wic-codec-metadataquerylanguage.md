---
description: En este tema se presenta el lenguaje de consulta de metadatos Windows Imaging Component (WIC).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Información general sobre el lenguaje de consulta de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e141c543cae90ff99d8c0509a0f5802dba1139
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885217"
---
# <a name="metadata-query-language-overview"></a>Información general sobre el lenguaje de consulta de metadatos

En este tema se presenta el lenguaje de consulta de metadatos Windows Imaging Component (WIC). El lenguaje de consulta de metadatos se usa para crear expresiones que encuentran datos específicos (elementos de metadatos) y ubicaciones (bloques de metadatos) dentro de los metadatos de una imagen.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Anatomía de una expresión de ruta de acceso](#anatomy-of-a-path-expression)
    -   [Selección de bloques](#block-selection)
    -   [Selección de elementos](#item-selection)
    -   [Carácter de escape](#escape-character)
    -   [Ejemplos de expresiones](#sample-expressions)
-   [Expresiones de directiva de metadatos de fotos](#photo-metadata-policy-expressions)
-   [Resumen del lenguaje de consulta de metadatos](#metadata-query-language-summary)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

Para comprender este tema, debe estar familiarizado con el sistema de metadatos de WIC tal y como se describe en Información general sobre metadatos de [WIC](-wic-about-metadata.md) y acceso a los metadatos, como se describe en Información general sobre la lectura y escritura de metadatos de [imagen.](-wic-codec-readingwritingmetadata.md)

## <a name="introduction"></a>Introducción

Interactúa con la plataforma de metadatos principalmente a través de dos componentes del Modelo de objetos componentes (COM): un lector de consultas, representado por la interfaz [**IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) y un escritor de consultas, representado por la interfaz [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Estos componentes permiten leer o escribir metadatos mediante el lenguaje de consulta de metadatos. El lenguaje de consulta describe la sintaxis de una expresión de ruta de acceso y los componentes de consulta usan esta expresión de ruta de acceso para acceder a los metadatos deseados. Esta expresión de ruta de acceso describe la ubicación de un bloque o elemento de metadatos.

Un bloque de metadatos es un grupo con nombre de metadatos en un formato específico. Un bloque de metadatos puede contener elementos de metadatos individuales, como un autor o tiempo de creación, y bloques de metadatos adicionales. El nombre de un bloque de metadatos viene determinado por su formato. Por ejemplo, un bloque de metadatos que contiene metadatos de App1 se denominaría "app1". Los formatos de metadatos comunes incluyen App1, Exif, IFD y XMP.

Un elemento de metadatos es un par nombre-valor que describe características como autor, título y clasificación.

Una expresión de ruta de acceso contiene uno o varios nombres de bloque de metadatos. También puede especificar un elemento de metadatos dentro de un bloque de metadatos. La siguiente expresión de ruta de acceso representa un bloque App1 que contiene un bloque IFD que contiene el elemento de metadatos:

-   /app1/ifd/{ushort=18249}

En el diagrama siguiente se muestra la composición de una imagen JPEG de ejemplo con cuatro bloques de metadatos raíz: App0, App1, XMP y un bloque desconocido. Cada elemento resaltado anota el tipo de metadatos (bloque o elemento) y la expresión de consulta utilizada para recuperar los datos.

![imagen jpeg con llamadas de metadatos](graphics/jpegwithcallouts.png)

> [!Note]  
> En este documento se hace referencia al contenido de este diagrama y se usa en muchos de los ejemplos.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomía de una expresión de ruta de acceso

Para acceder a los metadatos mediante las API de WIC, se debe usar una expresión de consulta completa en la mayoría de los casos. En este tema se de abordan expresiones completa para acceder a los metadatos. Si necesita información sobre los casos en los que se usan expresiones no completa, consulte la sección Expresión de directiva de metadatos de fotos más adelante en este documento.

¿Qué es una expresión de consulta completa? En WIC, una expresión completa es una cadena que comienza con la barra diagonal de caracteres de ruta de acceso (/), seguida de una ruta de navegación a un bloque de metadatos o a un elemento de metadatos específico. Cada paso dentro de la ruta de navegación está separado por una barra diagonal, formando una expresión para tener acceso a un bloque de metadatos o un elemento de metadatos. Por ejemplo, la siguiente es una expresión de consulta completa que accede a la clasificación de fotos de Microsoft en un bloque IFD anidado en un bloque App1:

-   /app1/ifd/{ushort=18249}

Cuando WIC analiza esta expresión, primero busca el bloque de metadatos App1 dentro de los metadatos de la imagen. Si se encuentra el bloque App1, continúa su búsqueda en busca del bloque de metadatos IFD anidado. Si se encuentra el bloque IFD, busca el elemento de metadatos específico, en este caso la clasificación MicrosoftPhoto bajo la etiqueta 18249, dentro del bloque de metadatos IFD. Si en cualquier momento WIC no encuentra un elemento o un bloque de metadatos, anula la consulta.

### <a name="block-selection"></a>Selección de bloques

La expresión de consulta de metadatos de WIC más sencilla es una expresión para obtener un lector o escritor de consultas para un bloque de metadatos específico. La obtención de un lector o escritor de consultas permite dirigir las consultas posteriores directamente a un bloque de metadatos anidado sin tratar con su bloque primario. Una expresión de consulta de selección de bloque es una ruta de navegación al bloque de metadatos deseado. Por ejemplo, en la ilustración anterior hay cinco bloques de metadatos, dos de los cuales están anidados en otros bloques de metadatos. Estas son las expresiones de ruta de acceso a cada bloque de metadatos del ejemplo JPEG:

-   /app0
-   /app1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Cuando se usa un lector o escritor de consultas para ejecutar una consulta, devuelve un nuevo lector o escritor de consultas que proporciona servicios a las consultas dentro del ámbito del bloque de metadatos especificado. Por ejemplo, si ejecuta la consulta "/app1", se obtiene un nuevo lector de consultas y las consultas al nuevo lector son relativas al bloque App1. Esto significa que la consulta "/ifd" es válida para el nuevo lector porque el bloque App1 contiene un bloque IFD. Sin embargo, "/xmp" no funcionaría porque este bloque App1 no contiene un bloque de metadatos XMP.

El lenguaje de consulta también admite una notación de índice. La notación de índice proporciona acceso a un bloque de metadatos específico cuando existen varios bloques del mismo tipo. En el ejemplo JPEG, se puede usar la siguiente expresión de ruta de acceso indexada:

-   /\[0 \] app1/ \[ 0 \] ifd

En el lenguaje de consulta, todos los índices comienzan en cero. En la expresión anterior, el primer cero consulta el primer bloque App1 y el segundo cero consulta el primer bloque IFD anidado. La notación de índice todavía se puede usar incluso cuando no existen varios bloques del mismo tipo. Si el JPEG de ejemplo incluye un segundo bloque App1 con un bloque IFD incrustado, se usaría la expresión "/ \[ 1 app1/ifd" para acceder al segundo \] bloque App1.

La notación de índice es más común cuando se trabaja con fragmentos png de tEXt porque es probable que la imagen PNG tenga más de un fragmento de tEXt.

> [!Note]  
> No se admiten índices de matriz multidimensional.

 

### <a name="item-selection"></a>Selección de elementos

Puede acceder a los elementos de metadatos de un bloque de metadatos mediante la creación de expresiones de selección de bloques. Considere las propiedades de clasificación XMP y Microsoft Photo en el ejemplo JPEG. Estos metadatos existen en dos bloques de metadatos: los bloques App1/IFD y XMP. Por lo tanto, se puede usar más de una expresión para acceder a los mismos datos. La expresión siguiente tiene acceso a la clasificación MicrosoftPhoto en el bloque XMP:

-   /xmp/xmp:Rating

La parte "xmp:" de la expresión es un identificador descriptivo del esquema. XMP es un estándar extensible y permite a las entidades de terceros publicar sus propios esquemas que definen cómo almacenar determinados elementos de metadatos. Un esquema XMP se identifica completamente mediante una dirección URL, pero WIC proporciona un conjunto de identificadores descriptivos para esquemas conocidos. Para obtener más información, vea el tema Consultas de [metadatos de formato de imagen](-wic-native-image-format-metadata-queries.md) nativa.

En el caso de las imágenes JPEG, la información de clasificación también se puede almacenar dentro del bloque IFD anidado app1. Sin embargo, a diferencia del ejemplo de clasificación XMP, el bloque IFD no usa un nombre de esquema para acceder a la información de clasificación. En su lugar, se usa una expresión de datos. La siguiente expresión se usa para acceder a la clasificación MicrosoftPhoto en el bloque IFD anidado app1:

-   /app1/ifd/{ushort=18249}

En esta expresión, la parte "/app1/ifd" de la expresión es la ruta de navegación al bloque IFD (como se explicó anteriormente en la sección Selección de bloques). La segunda parte de la expresión "/{ushort=18249}" tiene acceso a los datos. Esta parte de la expresión indica al analizador de consultas que busque los datos insertados en la etiqueta corta sin signo que tiene el identificador de etiqueta 18249.

> [!Note]  
> Para obtener una lista de los formatos de metadatos comunes admitidos por cada formato de imagen en , vea el tema Consultas de metadatos de formato [de imagen](-wic-native-image-format-metadata-queries.md) nativa.

 

{ushort=18249} es una expresión de datos y puede tener varias formas. Una expresión de datos es una expresión de dos partes que contiene la etiqueta o clave de metadatos solicitada, en este caso "18249", y el tipo de datos de la clave, en este caso "ushort". Las dos partes están separadas por un signo igual (=). WIC admite la mayoría de los tipos de datos comunes de C/C++. El lenguaje de consulta acepta los siguientes tipos de datos:

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
> Esta lista solo especifica los tipos de datos admitidos por el lenguaje de consulta de metadatos. Use estos tipos de datos al crear una expresión de datos de consulta de metadatos como {ushort=18249}. WiC devuelve el valor del elemento de metadatos en forma de PROPVARIANT, que define su propio sistema de tipos.

 

El "18249" del ejemplo es la etiqueta de datos. Microsoft define este número concreto para que contenga la clasificación MicrosoftPhoto. La etiqueta de datos puede ser cualquier número, cadena o GUID en función del elemento de datos que esté buscando.

A diferencia del ejemplo de clasificación XMP, no hay ninguna colisión de nombres para el valor de clasificación en el bloque App1/IFD. Esto se debe a que el valor de clasificación XMP se almacena realmente en una etiqueta ushort diferente, 18246. Por lo tanto, la expresión para acceder a la clasificación XMP en el bloque App1/IFD es:

-   /app1/ifd/{ushort=18246}

> [!Note]  
> Para obtener una descripción formal del lenguaje de consulta de metadatos, vea la sección Resumen del lenguaje de consulta de metadatos más adelante en este documento.

 

### <a name="escape-character"></a>Carácter de escape

El lenguaje de consulta no distingue mayúsculas de minúsculas y trata todos los caracteres en minúsculas. Sin embargo, algunos formatos de metadatos (como XMP) distinguen mayúsculas de minúsculas. Cuando trabaje con un formato de metadatos que distingue mayúsculas de minúsculas, use el carácter de barra diagonal inversa ( ) cuando desee especificar \\ un carácter en mayúsculas.

El analizador de idioma consume el carácter de escape y el siguiente carácter que lo sigue se interpreta directamente. Por ejemplo, la expresión {char= } se resuelve como ' ' y \\ \\ \\ {char= C} se resuelve \\ como una C mayúscula. Sin el carácter de escape, {char= } sería una expresión no válida y {char=C} se interpretaría como una c \\ minúscula. Asegúrese de usar el carácter de escape de barra diagonal inversa antes de todas las letras mayúsculas en formatos de metadatos que distinguen mayúsculas de minúsculas.

### <a name="sample-expressions"></a>Ejemplos de expresiones

En la tabla siguiente se proporcionan algunas expresiones de ejemplo y descripciones de sus interpretaciones por parte del analizador del lenguaje de consulta. 

| Expression                     | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ifd/xmp/exif:Author            | Corresponde a la siguiente ruta de navegación: bloque IFD -> bloque XMP -> propiedad "Author" en el esquema "Exif".                                                                                                                                                                                                                                            |
| /\[1 \] \[ ifd/0 \] xmp/exif:Author | Igual que el primer elemento de esta tabla, salvo que el prefijo describe qué elemento navegar en caso de colisión \[ \# \] de nombres.                                                                                                                                                                                                                                |
| /ifd/{ushort=700}/Author       | Igual que el primer elemento de esta tabla, salvo que usa una expresión de datos para hacer referencia al bloque XMP en lugar del nombre de bloque "xmp" (el bloque XMP está incrustado bajo el identificador de etiqueta corta sin signo 700). Además, la propiedad "Author" no especifica un esquema. El analizador de consultas intentará hacer coincidir la propiedad en todos los esquemas y devolverá la primera coincidencia. |
| /ifd/xmp                       | Proporciona una ruta de navegación a un bloque de metadatos. Si se encuentra el bloque , se devuelve un nuevo lector o escritor de metadatos.                                                                                                                                                                                                                                                 |
| /\[\*\]tEXt/Keyword            | Obtiene o establece la propiedad Keyword para un fragmento PNG. Dado que la especificación de metadatos PNG permite varios fragmentos de un tipo determinado, la notación obtiene o establece el fragmento PNG de \[ \* \] datos con la propiedad adecuada. Según la especificación PNG, dos fragmentos no pueden tener las mismas propiedades.                                                                |



 

Cada bloque de metadatos también se identifica de forma única mediante el GUID de metadatos que se puede usar en lugar del nombre descriptivo del bloque. La sintaxis siguiente se puede usar en lugar de proporcionar nombres de bloque: "/{guid=GUID}/ \[ n \] {guid=GUID}/schema:tagidentifier"

En la tabla siguiente se proporcionan algunos ejemplos no válidos y las razones por las que se rechazarían. 

| Expresión no válida         | Descripción del rechazo                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /ifd/ \[ 0 \] \[ 2 \] exif/       | Se rechaza porque no se admiten índices de matriz multidimensional.                                                                                                    |
| /ifd/{ushort=1}/{ushort=2} | Se rechaza a menos que el IFD tenga un tagID=1, que es un controlador de metadatos que contiene un elemento de metadatos con un tagID=2.                                                        |
| /{ushort=1}                | Se rechaza si el procesamiento de consultas es relativo a un nivel superior de la jerarquía de metadatos. Esto se debe a que el nivel superior solo contiene bloques de metadatos y no elementos de datos. |



 

## <a name="photo-metadata-policy-expressions"></a>Expresiones de directiva de metadatos de fotos

Como se indicó anteriormente, una expresión de consulta completa comienza con una barra diagonal (/). Las expresiones que no comienzan con la barra diagonal se evalúan como expresiones de directiva. Una expresión de directiva le permite consultar los metadatos de la foto para obtener información relacionada con la imagen Windows [propiedades de Shell](https://msdn.microsoft.com/library/ms788673(VS.85).aspx). En la sección Selección de datos anterior de este documento, se usó la expresión "/xmp/xmp:Rating" para acceder a la propiedad de clasificación XMP. Esta propiedad también se puede consultar mediante la siguiente expresión de directiva:

-   System.SimpleRating

Para acceder a la propiedad de clasificación desde el esquema MicrosoftPhoto, se puede usar la siguiente expresión de consulta:

-   System.Rating

Las expresiones de directiva de metadatos de fotos se comportan de manera diferente a las consultas de metadatos completa de varias maneras importantes.

En primer lugar, al acceder a los metadatos mediante una expresión de directiva, WIC realiza el arbitraje y la resolución de conflictos en caso de que la misma propiedad esté disponible en varios bloques de metadatos. Por ejemplo, los valores de clasificación MicrosoftPhoto y XMP se almacenan tanto en el bloque App1/IFD como en el bloque XMP. La directiva de metadatos de fotos determina la prioridad para la que se devuelve el valor de bloque al leer los metadatos. Al escribir metadatos, la directiva de metadatos de fotos garantiza que las mismas propiedades de distintos bloques sean coherentes. Si usa una consulta de metadatos como "/xmp/xmp:Rating", usted es responsable de la distensión entre las distintas ubicaciones de metadatos.

> [!Note]  
> Para obtener una lista de las expresiones de directiva admitidas y sus directivas de asignación, vea el tema Directivas de [metadatos de](photo-metadata-policies.md) fotos.

 

En segundo lugar, las expresiones de directiva de metadatos de fotos son independientes del formato de imagen, mientras que las consultas de metadatos completa no lo son. Por ejemplo, la consulta "/xmp/xmp:Rating" es específica del formato JPEG. Las imágenes TIFF también admiten metadatos XMP, pero se almacenan de forma diferente en comparación con JPEG, por lo que la consulta TIFF sería "/ifd/xmp/xmp:Rating". Sin embargo, en ambos casos, la expresión de directiva sería "System.SimpleRating".

Las expresiones de directiva de metadatos de fotos proporcionan un mayor nivel de abstracción y simplicidad en comparación con las consultas de metadatos completa, por lo que deben ser preferibles en casos en los que no se necesita acceso a metadatos de bajo nivel. Sin embargo, las expresiones de directiva solo proporcionan acceso a un conjunto limitado de metadatos de imagen, mientras que el lenguaje de consulta de metadatos proporciona acceso a casi todos los metadatos almacenados en un archivo de imagen.

## <a name="metadata-query-language-summary"></a>Resumen del lenguaje de consulta de metadatos

La tabla siguiente es una definición formal del lenguaje de consulta de metadatos de WIC. Cada símbolo de gramática representa una expresión que se conste de otros símbolos. La expresión puede ser otro símbolo o una secuencia de otros símbolos separados por la barra vertical ( \| ), que indica una opción "o". La expresión completa de la derecha es una posible sustitución del símbolo especificado a la izquierda. 

| Símbolo                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item>\| <indexed item>&lt; Índice&gt;                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | '<' \<name> '>'                                                                                                                                                    |
| \<item>             | \<name>\| \& &gt; \<data> lt;index \|\<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \&lt;index&gt;            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | 'char' \| 'uchar' \| 'short' \| 'ushort' \| \| 'long' 'ulong' \| \| 'int' 'uint' \| 'longlong' \| 'ulonglong' \| 'float' \| 'double' \| 'str' \| 'wstr' \| 'guid' \| 'bool' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | number                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imágenes](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre extensibilidad de metadatos](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Cómo: Volver a codificar una imagen JPEG con metadatos](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 




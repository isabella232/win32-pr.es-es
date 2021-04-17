---
description: El sistema de propiedades de Windows es un sistema de lectura y escritura extensible de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Información general del sistema de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab3a17eacdbaa9a5d0255004ba544b7c3f7ff2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706115"
---
# <a name="property-system-overview"></a>Información general del sistema de propiedades

El sistema de propiedades de Windows es un sistema de lectura y escritura extensible de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell. El sistema de propiedades de Windows en Windows Vista y versiones posteriores le permite almacenar y recuperar metadatos para elementos de Shell. Un elemento de Shell es cualquier parte única de contenido, como un archivo, una carpeta, un correo electrónico o un contacto. Una propiedad es una parte individual de los metadatos asociados a un elemento de Shell. Los valores de propiedad se expresan como una estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Este tema se organiza de la siguiente manera:

-   [Introducción](#introduction)
-   [Escenarios de desarrollo](#development-scenarios)
-   [Propiedades y búsqueda de Windows](#properties-and-windows-search)
-   [Nota para los implementadores](#note-to-implementers)
-   [Documentación del sistema de propiedades de Windows](#windows-property-system-documentation)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Las propiedades se identifican de forma única mediante su nombre canónico (como `System.Document.LastAuthor` ) y la clave de propiedad (como `PKEY_Document_LastAuthor` ). Una clave de propiedad (PKEY) es la parte del nombre de un par nombre-valor que consta de un PKEY/PROPVARIANT o una cadena/PROPVARIANT, donde la cadena es el nombre canónico del PKEY (como `System.Document.LastAuthor` ). Un PKEY es una definición que indica al sistema de propiedades todo lo que necesita saber sobre la propiedad, mientras que el valor es una instancia real de la propiedad. Un PKEY contiene internamente un formatID y un propID.

Una propiedad individual consta de las tres partes siguientes:

-   Un nombre canónico, como `System.Music.Artist` .
-   Una descripción de esquema, que se especifica en el formato de archivo XML. propDesc y se expresa mediante programación a través de [**IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Un valor, como el nombre de un cantante.

La descripción del esquema consta de información sobre la propiedad, como el nombre de la propiedad, el tipo de datos, las restricciones, la información sobre cómo interactúa la propiedad con las vistas y el sistema de búsqueda, etc. El nombre y la descripción del esquema se definen globalmente y son los mismos para todos los elementos y tipos. Un valor es específico de un elemento individual. Es decir, la `System.Music.Artist` propiedad siempre se define como una cadena de varios valores, pero puede tener un valor diferente (o ningún valor en absoluto) para cada elemento.

Un controlador de propiedades traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que puede tener acceso el explorador de Windows, Windows Search y otras aplicaciones. Después, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer las propiedades del archivo. Los datos traducidos se exponen mediante programación y se muestran al usuario a través del explorador de Windows en diversos contextos, como vista de detalles, recuadros informativos, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedad está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Los desarrolladores deben implementar un controlador de propiedades que genere y consuma el formato nativo de su tipo de archivo, como. jpg o. png, o use el In-Memory almacén de propiedades, que genera y usa el formato binario MS-PROPSTORE.

El sistema de propiedades de Windows crea un modelo de datos abstracto que proporciona un nivel de abstracción a partir de formatos de archivo individuales. El modelo de datos abstracto proporcionado por el sistema de propiedades de Windows es un método para leer y escribir un conjunto extensible de valores con nombre que están asociados a un elemento de Shell. La expresión de valor es flexible, admite muchos tipos de datos y es extensible, lo que permite que los datos arbitrarios (**\_ BLOB de VT**) y los objetos se expresen como un valor.

Debido a la abstracción, puede consultar los atributos o metadatos de cualquier elemento. Algunos ejemplos de elementos que se pueden abstraer son Microsoft Office documentos, etiquetas ID3 y AutoCAD y otro software de propiedad de terceros. Del mismo modo, si tiene un archivo. JPEG, puede usar los códecs. JPEG y EXIF para leer los bytes del archivo para detectar cuáles son las dimensiones de la imagen. Si tiene un archivo. png en su lugar, necesitará un códec diferente y otro código para hacerlo. El uso del sistema de propiedades de Windows evita este tipo de problema. Si implementa un nuevo tipo de archivo, tiene la opción de conectarse a la abstracción uniforme ofrecida por el sistema de propiedades de Windows y especificar cómo hacer que los metadatos se consuman. Por estos motivos, siempre es preferible usar la plataforma común que proporciona el sistema de propiedades de Windows.

## <a name="development-scenarios"></a>Escenarios de desarrollo

Las propiedades las expresan los productores y los consumidores. En este contexto, los productores son los inventarios de propiedades en el sistema de propiedades de Windows y los consumidores son aplicaciones (y sus desarrolladores) que consumen información de propiedades de este sistema. Los usos de los participantes y en el sistema de propiedades de Windows se identifican en la tabla siguiente.



| Uso del sistema de propiedades de Windows                                                                                                                                                                                            | Participante |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Bloque de creación que proporciona un registro extensible de descripciones de propiedades, una implementación del almacén de propiedades en memoria y servicios para enlazar a controladores de propiedades, convertir tipos y serializar almacenes de propiedades. | Consumidor    |
| Aplicaciones que quieren leer y escribir propiedades de forma abstracta.                                                                                                                                                       | Consumidor    |
| Los inventores de propiedades que definen las nuevas propiedades del sistema de propiedades definiendo esquemas de propiedades personalizadas y desarrollando sus propios controladores de propiedades.                                                                          | Productor    |
| Propietarios de formato de archivo que desean habilitar el acceso a las propiedades almacenadas en sus formatos de archivo personalizados.                                                                                                                           | Productor    |



 

Los consumidores consumen propiedades, esquemas y controladores de propiedades existentes. Las propiedades disponibles para el consumo incluyen propiedades de lectura y escritura de los controladores de propiedades de los tipos de archivo compatibles y también pueden incluir algunas propiedades personalizadas. Los esquemas disponibles incluyen al menos el esquema del sistema y, a veces, otros también. Un consumidor puede crear una aplicación para consumir metadatos y crear una vista basada en el artista, independientemente de en qué carpetas se almacenan los elementos. La jerarquía de carpetas de archivos es irrelevante. Por ejemplo, puede especificar todos los elementos de la canción por un cantante determinado sin preocuparse por la ubicación de dichos elementos. Este escenario complejo de un extremo a otro no se limita al sistema de propiedades de Windows, sino que implica varios componentes diferentes, como las carpetas de indexación y búsqueda.

Los inventarios de propiedades, o los desarrolladores de terceros, son productores del sistema de propiedades de Windows. Al preparar la definición de una nueva propiedad, inspeccione primero el conjunto de propiedades que define Windows. Si encuentra una que satisface sus necesidades, del tipo y la semántica que coincida con el uso requerido, use esa propiedad y no inventar una nueva. Si está definiendo una nueva propiedad personalizada, intente obtener el acuerdo con otros desarrolladores que puedan querer usarla y publicar el resultado de ese contrato para que puedan unirse a la comunidad de usuarios de esa propiedad.

Los productores pueden aprovechar las ventajas de la funcionalidad del explorador de Windows. Por ejemplo, si está escribiendo un nuevo formato de imagen e implementa un controlador de propiedades, el nuevo formato de archivo estará disponible en el explorador de Windows. A continuación, los usuarios pueden etiquetar sus fotografías y dinamizar su colección de fotografías en función de cualquier propiedad del sistema de propiedades de Windows. De hecho, todo lo que hace Shell con las propiedades, los desarrolladores de terceros pueden hacerlo en sus propias aplicaciones. Esto incluye la agrupación, ordenación, consulta y visualización de propiedades completas. La experiencia del usuario que proporciona el explorador de Windows se puede implementar en gran medida por parte de terceros con API disponibles públicamente. El explorador de Windows se puede reemplazar o extender con estas API.

Desde el punto de vista de una aplicación que usa el modelo de datos de Shell, existe una gran variedad de escenarios que implican el uso del sistema de propiedades de Windows. Las aplicaciones de administración de medios son un ejemplo destacado. Los escenarios principales del sistema de propiedades incluyen escenarios como la lectura de la propiedad de palabra clave de una fotografía o la configuración de la propiedad datetaken. Ejemplos de escenarios de integración de un extremo a otro que el sistema de propiedades de Windows habilita, pero que requieren varios componentes para funcionar, incluyen Mostrar todas las imágenes o buscar un documento que contiene una palabra clave.

## <a name="properties-and-windows-search"></a>Propiedades y búsqueda de Windows

Las propiedades sirven a productores y consumidores cuando interactúan con búsqueda e indexación de Windows. Windows Search tiene una memoria caché de valores de propiedad que se usan en la implementación de Windows Search Service (WSS). Estos valores de propiedad se pueden consultar mediante programación con el proveedor de OLE DB de Windows Search o a través de [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa los elementos de los resultados de la búsqueda y las vistas basadas en consultas. Windows Search recopila y almacena las propiedades que emiten los controladores de filtro o los controladores de propiedades cuando se indiza un elemento como un documento de Word. Este almacén se descarta y se vuelve a generar cuando se vuelve a generar el índice.

> [!Note]  
> Recuerde que, al volver a registrar un esquema, el indizador no respeta los cambios realizados en los atributos de propiedades definidas previamente. La solución consiste en volver a generar el índice o introducir nuevas propiedades que reflejen los cambios en lugar de actualizar los anteriores (no se recomienda). Para obtener más información, vea la nota de los [implementadores](#note-to-implementers) más adelante en este tema.

 

Por ejemplo, un desarrollador que crea una aplicación multimedia desea mostrar a los usuarios de la aplicación toda la música disponible por un artista determinado. La aplicación proporcionará al usuario una lista de intérpretes disponibles y, a continuación, generará una lista de todas las música disponibles por el artista que seleccione el usuario. O bien, es posible que un usuario final desee realizar una consulta para? artista: Beethoven? y estar expuesto a la lista completa de propiedades disponibles en el transcurso de su búsqueda. Este ejemplo implica el uso del espacio de nombres de Shell, los controladores de propiedades y/o la consulta del índice a través de uno de los siguientes elementos:

-   Un origen de datos de Shell.
-   Proveedor OLE DB.
-   Un archivo de búsqueda guardado (. Search-MS) que se usa para iniciar una consulta desplazándose hasta el archivo de búsqueda en el explorador de Windows o enlazando a [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) mediante programación.

> [!Note]  
> Aunque la `System.Kind` propiedad no participa en este escenario de aplicación multimedia, podría usarse para crear una consulta que devolvería todos los archivos. Search-MS en un ámbito determinado.

 

La mejor manera de tener acceso a las API de búsqueda y crear aplicaciones de Windows Search es a través de un origen de datos de Shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) es un componente que puede crear instancias del origen de datos de la carpeta de búsqueda, que es un tipo de origen de datos "virtual" proporcionado por el shell que puede ejecutar consultas sobre otros orígenes de datos en el espacio de nombres del shell y enumerar los resultados. Puede hacerlo mediante el indizador, o bien enumerando e inspeccionando manualmente los elementos de los ámbitos especificados.

Los desarrolladores de terceros pueden crear aplicaciones que consuman los datos en el índice mediante consultas mediante programación y pueden extender los datos del índice para que los tipos de archivo y elemento personalizados los indexe Windows Search. Si desea mostrar los resultados de la consulta en el explorador de Windows, debe implementar un origen de datos de Shell antes de poder crear un controlador de protocolo para extender el índice. Sin embargo, si todas las consultas se realizarán mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, un espacio de nombres del shell sigue siendo preferible, pero no es necesario. Se requiere un controlador de protocolo para que Windows obtenga información sobre el contenido de los archivos, como los elementos de las bases de datos o los tipos de archivo personalizados. Aunque Windows Search puede indizar el nombre y las propiedades del archivo, Windows no tiene información sobre el contenido del archivo. Como resultado, estos elementos no se pueden indizar ni exponer en el shell de Windows. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando conseguir, vea "información general de los controladores" en [Windows Search como plataforma de desarrollo](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. Un controlador a veces se conoce como una extensión de shell o un controlador de extensión de Shell.

 

## <a name="note-to-implementers"></a>Nota para los implementadores

Debido a las posibles dificultades que puede tener el indizador al consumir el esquema del sistema de propiedades, es fundamental que defina los atributos con cuidado y de forma estratégica para la primera versión del esquema. Cualquier cambio en los atributos (tipo, ancho de columna, si indexable) no se reflejará en la base de datos después de que se haya registrado un esquema. Las únicas maneras de que estos cambios se reconozcan después de que el esquema se haya registrado una vez en un sistema serían volver a generar el índice y, a continuación, registrar el nuevo esquema, o registrar el esquema y, a continuación, crear una nueva propiedad para cada versión posterior; por ejemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , y así sucesivamente. No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas extrañas pueden afectar al rendimiento del sistema.

## <a name="windows-property-system-documentation"></a>Documentación del sistema de propiedades de Windows

El resto de esta documentación contiene las siguientes secciones:

-   [Guía del desarrollador del sistema de propiedades de Windows](property-system-developer-s-guide.md)

    Describe en detalle cómo implementar los escenarios de desarrollo principales con el sistema de propiedades de Windows.

-   [Referencia del sistema de propiedades](property-system-reference.md)

    Documenta las [propiedades de Windows](props.md), el [esquema de descripción de propiedades](property-description-schema.md), las [interfaces](interfaces.md), [las funciones, las](functions.md) [estructuras](structures.md)y las [constantes, las enumeraciones y las marcas](constants--enumerations--and-flags.md) del sistema de propiedades de Windows.

-   [Ejemplos de código del sistema de propiedades](property-system-code-samples.md)

    Describe ejemplos que muestran cómo usar el sistema de propiedades de Windows.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo reutilizar el almacén de propiedades In-Memory, vea [inicializar controladores de propiedades](building-property-handlers-property-handlers.md) y [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Para obtener una especificación del formato de archivo binario del almacén de propiedades de Microsoft, consulte [ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   La relación entre la búsqueda de Windows y la indexación, y cómo extender el índice, se explica en los temas siguientes en Windows Search:
    -   [Desarrollar controladores de filtro para Windows Search](../search/-search-ifilter-conceptual.md)
    -   [Desarrollo de controladores de protocolo para Windows Search](../search/-search-3x-wds-phaddins.md)
    -   [Desarrollar controladores de propiedades para Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Para Windows 7 o la descarga del SDK de Windows Vista actualizado, consulte la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía del desarrollador del sistema de propiedades de Windows](property-system-developer-s-guide.md)
</dt> <dt>

[Referencia del sistema de propiedades](property-system-reference.md)
</dt> <dt>

[Ejemplos de código del sistema de propiedades](property-system-code-samples.md)
</dt> </dl>

 

 

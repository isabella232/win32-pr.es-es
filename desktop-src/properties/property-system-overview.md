---
description: El Windows propiedad es un sistema extensible de lectura y escritura de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Información general del sistema de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742eebbdb05541a3cfcc1468cd0f93d255f13b67b4bfe777729d1d02d2ed70a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460035"
---
# <a name="property-system-overview"></a>Información general del sistema de propiedades

El Windows propiedad es un sistema extensible de lectura y escritura de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell. El Windows property de Windows Vista y versiones posteriores le permite almacenar y recuperar metadatos para los elementos de Shell. Un elemento de Shell es cualquier elemento de contenido único, como un archivo, una carpeta, un correo electrónico o un contacto. Una propiedad es un fragmento individual de metadatos asociado a un elemento de Shell. Los valores de propiedad se expresan [**como una estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Este tema se organiza de la siguiente manera:

-   [Introducción](#introduction)
-   [Escenarios de desarrollo](#development-scenarios)
-   [Propiedades y búsqueda Windows búsqueda](#properties-and-windows-search)
-   [Nota para los implementadores](#note-to-implementers)
-   [Windows Documentación del sistema de propiedades](#windows-property-system-documentation)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Las propiedades se identifican de forma única por su nombre canónico (como ) y `System.Document.LastAuthor` la clave de propiedad (como `PKEY_Document_LastAuthor` ). Una clave de propiedad (PKEY) es la parte del nombre de un par nombre-valor que consta de un PKEY/PROPVARIANT o una cadena/PROPVARIANT, donde la cadena es el nombre canónico de PKEY (por ejemplo, `System.Document.LastAuthor` ). Un PKEY es una definición que indica al sistema de propiedades todo lo que necesita saber sobre la propiedad, mientras que el valor es una instancia real de la propiedad. Un PKEY contiene internamente un formatID y propID.

Una propiedad individual consta de las tres partes siguientes:

-   Un nombre canónico, como `System.Music.Artist` .
-   Descripción del esquema, que se especifica en el formato de archivo XML .propdesc y se expresa mediante programación a través [**de IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Valor, como el nombre de un grupo.

La descripción del esquema consta de información sobre la propiedad, como el nombre de la propiedad, el tipo de datos, las restricciones, la información sobre cómo interactúa la propiedad con las vistas y el sistema de búsqueda, etc. El nombre y la descripción del esquema se definen globalmente y son iguales para todos los elementos y tipos. Un valor es específico de un elemento individual. Es decir, la propiedad siempre se define como una cadena de varios valores, pero puede tener un valor diferente (o ningún valor `System.Music.Artist` en absoluto) para cada elemento.

Un controlador de propiedades convierte los datos almacenados en un archivo en un esquema estructurado reconocido por y al que pueden acceder Windows Explorer, Windows Search y otras aplicaciones. A continuación, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer propiedades en y desde el archivo. Los datos traducidos se exponen mediante programación y se muestran al usuario a través de Windows Explorer en una variedad de contextos, como la vista de detalles, información sobre información, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedades está asociado a un tipo de archivo determinado, que se identifica mediante la extensión de nombre de archivo. Los desarrolladores deben implementar un controlador de propiedades que genera y consume el formato nativo de su tipo de archivo, como .jpg o .png, o usar el In-Memory Almacén de propiedades, que genera y consume el formato binario MS-PROPSTORE.

El Windows propiedad crea un modelo de datos abstracto que proporciona un nivel de abstracción a partir de formatos de archivo individuales. El modelo de datos abstracto proporcionado por Windows Property System es un método para leer y escribir un conjunto extensible de valores con nombre asociados a un elemento de Shell. La expresión de valor es flexible, admite muchos tipos de datos y es extensible, lo que permite que los datos arbitrarios **(VT \_ BLOB)** y los objetos se exprese como un valor.

Debido a la abstracción, puede consultar los atributos o metadatos de cualquier elemento. Entre los ejemplos de elementos que se pueden abstraer se incluyen Microsoft Office, etiquetas ID3 y AutoCAD software propietario de terceros. Del mismo modo, si tiene un archivo .jpeg, puede usar los códecs .jpeg y EXIF para leer los bytes del archivo para detectar cuáles son las dimensiones de la imagen. Si tiene un archivo .png, necesita un códec diferente y otro código para hacerlo. El uso del Windows de propiedades evita este tipo de problema. Si implementa un nuevo tipo de archivo, tiene la opción de conectarse a la abstracción uniforme que ofrece el sistema de propiedades de Windows y especificar cómo hacer que los metadatos se consuma. Por estos motivos, siempre es preferible usar la plataforma común proporcionada por el sistema de Windows propiedad.

## <a name="development-scenarios"></a>Escenarios de desarrollo

Las propiedades las expresan los productores y los consumidores. En este contexto, los productores son los inventores de las propiedades del sistema de propiedades Windows y los consumidores son aplicaciones (y sus desarrolladores) que consumen información de propiedades de este sistema. En la tabla siguiente se identifican los Windows y de los participantes en el sistema de propiedades.



| Uso del sistema Windows propiedades                                                                                                                                                                                            | Participante |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Bloque de creación que proporciona un registro extensible de descripciones de propiedades, una implementación de almacén de propiedades en memoria y servicios para enlazar a controladores de propiedades, convertir tipos y serializar almacenes de propiedades. | Consumidor    |
| Aplicaciones que desean leer y escribir propiedades de forma abstracta.                                                                                                                                                       | Consumidor    |
| Inventores de propiedades que definen nuevas propiedades para el sistema de propiedades mediante la definición de esquemas de propiedades personalizados y el desarrollo de sus propios controladores de propiedades.                                                                          | Productor    |
| Propietarios de formato de archivo que desean habilitar el acceso a las propiedades almacenadas en sus formatos de archivo personalizados.                                                                                                                           | Productor    |



 

Los consumidores consumen propiedades, esquemas y controladores de propiedades existentes. Las propiedades disponibles para el consumo incluyen propiedades de lectura y escritura de controladores de propiedades para los tipos de archivo admitidos y también pueden incluir algunas propiedades personalizadas. Los esquemas disponibles incluyen al menos el esquema del sistema y, a veces, otros también. Un consumidor puede crear una aplicación para consumir metadatos y crear una vista basada en artist, independientemente de las carpetas en las que se almacenan los elementos. La jerarquía de carpetas de archivos es irrelevante. Por ejemplo, puede especificar todos los elementos de canción por un momento determinado sin preocuparse por la ubicación de dichos elementos. Este escenario complejo de un extremo a otro no se limita al sistema de propiedades Windows, sino que implica varios componentes diferentes, como las carpetas de indexación y búsqueda.

Los inventores de propiedades o desarrolladores de terceros son productores del Windows propiedad. Al prepararse para definir una nueva propiedad, inspeccione primero el conjunto de propiedades que Windows define. Si encuentra uno que satisfaga sus necesidades, del tipo y la semántica que coincidan con su uso necesario, use esa propiedad y no inventar una nueva. Si va a definir una nueva propiedad personalizada, intente obtener un acuerdo con otros desarrolladores que quieran usarla y publicar el resultado de ese contrato para que puedan unirse a la comunidad de usuarios de esa propiedad.

Los productores pueden aprovechar las ventajas de Windows Explorer. Por ejemplo, si escribe un nuevo formato de imagen e implementa un controlador de propiedades, el nuevo formato de archivo estará disponible en Windows Explorer. A continuación, los usuarios pueden etiquetar sus fotografías y dinamr su colección de fotografías en función de cualquier propiedad del Windows propiedad. De hecho, todo lo que Shell hace con las propiedades, los desarrolladores de terceros pueden hacer en sus propias aplicaciones. Esto incluye la agrupación, ordenación, consulta y visualización de propiedades completa. La experiencia del usuario Windows Explorer puede implementarse en gran medida por terceros con API disponibles públicamente. Windows El Explorador se puede reemplazar o extender mediante estas API.

Desde el punto de vista de una aplicación que usa el modelo de datos de Shell, hay una gran variedad de escenarios que implican el uso del Windows de propiedades. Las aplicaciones de administración de medios son un ejemplo destacado. Los escenarios principales del sistema de propiedades incluyen escenarios como leer la propiedad keyword de una fotografía o establecer la propiedad datetaken. Entre los ejemplos de escenarios de integración de un extremo a otro que habilita el sistema de propiedades de Windows, pero que requieren que funcionen otros componentes, se incluyen la presentación de todas las imágenes o la búsqueda de un documento que contenga una palabra clave.

## <a name="properties-and-windows-search"></a>Propiedades y búsqueda Windows búsqueda

Las propiedades sirven tanto a los productores como a los consumidores cuando se Windows búsqueda e indexación. Windows La búsqueda tiene una caché de valores de propiedad que se usan en la implementación de Windows Search Service (WSS). Estos valores de propiedad se pueden consultar mediante programación mediante el proveedor de Windows Search OLE DB o mediante [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa los elementos de los resultados de búsqueda y las vistas basadas en consultas. Windows A continuación, search recopila y almacena las propiedades emitidas por controladores de filtro o controladores de propiedades cuando se indexa un elemento como un documento de Word. Este almacén se descarta y se recompila cuando se recompila el índice.

> [!Note]  
> Recuerde que al volver a registrar un esquema, es posible que el indexador no respete los cambios realizados en los atributos de las propiedades definidas previamente. La solución es recompilar el índice o introducir nuevas propiedades que reflejen los cambios en lugar de actualizar los antiguos (no recomendado). Para obtener más información, vea [Nota para implementadores más](#note-to-implementers) adelante en este tema.

 

Por ejemplo, un desarrollador que crea una aplicación multimedia quiere mostrar a los usuarios de la aplicación toda la música disponible de un determinado intérprete. La aplicación proporcionaría al usuario una lista de los intérpretes disponibles y, a continuación, generaría una lista de todas las músicas disponibles por el intérprete que el usuario selecciona. O bien, es posible que un usuario final quiera realizar una consulta para ?artist:Taxis? y exponerse a la lista completa de propiedades disponibles en el transcurso de su búsqueda. Este ejemplo implica el uso del espacio de nombres shell, los controladores de propiedades o la consulta del índice a través de una de las siguientes opciones:

-   Origen de datos de Shell.
-   Proveedor OLE DB.
-   Un archivo de búsqueda guardado (.search-ms) que se usa para iniciar una consulta navegando al archivo de búsqueda en el Explorador de Windows o enlazando a [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) mediante programación.

> [!Note]  
> Aunque la propiedad no participa en este escenario de aplicación multimedia, se podría usar para compilar una consulta que devolvería todos los archivos `System.Kind` .search-ms en un ámbito determinado.

 

La manera preferida de acceder a las API de búsqueda y crear Windows Search es a través de un origen de datos de Shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) es un componente que puede crear instancias del origen de datos de la carpeta Search, que es una especie de origen de datos "virtual" proporcionado por el Shell que puede ejecutar consultas sobre otros orígenes de datos en el espacio de nombres de Shell y enumerar los resultados. Puede hacerlo mediante el indexador o enumerando e inspeccionando manualmente los elementos de los ámbitos especificados.

Los desarrolladores de terceros pueden crear aplicaciones que consuman los datos del índice a través de consultas mediante programación y pueden ampliar los datos del índice para los tipos de archivo y elemento personalizados que se indexarán mediante Windows Search. Si desea mostrar los resultados de la consulta en Windows Explorer, debe implementar un origen de datos de Shell para poder crear un controlador de protocolo para ampliar el índice. Sin embargo, si todas las consultas van a ser mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, se prefiere un espacio de nombres de Shell, pero no es necesario. Se requiere un controlador de protocolo para Windows obtener información sobre el contenido del archivo, como elementos de bases de datos o tipos de archivo personalizados. Aunque Windows Search puede indexar el nombre y las propiedades del archivo, Windows no tiene información sobre el contenido del archivo. Como resultado, estos elementos no se pueden indexar ni exponer en el Windows Shell. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando lograr, vea "Información general de los controladores" en [Windows Search como](../search/-search-3x-wds-development-ovr.md)plataforma de desarrollo .

> [!Note]  
> Un origen de datos de Shell se conoce a veces como una extensión de espacio de nombres de Shell. A veces, un controlador se conoce como una extensión de Shell o un controlador de extensión de Shell.

 

## <a name="note-to-implementers"></a>Nota para implementadores

Debido a las posibles dificultades que puede tener el indexador al consumir el esquema del sistema de propiedades, es fundamental definir los atributos de forma cuidadosa y estratégica para la primera versión del esquema. Los cambios en los atributos (tipo, ancho de columna, si se pueden indexar) no se reflejarán en la base de datos después de registrar un esquema. Las únicas maneras de que estos cambios se reconozcan después de registrar el esquema una vez en un sistema sería volver a generar el índice y, a continuación, registrar el nuevo esquema, o registrar el esquema y, a continuación, crear una nueva propiedad para cada versión posterior. por `PKEY_GroupName_PropertyNameV2` ejemplo, `PKEY_GroupName_PropertyNameV3` , , etc. No se recomienda crear nuevas propiedades de esta manera, ya que varias columnas externas pueden afectar al rendimiento del sistema.

## <a name="windows-property-system-documentation"></a>Windows Documentación del sistema de propiedades

El resto de esta documentación contiene las secciones siguientes:

-   [Windows Guía del desarrollador del sistema de propiedades](property-system-developer-s-guide.md)

    Describe en detalle cómo implementar los principales escenarios de desarrollo mediante el Windows propiedades.

-   [Referencia del sistema de propiedades](property-system-reference.md)

    Documenta [Windows](props.md)propiedades, esquema de [descripción](property-description-schema.md)de propiedad, [interfaces](interfaces.md) [,](structures.md) [funciones](functions.md), estructuras y [constantes,](constants--enumerations--and-flags.md) enumeraciones y marcas del sistema de Windows propiedades.

-   [Ejemplos de código del sistema de propiedades](property-system-code-samples.md)

    Describe ejemplos que muestran cómo usar el sistema de Windows propiedades.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo volver a In-Memory Almacén de propiedades, vea [Inicializar](building-property-handlers-property-handlers.md) controladores de propiedades y [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Para obtener una especificación del formato de Almacén de propiedades binario de Microsoft, vea [ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   La relación entre Windows search y la indexación, y cómo ampliar el índice, se explican en los temas siguientes en Windows Search:
    -   [Desarrollar controladores de filtro para la Windows búsqueda](../search/-search-ifilter-conceptual.md)
    -   [Desarrollar controladores de protocolo para Windows Search](../search/-search-3x-wds-phaddins.md)
    -   [Desarrollar controladores de propiedades para Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Para ver la Windows 7 o la actualización Windows SDK de Vista, consulte el sdk [de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guía del desarrollador del sistema de propiedades](property-system-developer-s-guide.md)
</dt> <dt>

[Referencia del sistema de propiedades](property-system-reference.md)
</dt> <dt>

[Ejemplos de código del sistema de propiedades](property-system-code-samples.md)
</dt> </dl>

 

 

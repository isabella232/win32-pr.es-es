---
description: Para indizar el contenido y las propiedades de los nuevos formatos de archivo y almacenes de datos, Microsoft Windows Search debe extenderse con complementos.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search como plataforma de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808983"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search como plataforma de desarrollo

Para indizar el contenido y las propiedades de los nuevos formatos de archivo y almacenes de datos, Microsoft Windows Search debe extenderse con complementos.

Antes de que un desarrollador de terceros con nuevos formatos de archivo y almacenes de datos pueda obtener esos formatos y almacenes para que aparezcan en los resultados de la consulta en el explorador de Windows, el desarrollador debe hacer lo siguiente:

-   Implemente un origen de datos de Shell para extender el espacio de nombres del shell.
-   Exponga los elementos de un almacén de datos (si están agregando un nuevo almacén de datos, ya que es necesario indizar).
-   Desarrolle un controlador de protocolo para que Windows Search pueda acceder a los datos para la indexación.

Este tema se organiza de la siguiente manera:

-   [Introducción](#getting-started)
-   [Información general sobre los escenarios de desarrollo de búsqueda](#overview-of-search-development-scenarios)
    -   [Adición de un nuevo almacén de datos](#adding-a-new-data-store)
    -   [Agregar un nuevo formato de archivo](#adding-a-new-file-format)
    -   [Consumir resultados de Windows Search](#consuming-windows-search-results)
-   [Información general de los controladores](#overview-of-handlers)
-   [Instrucciones del instalador de complementos](#add-in-installer-guidelines)
-   [Nota para los implementadores](#note-to-implementers)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="getting-started"></a>Introducción

Antes de empezar a crear una aplicación de Windows Search, recuerde que la mejor manera de hacerlo es a través de un origen de datos de Shell. Un origen de datos de Shell extiende el espacio de nombres del shell y expone los elementos de un almacén de datos. Después, el sistema de Windows Search puede indizar los elementos del almacén de datos mediante un controlador de protocolo. Se prefiere este enfoque indirecto para tener acceso a la búsqueda de Windows mediante la implementación de un origen de datos de Shell, ya que proporciona acceso a toda la funcionalidad del shell. De este modo, se garantiza una experiencia de usuario razonable.

Si desea que los resultados de la consulta aparezcan en el explorador de Windows, debe implementar un origen de datos de Shell antes de poder crear un controlador de protocolo para extender el índice. Sin embargo, si todas las consultas se realizarán mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, el espacio de nombres del shell sigue siendo preferible, pero no es necesario.

Se requiere un controlador de protocolo para que Windows obtenga conocimiento del contenido del archivo, como los elementos de las bases de datos o los tipos de archivo personalizados. Aunque Windows Search puede indizar el nombre y las propiedades del archivo, Windows no tiene ningún conocimiento del contenido del archivo. Como resultado, estos elementos no se pueden indizar ni exponer en el shell de Windows. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando conseguir, consulte [información general de los controladores](#overview-of-handlers).

## <a name="overview-of-search-development-scenarios"></a>Información general sobre los escenarios de desarrollo de búsqueda

Los escenarios de desarrollo más comunes en la búsqueda de Windows son:

-   [Adición de un nuevo almacén de datos](#adding-a-new-data-store)
-   [Agregar un nuevo formato de archivo](#adding-a-new-file-format)
-   [Consumir resultados de Windows Search](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Adición de un nuevo almacén de datos

Solo necesita un almacén de datos de Shell para Windows Search si va a agregar un nuevo almacén de datos que se va a indexar. Un almacén de datos es un repositorio de datos que se puede exponer en el modelo de programación de shell como un contenedor mediante un origen de datos de Shell. Después, el sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo. El controlador de protocolo implementa el protocolo para tener acceso a un origen de contenido en su formato nativo. Las interfaces [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) y [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) se usan para implementar un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indizar. Para obtener información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Agregar un nuevo formato de archivo

Si agrega un nuevo formato de archivo personalizado, debe desarrollar un controlador de filtro o un controlador de propiedades, pero no ambos. Un filtro es una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Abre los archivos de un tipo de archivo determinado y filtra las propiedades y fragmentos de texto del indexador. Los filtros se asocian a los tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLSID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo de archivo funciona con un solo filtro.

Un controlador de propiedades traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que puede tener acceso el explorador de Windows, Windows Search y otras aplicaciones. Después, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer propiedades en un archivo. Los datos traducidos incluyen vista de detalles, recuadros informativos, panel de detalles, páginas de propiedades, etc. Cada controlador de propiedad está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Necesita un controlador de propiedad para hacer lo siguiente:

-   Muestra las propiedades de los elementos no indexados en la interfaz de usuario.
-   Permite escribir propiedades.

### <a name="consuming-windows-search-results"></a>Consumir resultados de Windows Search

En las secciones siguientes se describen varias formas de utilizar los resultados de la búsqueda de Windows:

-   [Consultar datos](#querying-data)
-   [Consultar almacenes de datos remotos (búsqueda federada)](#querying-remote-data-stores-federated-search)
-   [Indexación de archivos y elementos](#indexing-files-and-items)
-   [Indexación de un almacén de datos](#indexing-a-data-store)
-   [Administrar el proceso de indexación](#managing-the-indexing-process)
-   [Integración del sistema de propiedades de Windows con las aplicaciones de Windows Search](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Consulta de datos

Los desarrolladores que escriben aplicaciones sobre la combinación de Windows Search y el sistema de propiedades de Windows pueden tener acceso a archivos y elementos independientemente de la aplicación o el tipo de archivo. Hay dos maneras de que las aplicaciones tengan acceso a los datos del indexador:

-   Las aplicaciones se comunican directamente con OLE DB mediante el envío de consultas de Windows Search Lenguaje de consulta estructurado (SQL) al proveedor de OLE DB de Windows Search para recuperar los resultados. Las consultas se pueden construir manualmente o mediante la interfaz [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para generar el SQL a partir de palabras clave de búsqueda y la sintaxis de consulta avanzada (AQS).
-   Las aplicaciones funcionan a través de la capa de Shell. La ventaja de la capa de Shell es que también admite otros orígenes como grep. Sin embargo, el inconveniente es que no todas las características del indexador están disponibles.

Otra opción es usar los protocolos Search-MS://y search://, que ejecutan las búsquedas basadas en URL que se representan a través del explorador de Windows. Esta opción habilita el desarrollo más ligero pero no devuelve resultados ni selecciones de usuario de la vista de resultados a la aplicación que realiza la llamada. Además, al igual que otros protocolos, las aplicaciones de búsqueda de terceros pueden asumir los protocolos Search-MS://y search://si las aplicaciones se ajustan al conjunto de características necesario. Para obtener más información acerca de las consultas, vea [consultar el proceso en Windows Search](querying-process--windows-search-.md) y [consultar el índice mediante programación](-search-3x-wds-qryidx-overview.md).

### <a name="querying-remote-data-stores-federated-search"></a>Consultar almacenes de datos remotos (búsqueda federada)

En Windows 7 y versiones posteriores, la búsqueda federada ofrece un nuevo proveedor de búsquedas que consulta los almacenes de datos remotos a través de servidores Web, a través del protocolo [OpenSearch](https://github.com/dewitt/opensearch) , y enumera los resultados como fuentes XML de Atom o RSS. Los conectores de búsqueda son uniones de espacios de nombres que simulan el comportamiento de carpetas mediante un proveedor de búsquedas. Para obtener más información acerca de la Federación de búsqueda en almacenes de datos remotos en Windows 7, consulte [búsqueda federada en Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indexación de archivos y elementos

El contenido que se indexa se basa en el archivo y los tipos de datos admitidos a través de complementos incluidos con Windows Search y las reglas de inclusión y exclusión predeterminadas para las carpetas del sistema de archivos. Por ejemplo, los filtros incluidos en la búsqueda de Windows admiten más de 200 tipos comunes de datos, como documentos de Microsoft Office, correo electrónico de Microsoft Outlook (junto con el controlador de protocolo MAPI), archivos de texto sin formato, HTML y muchos más. Para obtener una lista completa de los tipos de archivo admitidos de forma nativa, vea [qué se incluye en el índice](-search-3x-wds-included-in-index.md).

El índice se puede extender con controladores de propiedades y filtros para exponer el contenido y las propiedades de los nuevos formatos de archivo en el índice y el explorador de Windows. Los filtros son una implementación de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Hay dos tipos de filtros: uno que interactúa con elementos individuales, como archivos y otro que interactúa con contenedores como carpetas. Los filtros tienen varios propósitos, ya que admiten la fragmentación de datos, el contenido de texto, algunas propiedades y varios lenguajes.

En cambio, los controladores de propiedades tienen un propósito más específico: para exponer las propiedades de tipos de archivo específicos que se identifican mediante las extensiones de nombre de archivo. Un controlador de propiedades para un tipo de archivo puede habilitar las propiedades get y Set, y puede enumerar las propiedades asociadas a ese tipo de archivo. A diferencia de los filtros, los controladores de propiedades no admiten datos o contenido de texto de Chuck, y los controladores de propiedades no tienen forma de indicar en qué idioma se encuentra una propiedad de texto a menos que admitan la escritura de propiedades.

### <a name="indexing-a-data-store"></a>Indexación de un almacén de datos

El índice se puede extender con controladores de protocolo para proporcionar acceso a almacenes de datos de propiedad. Por ejemplo, los archivos y elementos contenidos en los almacenes de datos que no son del sistema de archivos (como las bases de datos y los almacenes de correo electrónico) requieren un controlador de protocolo para asignar desde una dirección URL a una secuencia. Los controladores de protocolo también pueden determinar opcionalmente los filtros correctos que se usarán para extraer información de una secuencia. Los filtros enumeran las direcciones URL del almacén de datos. Los elementos se indexan individualmente mediante el filtro o el controlador de propiedad adecuados. Para obtener más información, vea [extender el índice](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Administrar el proceso de indexación

Los desarrolladores de aplicaciones pueden controlar el ámbito y la frecuencia de la indización de Windows Search mediante el uso de varias interfaces de administración. Estas interfaces incluyen funcionalidad para agregar y quitar los directorios en los que el indexador busca cambios, notificar manualmente el índice de los cambios a los datos, comprobar el estado del indexador y forzar la reindización de algunos o todos los datos. Para obtener más información, vea [administrar el índice](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>Integración del sistema de propiedades de Windows con las aplicaciones de Windows Search

El sistema de propiedades de Windows es un sistema de lectura y escritura extensible de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre los elementos de Shell. El sistema de propiedades de Windows en Windows Vista y versiones posteriores le permite almacenar y recuperar metadatos para elementos de Shell. Un elemento de Shell es cualquier parte única de contenido, como un archivo, una carpeta, un correo electrónico o un contacto. Una propiedad es una parte individual de los metadatos asociados a un elemento de Shell. Los valores de propiedad se expresan como una estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Se incluye una amplia lista de propiedades comunes para varios tipos de elementos comunes, como fotos, música, documentos, mensajes, contactos y archivos. Los desarrolladores también pueden introducir sus propias propiedades en la plataforma si ninguna propiedad existente satisface sus necesidades. Para obtener más información sobre la integración de aplicaciones con el sistema de propiedades de Windows, vea [desarrollar controladores de propiedades](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Información general de los controladores

Un controlador es un objeto COM (modelo de objetos componentes) que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta sistema de archivos utiliza el sistema de Asociación para buscar los controladores de un tipo de archivo determinado. Se requiere un controlador específico para cada tipo de archivo. Se requiere un controlador de filtro para el tipo de archivo Adobe Acrobat. pdf, por ejemplo, se requiere otro controlador de filtro para el formato de archivo. doc, etc.

Los diferentes controladores tienen algunas similitudes. En Windows Vista y versiones posteriores, todos los controladores deben usar una de las interfaces siguientes para inicializar el controlador: [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

En la tabla siguiente se enumeran las tareas de desarrollador de alto nivel, el tipo de controlador necesario para cada tarea, y se proporciona un vínculo a información conceptual acerca de cómo realizar cada tarea.



| Tarea                                                                                                                                                            | Controlador                          | Información conceptual                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtener acceso a las propiedades de un archivo para la indexación                                                                                                                 | Controlador de propiedades                 | [Desarrollar controladores de propiedades](-search-3x-wds-extidx-propertyhandlers.md)<br/> [Propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Agregar formatos del portapapeles para el objeto de datos ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) de un elemento (los objetos de datos se utilizan en escenarios de arrastrar y colocar, y copiar y pegar). | Controlador de objeto de datos              | [Crear controladores de datos](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Agregar verbos para un elemento que se muestran normalmente en un menú contextual                                                                                         | Controlador del menú contextual            | [Crear controladores de menú contextual](../shell/context-menu-handlers.md)<br/> [Personalización de un menú contextual mediante verbos dinámicos](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Asociar un tipo de archivo a un icono específico                                                                                                                    | Controlador de iconos                     | [Crear controladores de iconos](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Crear hojas de propiedades con imágenes y controles de interfaz de usuario que permiten la interacción personalizada con un tipo de archivo                                                          | Controlador de la hoja de propiedades           | [Controladores de hoja de propiedades](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Habilitar un tipo de elemento para admitir escenarios de arrastrar y colocar, y copiar y pegar                                                                                         | Quitar controlador                     | [Transferir objetos de Shell con arrastrar y colocar y el portapapeles](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Extraer fragmentos de texto y propiedades de documento para la indexación                                                                                                  | Controlador de filtro                   | [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indexación de un nuevo tipo de archivo                                                                                                                                        | Controlador de filtro, controlador de propiedades | [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)<br/> [Desarrollar controladores de propiedades](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indizar el contenido de un almacén de datos                                                                                                                           | Controlador de protocolo                 | [Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)                                                                                                                                            |
| Vista previa de una vista simplificada del elemento de Shell en el panel de vista previa del explorador de Windows                                                                             | Controlador de vista previa                  | [Controladores de vista previa](../shell/preview-handlers.md)                                                                                                                                                             |
| Proporcionar texto emergente cuando se mantiene el mouse sobre un objeto de interfaz de usuario                                                                                                      | Controlador de recuadro informativo                  | [Crear controladores de extensión de Shell](../shell/handlers.md) (personalización de recuadro)                                                                                                                            |
| Proporcionar una imagen estática para representar un elemento de Shell                                                                                                              | Controlador de miniaturas                | [Controladores en miniatura](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

En la tabla siguiente se enumeran los controladores y las interfaces para implementar cada tipo de controlador.



| Controlador                | Interfaces                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quitar controlador           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), [**IDropTargetHelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Controlador de objeto de datos    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Controlador de filtro         | [**Imaging**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Controlador de iconos           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Opcional: [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| Controlador de recuadro informativo        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Controlador de vista previa        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Controlador de propiedades       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Controlador de protocolo       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol), [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Opcional: [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2), [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2), [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3), [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Controlador de la hoja de propiedades | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Controlador del menú contextual  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Controlador de miniaturas      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> A veces, un controlador de propiedades se kown como un controlador de metadatos. Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. Un controlador de tipo de archivo a veces se conoce como controlador de extensión de shell o extensión de Shell.

 

Para obtener más información sobre la creación de controladores, vea [crear controladores de extensión de Shell](../shell/handlers.md). Para obtener más información sobre las propiedades, vea [sistema de propiedades de Windows](../properties/windows-properties-system.md).

## <a name="add-in-installer-guidelines"></a>Instrucciones del instalador de complementos

Siga estas instrucciones al crear un instalador de complementos:

-   El instalador debe utilizar el instalador EXE o MSI.
-   Se deben proporcionar las notas de la versión.
-   Se debe crear una entrada **Agregar o quitar programas** para cada complemento instalado.
-   El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.
-   Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito un complemento anterior, el usuario debe ser capaz de restaurar la funcionalidad del complemento anterior y volver a convertirlo en el complemento predeterminado para ese tipo de archivo o almacén.

## <a name="note-to-implementers"></a>Nota para los implementadores

Antes de crear un filtro o un controlador de propiedades, los desarrolladores deben tener en cuenta lo siguiente:

-   Estos controladores son extensiones en proceso que se cargan en procesos que no controla, como el proceso de demonio de filtro, el explorador de Windows (búsqueda de grep) y los hosts de terceros como Windows Mail).
-   Debe escribir código seguro que sea lo suficientemente eficaz como para controlar los formatos de archivo dañados arbitrariamente que se crearon para atacar el sistema.
-   El complemento no debe perder los recursos que producirán problemas en los procesos de host.
-   El complemento no debe bloquearse, ya que esto también bloqueará los procesos de host y ralentizará el proceso de filtrado.
-   Dado que estos controladores se ejecutan en un proceso del sistema en segundo plano, deben ejecutarse rápidamente con un mínimo de CPU y e/s consumidos para cumplir los requisitos de rendimiento del sistema.

Por lo tanto, los desarrolladores deben escribir estos complementos con experiencia en la creación de código de nivel de sistema.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   En el caso de los orígenes de datos que necesitan usar el objeto de vista de carpeta del sistema predeterminado del shell (DefView), vea [implementar una vista de carpeta, una](../lwef/nse-folderview.md)función de [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) y [**SFV \_ crear**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) la estructura. Los orígenes de datos que utilizan el objeto de vista de carpeta del sistema predeterminado del shell (DefView) deben implementar el siguiente conjunto de interfaces: [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)y (opcionalmente) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Si la implementación de **IShellFolder** no usa **SHCreateShellFolderView** para crear el DefView, el objeto de vista de Shell puede necesitar [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview).
-   [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) es la interfaz principal para los consumidores del origen de datos de Shell conocido como DBFolder. Para obtener más información sobre DBFolder, vea la descripción de la \_ constante Str Parse \_ with \_ Properties en [**BIND context String Keys**](../shell/str-constants.md). Vea también [matrices de asociación](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) y [**IPropertySystem:: GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obtener información sobre OLE DB, consulte [información general sobre la programación de OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Para obtener información sobre el proveedor de datos de .NET Framework para OLE DB, consulte la documentación del [espacio de nombres System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .
-   En el caso de los paneles de mensajes compatibles con la comunidad en tecnologías de búsqueda, vea [Windows: Search forums](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) en MSDN.
-   Para ver ejemplos de código relacionados, consulte [ejemplos de código de Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Idiomas admitidos por búsqueda de Windows](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Guía del desarrollador de Windows Search](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 

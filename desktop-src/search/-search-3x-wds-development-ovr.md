---
description: Para indexar el contenido y las propiedades de nuevos formatos de archivo y almacenes de datos, Microsoft Windows Search debe ampliarse con complementos.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search como plataforma de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a660467aa5fe8b76db2f72704e59a3f4677efbdeb9c354a04a6887d9a9d4a8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681221"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search como plataforma de desarrollo

Para indexar el contenido y las propiedades de nuevos formatos de archivo y almacenes de datos, Microsoft Windows Search debe ampliarse con complementos.

Para que un desarrollador de terceros de nuevos formatos de archivo y almacenes de datos pueda obtener esos formatos y almacenes para que aparezcan en los resultados de la consulta en Windows Explorer, el desarrollador debe hacer lo siguiente:

-   Implemente un origen de datos de Shell para ampliar el espacio de nombres de Shell.
-   Exponga los elementos de un almacén de datos (si va a agregar un nuevo almacén de datos, porque tendría que indexarse).
-   Desarrolle un controlador de protocolo para que Windows Search pueda acceder a los datos para la indexación.

Este tema se organiza de la siguiente manera:

-   [Introducción](#getting-started)
-   [Introducción a los escenarios de desarrollo de búsqueda](#overview-of-search-development-scenarios)
    -   [Agregar un nuevo almacén de datos](#adding-a-new-data-store)
    -   [Agregar un nuevo formato de archivo](#adding-a-new-file-format)
    -   [Consumo de Windows resultados de la búsqueda](#consuming-windows-search-results)
-   [Información general de los controladores](#overview-of-handlers)
-   [Instrucciones del instalador del complemento](#add-in-installer-guidelines)
-   [Nota para implementadores](#note-to-implementers)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="getting-started"></a>Introducción

Antes de empezar a crear una Windows Search, recuerde que la manera preferida de hacerlo es a través de un origen de datos de Shell. Un origen de datos de Shell amplía el espacio de nombres de Shell y expone los elementos de un almacén de datos. A continuación, los elementos del almacén de datos se pueden indexar mediante el Windows Search mediante un controlador de protocolo. Este enfoque indirecto para acceder a Windows Search mediante la implementación de un origen de datos de Shell es preferible porque proporciona acceso a la funcionalidad completa de Shell. Hacerlo de esta manera garantiza una experiencia de usuario razonable.

Si desea que los resultados de la consulta aparezcan en Windows Explorer, debe implementar un origen de datos de Shell para poder crear un controlador de protocolo para ampliar el índice. Sin embargo, si todas las consultas se van a realizar mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, se prefiere un espacio de nombres de Shell, pero no es necesario.

Se requiere un controlador de protocolo para Windows obtener conocimientos sobre el contenido del archivo, como elementos de bases de datos o tipos de archivo personalizados. Aunque Windows Search puede indexar el nombre y las propiedades del archivo, Windows no tiene conocimiento del contenido del archivo. Como resultado, estos elementos no se pueden indexar ni exponer en el shell Windows Shell. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando lograr, vea [Información general de los controladores.](#overview-of-handlers)

## <a name="overview-of-search-development-scenarios"></a>Introducción a los escenarios de desarrollo de búsqueda

Los escenarios de desarrollo más comunes en Windows Search son:

-   [Adición de un nuevo almacén de datos](#adding-a-new-data-store)
-   [Agregar un nuevo formato de archivo](#adding-a-new-file-format)
-   [Consumo de resultados Windows search](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Agregar un nuevo almacén de datos

Solo necesita un almacén de datos de Shell Windows search si va a agregar un nuevo almacén de datos para indexar. Un almacén de datos es un repositorio de datos que se puede exponer al modelo de programación de Shell como contenedor mediante un origen de datos de Shell. Los elementos de un almacén de datos se pueden indexar mediante el sistema Windows Search mediante un controlador de protocolo. El controlador de protocolo implementa el protocolo para acceder a un origen de contenido en su formato nativo. Las [**interfaces ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) se usan para implementar un controlador de protocolo personalizado para expandir los orígenes de datos que se pueden indexar. Para obtener información sobre cómo crear un origen de datos de Shell, vea [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Agregar un nuevo formato de archivo

Si agrega un nuevo formato de archivo personalizado, debe desarrollar un controlador de filtros o un controlador de propiedades, pero no ambos. Un filtro es una implementación de la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) Abre archivos de un tipo de archivo determinado y filtra propiedades y fragmentos de texto para el indexador. Los filtros están asociados a tipos de archivo, como se indica en extensiones de nombre de archivo, tipos MIME o identificadores de clase (CLSID). Aunque un filtro puede controlar varios tipos de archivo, cada tipo de archivo funciona con un solo filtro.

Un controlador de propiedades traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que pueden acceder Windows Explorer, Windows Search y otras aplicaciones. A continuación, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer propiedades en y desde un archivo. Los datos traducidos incluyen la vista de detalles, información sobre información, el panel de detalles, las páginas de propiedades, etc. Cada controlador de propiedades está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo. Necesita un controlador de propiedades para hacer lo siguiente:

-   Mostrar propiedades de elementos no indexados en la interfaz de usuario.
-   Admite la escritura de propiedades.

### <a name="consuming-windows-search-results"></a>Consumo de Windows resultados de la búsqueda

En las secciones siguientes se describen varias maneras de consumir Windows resultados de búsqueda:

-   [Consultar datos](#querying-data)
-   [Consulta de almacenes de datos remotos (Búsqueda federada)](#querying-remote-data-stores-federated-search)
-   [Indexación de archivos y elementos](#indexing-files-and-items)
-   [Indexación de un almacén de datos](#indexing-a-data-store)
-   [Administración del proceso de indexación](#managing-the-indexing-process)
-   [Integración del sistema Windows propiedades con Windows Search](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Consulta de datos

Los desarrolladores que escriben aplicaciones sobre el sistema de propiedades Windows search y Windows combinados pueden acceder a archivos y elementos independientemente del tipo de aplicación o archivo. Hay dos maneras de que las aplicaciones accedan a los datos del indexador:

-   Las aplicaciones se comunican directamente con OLE DB mediante el envío de consultas Windows Search Lenguaje de consulta estructurado (SQL) al proveedor de Windows Search OLE DB para recuperar los resultados. Las consultas se pueden construir manualmente o mediante la interfaz [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para generar el SQL a partir de palabras clave de búsqueda y la sintaxis de consulta avanzada (AQS).
-   Las aplicaciones funcionan a través de la capa de Shell. La ventaja de la capa de Shell es que también admite otros orígenes, como grep. Sin embargo, la desventaja es que no todas las características del indexador están disponibles.

Otra opción es usar los protocolos search-ms:// y search://, que ejecutan búsquedas basadas en URL que se representan a través de Windows Explorer. Esta opción permite el desarrollo más ligero, pero no devuelve resultados ni selecciones de usuario desde la vista de resultados a la aplicación que realiza la llamada. Además, al igual que otros protocolos, las aplicaciones de búsqueda de terceros pueden asumir los protocolos search-ms:// y search:// si las aplicaciones se ajustan al conjunto de características necesario. Para obtener más información sobre las consultas, vea [Querying Process in Windows Search](querying-process--windows-search-.md) and [Querying the Index Programmatically](-search-3x-wds-qryidx-overview.md).

### <a name="querying-remote-data-stores-federated-search"></a>Consulta de almacenes de datos remotos (búsqueda federada)

En Windows 7 y versiones posteriores, la búsqueda federada ofrece un nuevo proveedor de búsqueda que consulta almacenes de datos remotos a través de servidores [web, a](https://github.com/dewitt/opensearch) través del protocolo OpenSearch, y enumera los resultados como fuentes RSS o Atom XML. Los conectores de búsqueda son uniones de espacio de nombres que simulan el comportamiento de las carpetas mediante un proveedor de búsqueda. Para obtener más información sobre la federación de búsqueda en almacenes de datos remotos Windows 7, vea Búsqueda federada [en Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indexación de archivos y elementos

El contenido que se indexa se basa en los tipos de archivo y datos admitidos a través de complementos incluidos con Windows Search y las reglas de inclusión y exclusión predeterminadas para las carpetas del sistema de archivos. Por ejemplo, los filtros incluidos en Búsqueda de ventanas admiten más de 200 tipos comunes de datos, incluidos documentos de Microsoft Office, correo electrónico de Microsoft Outlook (junto con el controlador de protocolo SMTP), archivos de texto sin formato, HTML y muchos más. Para obtener una lista completa de los tipos de archivo admitidos de forma nativa, vea [Qué se incluye en el índice](-search-3x-wds-included-in-index.md).

El índice se puede extender con controladores de propiedades y filtros para exponer el contenido y las propiedades de los nuevos formatos de archivo al índice y Windows Explorer. Los filtros son una implementación de la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) Hay dos tipos de filtros: uno que interactúa con elementos individuales como archivos y otro que interactúa con contenedores como carpetas. Los filtros son multipropósito, ya que admiten la fragmentación de datos, el contenido de texto, algunas propiedades y varios idiomas.

Por el contrario, los controladores de propiedades tienen un propósito más específico: exponer las propiedades de tipos de archivo específicos identificados por las extensiones de nombre de archivo. Un controlador de propiedades para un tipo de archivo puede habilitar obtener y establecer propiedades, y puede enumerar las propiedades asociadas a ese tipo de archivo. A diferencia de los filtros, los controladores de propiedades no admiten el envío de datos o contenido de texto, y los controladores de propiedades no tienen ninguna manera de indicar en qué idioma se encuentra una propiedad de texto a menos que admitan la escritura de propiedades.

### <a name="indexing-a-data-store"></a>Indexación de un almacén de datos

El índice se puede ampliar con controladores de protocolo para proporcionar acceso a almacenes de datos propietarios. Por ejemplo, los archivos y elementos contenidos en almacenes de datos que no son del sistema de archivos (como bases de datos y almacenes de correo electrónico) requieren un controlador de protocolo para asignar desde una dirección URL a una secuencia. Los controladores de protocolo también pueden determinar opcionalmente los filtros correctos que se usarán para extraer información de una secuencia. Los filtros enumeran las direcciones URL del almacén de datos. A continuación, los elementos se indexa individualmente con el filtro o el controlador de propiedades adecuados. Para obtener más información, [vea Extender el índice](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Administración del proceso de indexación

Los desarrolladores de aplicaciones pueden controlar el ámbito y la frecuencia de Windows search mediante varias interfaces de administración. Estas interfaces incluyen funcionalidad para agregar y quitar los directorios que el indexador examina en busca de cambios, notificar manualmente al índice los cambios en los datos, comprobar el estado del indexador y forzar la nueva indexación de algunos o todos los datos. Para obtener más información, vea [Administración del índice](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>Integración del sistema Windows propiedades con Windows Search

El Windows de propiedades es un sistema extensible de lectura y escritura de definiciones de datos que proporciona una manera uniforme de expresar metadatos sobre elementos de Shell. El Windows de propiedades de Windows Vista y versiones posteriores le permite almacenar y recuperar metadatos para elementos de Shell. Un elemento de Shell es cualquier elemento de contenido, como un archivo, una carpeta, un correo electrónico o un contacto. Una propiedad es un fragmento individual de metadatos asociado a un elemento de Shell. Los valores de propiedad se expresan [**como una estructura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Se incluye una amplia lista de propiedades comunes para varios tipos de elementos comunes, como fotos, música, documentos, mensajes, contactos y archivos. Los desarrolladores también pueden presentar sus propias propiedades a la plataforma si ninguna propiedad existente satisface sus necesidades. Para obtener más información sobre la integración de aplicaciones con el Windows de propiedades, vea [Developing Property Handlers](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Información general de los controladores

Un controlador es un objeto de Modelo de objetos componentes (COM) que proporciona funcionalidad para un elemento de Shell. La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos. Por ejemplo, la carpeta del sistema de archivos usa el sistema de asociación para buscar los controladores de un tipo de archivo determinado. Se requiere un controlador específico para cada tipo de archivo. Se requiere un controlador de filtro para el tipo de archivo .pdf Adobe Acrobat; por ejemplo, se requiere otro controlador de filtro para el formato de archivo .doc, etc.

Los distintos controladores tienen algo de comúnidad. En Windows Vista y versiones posteriores, todos los controladores deben usar una de las interfaces siguientes para inicializar el controlador: [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

En la tabla siguiente se enumeran las tareas de desarrollador de alto nivel, el tipo de controlador necesario para cada tarea y se proporciona un vínculo a información conceptual sobre cómo realizar cada tarea.



| Tarea                                                                                                                                                            | Controlador                          | Información conceptual                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acceso a las propiedades de un archivo para la indexación                                                                                                                 | Controlador de propiedades                 | [Desarrollar controladores de propiedades](-search-3x-wds-extidx-propertyhandlers.md)<br/> [Propiedades definidas por el sistema para formatos de archivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Agregar formatos del Portapapeles para el objeto de datos ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) de un elemento (los objetos de datos se usan en escenarios de arrastrar y colocar y copiar y pegar). | Controlador de objeto de datos              | [Crear controladores de datos](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Agregar verbos para un elemento que se muestran normalmente en un menú contextual                                                                                         | Controlador de menú contextual            | [Crear controladores de menú contextual](../shell/context-menu-handlers.md)<br/> [Personalizar un menú contextual mediante verbos dinámicos](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Asociación de un tipo de archivo con un icono específico                                                                                                                    | Controlador de iconos                     | [Crear controladores de iconos](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Creación de hojas de propiedades con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo                                                          | Controlador de la hoja de propiedades           | [Controladores de hoja de propiedades](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Habilitación de un tipo de elemento para admitir escenarios de arrastrar y colocar y copiar y pegar                                                                                         | Controlador de colocación                     | [Transferencia de objetos de shell con arrastrar y colocar y el Portapapeles](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Extracción de fragmentos de texto y propiedades de documento para la indexación                                                                                                  | Controlador de filtro                   | [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indexación de un nuevo tipo de archivo                                                                                                                                        | Controlador de filtro, controlador de propiedades | [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)<br/> [Desarrollar controladores de propiedades](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indexación del contenido de un almacén de datos                                                                                                                           | Controlador de protocolo                 | [Desarrollo de controladores de protocolo](-search-3x-wds-phaddins.md)                                                                                                                                            |
| Vista previa de una vista simplificada del elemento shell en el panel de vista previa Windows Explorer                                                                             | Controlador de vista previa                  | [Controladores de vista previa](../shell/preview-handlers.md)                                                                                                                                                             |
| Proporcionar texto emergente cuando un mouse mantiene el mouse sobre un objeto de interfaz de usuario                                                                                                      | Controlador de recuadro informativo                  | [Crear controladores de extensión de shell](../shell/handlers.md) (personalización de información)                                                                                                                            |
| Proporcionar una imagen estática para representar un elemento de Shell                                                                                                              | Controlador de miniaturas                | [Controladores de miniaturas](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

En la tabla siguiente se enumeran los controladores y las interfaces para implementar cada tipo de controlador.



| Controlador                | Interfaces                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Controlador de colocación           | [**IDropTarget,**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) [**IDropTargetHelper,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Controlador de objeto de datos    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Controlador de filtro         | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Controlador de iconos           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Opcional: [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| Controlador de recuadro informativo        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Controlador de vista previa        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Controlador de propiedades       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Controlador de protocolo       | [**IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) [**ISearchProtocol,**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Opcional: [**ISearchProtocol2,**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) [**IUrlAccessor2,**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2) [**IUrlAccessor3,**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3) [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Controlador de la hoja de propiedades | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Controlador de menú contextual  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Controlador de miniaturas      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> A veces, un controlador de propiedades se denomina controlador de metadatos. Un origen de datos de Shell se conoce a veces como una extensión de espacio de nombres de Shell. Un controlador de tipo de archivo se conoce a veces como un controlador de extensiones de Shell o una extensión de Shell.

 

Para obtener más información sobre cómo crear controladores, vea [Creating Shell Extension Handlers](../shell/handlers.md). Para obtener más información sobre las propiedades, [vea Windows Property System](../properties/windows-properties-system.md).

## <a name="add-in-installer-guidelines"></a>Instrucciones del instalador del complemento

Use las siguientes directrices al crear un instalador de complementos:

-   El instalador debe usar el instalador EXE o MSI.
-   Se deben proporcionar notas de la versión.
-   Se **debe crear una entrada Agregar** o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.
-   Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito un complemento anterior, el usuario debe poder restaurar la funcionalidad del complemento anterior y volver a convertirla en el complemento predeterminado para ese tipo de archivo o almacén.

## <a name="note-to-implementers"></a>Nota para los implementadores

Antes de crear un controlador de filtro o propiedad, los desarrolladores deben tener en cuenta lo siguiente:

-   Estos controladores son extensiones en proceso que se cargan en procesos que no se controlan, como el proceso de demonio de filtro, Windows Explorer (búsqueda grep) y hosts de terceros como Windows Mail).
-   Debe escribir código seguro lo suficientemente sólido como para controlar formas arbitrariamente dañadas del formato de archivo que se crearon para atacar el sistema.
-   El complemento no debe filtrar recursos que produzcan problemas para los procesos del host.
-   El complemento no debe bloquearse, ya que esto también bloqueará los procesos de host y ralentizará el proceso de filtrado.
-   Dado que estos controladores se ejecutan en un proceso del sistema en segundo plano, deben realizarse rápidamente con un mínimo de CPU y E/S consumidas para cumplir los requisitos de rendimiento del sistema.

Por lo tanto, estos complementos deben ser escritos por desarrolladores con experiencia en la creación de código de nivel de sistema.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo crear un origen de datos de Shell, vea [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   Para los orígenes de datos que necesitan usar el objeto de vista de carpetas del sistema predeterminado (DefView) de Shell, vea [Implementación](../lwef/nse-folderview.md)de una vista de carpeta, función [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) y estructura [**SFV \_ CREATE.**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) Los orígenes de datos que usan el objeto de vista de carpetas del sistema predeterminado (DefView) de Shell deben implementar el siguiente conjunto de interfaces: [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) [**IPersistFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)e (opcionalmente) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Si la **implementación de IShellFolder** no usa **SHCreateShellFolderView para** crear defView, es posible que el objeto de vista shell necesite [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview).
-   [**ISearchFolderItemFactory es**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) la interfaz principal para los consumidores del origen de datos de Shell conocido como DBFolder. Para obtener más información sobre DBFolder, vea la descripción de la constante STR \_ PARSE \_ WITH PROPERTIES en Enlazar claves de cadena de \_ [**contexto**](../shell/str-constants.md). Vea también [Matrices de asociación](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) [**e IPropertySystem::GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obtener información sobre OLE DB, vea [información general OLE DB programación de aplicaciones.](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx) Para obtener información sobre el .NET Framework de datos para OLE DB, consulte la documentación del espacio de nombres [System.Data.OleDb.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1)
-   Para ver los paneles de mensajes admitidos por la comunidad en las tecnologías de búsqueda, [Windows: Foros de búsqueda](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) en MSDN.
-   Para obtener ejemplos de código relacionados, [vea Windows ejemplos de código de búsqueda.](-search-samples-ovw.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Idiomas admitidos por Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Windows Guía del desarrollador de búsqueda](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 

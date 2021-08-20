---
description: Windows Search es una plataforma de búsqueda de escritorio que tiene funcionalidades de búsqueda instantánea para los tipos de archivo y tipos de datos más comunes, y los desarrolladores de terceros pueden ampliar estas funcionalidades a nuevos tipos de archivo y tipos de datos.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Información general sobre Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a38b757936e9f960d71ac5d1a9759208b4b580af2526e23d4e5d88cde41a206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033133"
---
# <a name="windows-search-overview"></a>Información general sobre Windows Search

Windows Search es una plataforma de búsqueda de escritorio que tiene funcionalidades de búsqueda instantánea para los tipos de archivo y tipos de datos más comunes, y los desarrolladores de terceros pueden ampliar estas funcionalidades a nuevos tipos de archivo y tipos de datos.

Este tema se organiza de la siguiente manera:

-   [Introducción](#introduction)
    -   [Servicio de Windows Search](#windows-search-service)
    -   [Plataforma de desarrollo](#development-platform)
    -   [Interfaz de usuario](#user-interface)
-   [Requisitos técnicos previos](#technical-prerequisites)
    -   [Descarga y contenido del SDK](#sdk-download-and-contents)
-   [Windows Documentación del SDK de Búsqueda](#windows-search-sdk-documentation)
-   [Historial de la Windows búsqueda](#history-of-windows-search)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Windows Search es un componente estándar de Windows 7 y Windows Vista, y está habilitado de forma predeterminada. Windows Search reemplaza Windows Desktop Search (WDS), que estaba disponible como complemento para Windows XP y Windows Server 2003.

Windows La búsqueda se compone de tres componentes:

-   [Windows Search Service](#windows-search-service) (WSS)
-   [Plataforma de desarrollo](#development-platform)
-   [Interfaz de usuario](#user-interface)

### <a name="windows-search-service"></a>Servicio de Windows Search

El WSS organiza las características extraídas de una colección de documentos. El Windows Search Protocol permite a un cliente comunicarse con un servidor que hospeda un WSS, tanto para emitir consultas como para permitir que un administrador administre el servidor de indexación. Al procesar archivos, WSS analiza un conjunto de documentos, extrae información útil y, a continuación, organiza la información extraída para que las propiedades de esos documentos se puedan devolver eficazmente en respuesta a las consultas.

Una colección de documentos que se pueden consultar consta de un catálogo, que es la unidad de organización de nivel superior en Windows Search. Un catálogo representa un conjunto de documentos indexados que se pueden consultar. Un catálogo consta de una tabla de propiedades con el texto o el valor y la ubicación (configuración regional) correspondiente almacenada en columnas de la tabla. Cada fila de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada columna de la tabla corresponde a una propiedad . Un catálogo puede contener un índice invertido (para la coincidencia rápida de palabras) y una caché de propiedades (para la recuperación rápida de valores de propiedad).

El proceso de indexador se implementa como un servicio de Windows que se ejecuta en la cuenta LocalSystem y siempre se ejecuta para todos los usuarios (incluso si no hay ningún usuario conectado), lo que permite a Windows Search realizar lo siguiente:

-   Mantenga un índice que se comparta entre todos los usuarios.
-   Mantenga restricciones de seguridad en el acceso al contenido.
-   Procesar consultas remotas desde equipos cliente en la red.

La servicio Search está diseñada para proteger la experiencia del usuario y el rendimiento del sistema al indexar. Las condiciones siguientes hacen que el servicio limite o pause la indexación:

-   Uso elevado de CPU por procesos no relacionados con la búsqueda.
-   Alta tasa de E/S del sistema, incluidas las lecturas y escrituras de archivos, la E/S de caché de archivos y archivos de página, y la E/S de archivo asignada.
-   Disponibilidad de memoria baja.
-   Baja duración de la batería.
-   Poco espacio en disco en la unidad que almacena el índice.

### <a name="development-platform"></a>Plataforma de desarrollo

La manera preferida de acceder a las API de búsqueda y crear Windows Search es a través de un origen de datos de Shell. Un origen de datos de Shell es un componente que se usa para ampliar el espacio de nombres de Shell y exponer elementos en un almacén de datos. Un almacén de datos es un repositorio de datos. Un almacén de datos se puede exponer al modelo de programación de Shell como un contenedor que usa un origen de datos de Shell. Los elementos de un almacén de datos se pueden indexar mediante el sistema Windows Search mediante un controlador de protocolo.

Por ejemplo, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) es un componente que puede crear instancias del origen de datos de la carpeta de búsqueda, que es una especie de origen de datos "virtual" proporcionado por el Shell que puede ejecutar consultas sobre otros orígenes de datos en el espacio de nombres de Shell y enumerar los resultados. Puede hacerlo mediante el indexador o enumerando e inspeccionando manualmente los elementos de los ámbitos especificados. Esta interfaz permite configurar los parámetros de la búsqueda mediante métodos que crean y modifican carpetas de búsqueda. Si no se llama a los métodos de esta interfaz, se usan valores predeterminados en su lugar.

Se prefiere Windows la funcionalidad de búsqueda de Windows a través del modelo de datos de Shell, ya que proporciona acceso a la funcionalidad completa de Shell en el nivel del modelo de datos de Shell. Por ejemplo, puede establecer el ámbito de una búsqueda en una biblioteca (que es una característica disponible en Windows 7 y versiones posteriores) para usar las carpetas de biblioteca como ámbito de la consulta. Windows La búsqueda agrega los resultados de búsqueda de esas ubicaciones si se encuentran en índices diferentes (si las carpetas están en equipos diferentes). La capa de datos de Shell también crea una vista más completa de las propiedades de los elementos, sintetizando algunos valores de propiedad. También proporciona acceso a las características de búsqueda de almacenes de datos que no están indexados por Windows Search. Por ejemplo, puede buscar en dispositivos de almacenamiento de Bus serie universal (USB), dispositivo portátil que use el protocolo MTP o un servidor protocolo de transferencia de archivos (FTP) a través de los orígenes de datos de Shell que proporcionan acceso a esos sistemas de almacenamiento. Esto garantiza una mejor experiencia del usuario.

Windows La búsqueda tiene una caché de valores de propiedad que se usa en la implementación de Windows Search Service (WSS). Estos valores de propiedad se pueden consultar mediante programación mediante el proveedor de Windows Search OLE DB o mediante [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa los elementos de los resultados de búsqueda y las vistas basadas en consultas. Windows A continuación, search recopila y almacena las propiedades emitidas por controladores de filtro o controladores de propiedades cuando se indexa un elemento como un documento de Word. Este almacén se descarta y se recompila cuando se recompila el índice.

Los desarrolladores de terceros pueden crear aplicaciones que consumen los datos del índice a través de consultas mediante programación y pueden ampliar los datos del índice para los tipos de archivo y elemento personalizados que se indexarán mediante Windows Search. Si desea mostrar los resultados de la consulta en Windows Explorer, debe implementar un origen de datos de Shell para poder crear un controlador de protocolo para ampliar el índice. Sin embargo, si todas las consultas son mediante programación (a través de OLE DB por ejemplo) e interpretadas por el código de la aplicación en lugar del shell, se prefiere un espacio de nombres de Shell, pero no es necesario.

Se necesita un controlador de protocolo para Windows obtener información sobre el contenido del archivo, como elementos de bases de datos o tipos de archivo personalizados. Aunque Windows Search puede indexar el nombre y las propiedades del archivo, Windows no tiene información sobre el contenido del archivo. Como resultado, estos elementos no se pueden indexar ni exponer en el shell Windows shell. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando lograr, vea "Información general de los controladores" en [Windows Search como](-search-3x-wds-development-ovr.md)plataforma de desarrollo .

> [!Note]  
> Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. A veces, un controlador se conoce como una extensión de Shell o un controlador de extensiones de Shell.

 

### <a name="user-interface"></a>Interfaz de usuario

En Windows Vista y versiones posteriores, Windows Search se integra en todas las ventanas de Windows Explorer para obtener acceso instantáneo a la búsqueda. Esto permite a los usuarios buscar rápidamente archivos y elementos por nombre de archivo, propiedades y contenido de texto completo. Los resultados también se pueden filtrar aún más para refinar la búsqueda. Estas son algunas características más de Windows Search:

-   Un cuadro de búsqueda instantánea en cada ventana permite el filtrado instantáneo de todos los elementos actualmente en la vista. Los cuadros de búsqueda instantánea aparecen en la menú Inicio para buscar programas o archivos y en la esquina superior derecha de todas las ventanas de Windows Explorer para filtrar los resultados mostrados. La búsqueda instantánea también se integra en otras características Windows, como Reproductor de Windows Media, para buscar archivos relacionados.
-   Los documentos se pueden etiquetar con palabras clave para agruparlos por criterios personalizados definidos por el usuario. Las etiquetas son elementos de metadatos asignados por el usuario o las aplicaciones para facilitar la búsqueda de archivos basados en palabras clave que pueden no estar en el nombre o el contenido del elemento. Por ejemplo, un conjunto de imágenes podría etiquetarse como "Arizona Vacation 2009" para recuperar rápidamente más adelante buscando cualquiera de las palabras incluidas.
-   Los encabezados de columna mejorados Windows las vistas del Explorador permiten ordenar y agrupar documentos de maneras diferentes. Por ejemplo, los archivos se pueden ordenar según el nombre, la fecha de modificación, el tipo, el tamaño y las etiquetas. Los documentos también se pueden agrupar según cualquiera de estas propiedades y cada grupo se puede filtrar (ocultar o mostrar) según sea necesario.
-   Los documentos se pueden apilar según el nombre, la fecha de modificación, el tipo, el tamaño y las etiquetas. Las pilas incluyen todos los documentos que tienen la propiedad especificada y se encuentran dentro de cualquier subcarpeta de la carpeta seleccionada.
-   Las búsquedas se pueden guardar (para  recuperarse más adelante) haciendo clic en el botón Guardar búsqueda en el panel de búsqueda Windows Explorador. Los resultados se volverán a llenar dinámicamente en función de los criterios originales cuando se abra la búsqueda guardada. Para obtener instrucciones, consulte [Guardar los resultados de la búsqueda.](https://windows.microsoft.com/windows-vista/Save-your-search-results)
-   Los controladores de vista previa y los controladores de miniaturas permiten a los usuarios obtener una vista previa de los documentos en Windows Explorer sin tener que abrir la aplicación que los creó.

## <a name="technical-prerequisites"></a>Requisitos técnicos previos

Antes de empezar a leer la documentación Windows SDK de Search, debe tener un conocimiento fundamental de los siguientes conceptos:

-   Cómo implementar un origen de datos de Shell.
-   Cómo implementar un controlador.
-   Cómo trabajar en código nativo.

Un origen de datos de Shell es un componente que se usa para ampliar el espacio de nombres de Shell y exponer elementos en un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Un controlador es un objeto de Modelo de objetos componentes (COM) que proporciona funcionalidad para un elemento de Shell. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando lograr, vea "Información general de los controladores" en [Windows Search como](-search-3x-wds-development-ovr.md)plataforma de desarrollo .

Para obtener más información sobre el ensamblado de interoperabilidad del SDK de Windows Search para trabajar con objetos COM expuestos por Windows Search y otros programas que usan código administrado, consulte Uso de código administrado con datos de [shell y Windows Search](-search-3x-wds-managed-code.md). Sin embargo, tenga en cuenta que los filtros, los controladores de propiedades y los controladores de protocolo deben escribirse en código nativo. Esto se debe a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos. Los desarrolladores que no están nuevos en C++ pueden empezar a trabajar con el Centro [Visual C++ desarrolladores](https://msdn.microsoft.com/vstudio//default.aspx) y Windows [Desarrollo Tareas iniciales](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Descarga y contenido del SDK

Además de cumplir los requisitos previos técnicos enumerados, también debe descargar el SDK de [Windows para](https://msdn.microsoft.com/windowsvista/bb980924.aspx) obtener las bibliotecas Windows Search. Los [Windows SDK de Search contienen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) ejemplos de código útiles y un ensamblado de interoperabilidad para desarrollar con código administrado. Para obtener más información sobre el uso de los ejemplos de código, [vea Windows Buscar ejemplos de código](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Windows Documentación del SDK de Search

El contenido de la documentación Windows SDK de Search es el siguiente:

-   [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)

    Describe los principales escenarios de desarrollo en Windows Search. Proporciona una lista de los controladores identificados por el escenario de desarrollo que está intentando lograr, las directrices del instalador del complemento y las notas de implementación.

-   [Windows Guía del desarrollador de búsqueda](-search-developers-guide-entry-page.md)

    Proporciona explicaciones para [administrar el índice](-search-3x-wds-mngidx-overview.md), consultar el índice mediante programación, [extender](-search-3x-wds-extidx-overview.md)el índice y extender recursos [de lenguaje.](extending-language-resources-in-windows-search.md) [](-search-3x-wds-qryidx-overview.md)

-   [Windows Referencia de búsqueda](-search-reference-entry-page.md)

    Documenta las siguientes categorías de [interfaces](-search-protocol-handlers-interfaces-entry-page.md)Windows Search: Controladores de protocolo, Consulta [de](-search-querying-interfaces-entry-page.md), [Ámbito](-search-crawl-scope-interfaces-entry-page.md)de [rastreo,](-search-data-addins-interfaces-entry-page.md)Complementos de [datos,](-search-index-mgt-interfaces-entry-page.md)Administración de índices y [Notificaciones](-search-notifications-interfaces-entry-page.md). La documentación de referencia también incluye [constantes y enumeraciones,](-search-constants-and-enumerations-entry-page.md) [estructuras,](-search-structures-entry-page.md)asignaciones [de propiedades](-search-3x-wds-propertymappings.md)y el formato de archivo de [búsqueda guardado.](-search-savedsearchfileformat.md)

-   [Windows Ejemplos de código de búsqueda](-search-samples-ovw.md)

    Describe los ejemplos de código de Search API que están disponibles.

-   [Búsqueda federada en Windows](-search-federated-search-overview.md)

    Describe Windows 7 compatibilidad con la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch que permiten a los usuarios acceder a sus datos remotos e interactuar con ellos desde Windows Explorer.

-   [Tecnologías de búsqueda relacionadas](-search-3x-wds-sampleentry.md)

    Enumera las tecnologías relacionadas con Windows Search: Enterprise Search, SharePoint Enterprise Search y aplicaciones heredadas, como Windows Desktop Search 2.x y Platform SDK: Indexing Service.

-   [Windows Glosario de búsqueda](search-glossary.md)

    Define los términos esenciales usados en Windows search y shell.

## <a name="history-of-windows-search"></a>Historial de la Windows búsqueda

Windows Search reemplaza Windows Desktop Search (WDS), que estaba disponible como complemento para Windows XP y Windows Server 2003. WDS reemplazó el servicio de indexación heredado de versiones anteriores de Windows por mejoras en el rendimiento, la facilidad de uso y la extensibilidad. La nueva plataforma de desarrollo admite requisitos que generan un sistema más seguro y estable. Aunque la nueva plataforma de consulta no es compatible con Microsoft Windows Desktop Search (WDS) 2.x, los filtros y controladores de protocolo escritos para versiones anteriores de WDS se pueden actualizar para que funcionen con Windows Search. Windows Search también admite un nuevo sistema de propiedades. Para obtener información sobre los filtros, los controladores de propiedades y los controladores de protocolo, vea [Extender el índice](-search-3x-wds-extidx-overview.md).

Windows Search está integrado en Windows Vista y versiones posteriores, y está disponible como una actualización redistribuible de WDS 2.x, para admitir los siguientes sistemas operativos:

-   Versiones de 32 bits de Windows XP con Service Pack 2 (SP2).
-   Todas las versiones basadas en x64 de Windows XP.
-   Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores.
-   Todas las versiones basadas en x64 de Windows Server 2003.

Los sistemas que ejecutan estos sistemas operativos deben tener Windows Search para poder ejecutar aplicaciones escritas para Windows Search. Para obtener más información, vea el artículo de KB 917013: Descripción de [Windows Desktop Search 3.01 y Interfaz de usuario multilingüe Pack for Windows Desktop Search 3.01](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo crear un origen de datos de Shell, vea [Implementing the Basic Folder Object Interfaces](/previous-versions//bb776815(v=vs.85)).
-   Para obtener más información sobre [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) y el origen de datos de la carpeta de base de datos, vea la descripción de la constante STR PARSE WITH PROPERTIES en Enlazar claves \_ de cadena de \_ \_ [contexto](../shell/str-constants.md). Vea también [Matrices de asociación](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) [e IPropertySystem::GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obtener información sobre OLE DB, vea [información general OLE DB programación de aplicaciones.](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019) Para obtener información sobre el .NET Framework de datos para OLE DB, consulte la documentación del espacio de nombres [System.Data.OleDb.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true)
-   Para obtener información general sobre los controladores de tipos de archivo (también conocidos como controladores de extensión de Shell y controladores de búsqueda), vea [Windows Search como plataforma de desarrollo.](-search-3x-wds-development-ovr.md)
-   Para ver paneles de mensajes admitidos por la comunidad sobre las tecnologías de búsqueda, vea [Foro de MSDN: Windows desarrollo de búsqueda de escritorio.](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)
-   Para obtener ejemplos de código relacionados, [vea Windows ejemplos de código de búsqueda.](-search-samples-ovw.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Idiomas admitidos por Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 

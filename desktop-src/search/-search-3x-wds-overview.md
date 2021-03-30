---
description: Windows Search es una plataforma de búsqueda en el escritorio que tiene capacidades de búsqueda instantánea para la mayoría de los tipos de archivos y tipos de datos más comunes, y los desarrolladores de terceros pueden ampliar estas capacidades a nuevos tipos de archivos y tipos de datos.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Información general sobre Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907757"
---
# <a name="windows-search-overview"></a>Información general sobre Windows Search

Windows Search es una plataforma de búsqueda en el escritorio que tiene capacidades de búsqueda instantánea para la mayoría de los tipos de archivos y tipos de datos más comunes, y los desarrolladores de terceros pueden ampliar estas capacidades a nuevos tipos de archivos y tipos de datos.

Este tema se organiza de la siguiente manera:

-   [Introducción](#introduction)
    -   [Servicio de Windows Search](#windows-search-service)
    -   [Plataforma de desarrollo](#development-platform)
    -   [Interfaz de usuario](#user-interface)
-   [Requisitos técnicos previos](#technical-prerequisites)
    -   [Descarga y contenido del SDK](#sdk-download-and-contents)
-   [Documentación del SDK de Windows Search](#windows-search-sdk-documentation)
-   [Historial de Windows Search](#history-of-windows-search)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Windows Search es un componente estándar de Windows 7 y Windows Vista, y está habilitado de forma predeterminada. Windows Search reemplaza a la búsqueda de escritorio de Windows (WDS), que estaba disponible como complemento para Windows XP y Windows Server 2003.

Windows Search se compone de tres componentes:

-   [Windows Search Service](#windows-search-service) (WSS)
-   [Plataforma de desarrollo](#development-platform)
-   [Interfaz de usuario](#user-interface)

### <a name="windows-search-service"></a>Servicio de Windows Search

WSS organiza las características extraídas de una colección de documentos. El protocolo Windows Search permite a un cliente comunicarse con un servidor que hospeda un WSS, para emitir consultas y para permitir que un administrador administre el servidor de indexación. Al procesar archivos, WSS analiza un conjunto de documentos, extrae información útil y, a continuación, organiza la información extraída para que las propiedades de esos documentos puedan devolverse de forma eficaz en respuesta a las consultas.

Una colección de documentos que se pueden consultar se compone de un catálogo, que es la unidad de la organización de nivel superior de la organización en Windows Search. Un catálogo representa un conjunto de documentos indizados que se pueden consultar. Un catálogo consta de una tabla de propiedades con el texto o el valor y la ubicación correspondiente (configuración regional) almacenada en columnas de la tabla. Cada fila de la tabla corresponde a un documento independiente en el ámbito del catálogo y cada columna de la tabla corresponde a una propiedad. Un catálogo puede contener un índice invertido (para la coincidencia de palabras rápida) y una caché de propiedades (para recuperar rápidamente los valores de propiedad).

El proceso del indexador se implementa como un servicio de Windows que se ejecuta en la cuenta LocalSystem y siempre se ejecuta para todos los usuarios (incluso si ningún usuario ha iniciado sesión), lo que permite a Windows Search realizar lo siguiente:

-   Mantener un índice compartido entre todos los usuarios.
-   Mantener restricciones de seguridad en el acceso al contenido.
-   Procesar consultas remotas de equipos cliente en la red.

El servicio de búsqueda está diseñado para proteger la experiencia del usuario y el rendimiento del sistema al realizar la indexación. Las condiciones siguientes hacen que el servicio limite o PAUSE la indexación:

-   Uso intensivo de la CPU por parte de procesos no relacionados con la búsqueda.
-   Alta tasa de e/s del sistema, incluidas las lecturas y escrituras de archivos, el archivo de paginación y la e/s de archivos y la e/s de archivos asignada.
-   Disponibilidad de memoria baja.
-   Baja duración de la batería.
-   Espacio en disco insuficiente en la unidad donde se almacena el índice.

### <a name="development-platform"></a>Plataforma de desarrollo

La mejor manera de tener acceso a las API de búsqueda y crear aplicaciones de Windows Search es a través de un origen de datos de Shell. Un origen de datos de Shell es un componente que se utiliza para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos. Un almacén de datos es un repositorio de datos. Un almacén de datos se puede exponer en el modelo de programación de shell como un contenedor que usa un origen de datos de Shell. El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.

Por ejemplo, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) es un componente que puede crear instancias del origen de datos de la carpeta de búsqueda, que es un tipo de origen de datos "virtual" proporcionado por el shell que puede ejecutar consultas sobre otros orígenes de datos en el espacio de nombres del shell y enumerar los resultados. Puede hacerlo mediante el indizador o mediante la enumeración y inspección manuales de los elementos de los ámbitos especificados. Esta interfaz permite configurar los parámetros de la búsqueda mediante métodos que crean y modifican carpetas de búsqueda. Si no se llama a los métodos de esta interfaz, se usan los valores predeterminados en su lugar.

Se prefiere el acceso directo a la funcionalidad de búsqueda de Windows a través del modelo de datos de Shell, ya que proporciona acceso a toda la funcionalidad del shell en el nivel del modelo de datos de Shell. Por ejemplo, puede establecer el ámbito de una búsqueda en una biblioteca (que es una característica disponible en Windows 7 y versiones posteriores) para usar las carpetas de biblioteca como el ámbito de la consulta. Windows Search agrega entonces los resultados de la búsqueda desde esas ubicaciones si están en distintos índices (si las carpetas están en equipos diferentes). La capa de datos de Shell también crea una vista más completa de las propiedades de los elementos, sintetizando algunos valores de propiedad. También proporciona acceso a las características de búsqueda de almacenes de datos que no están indexados por Windows Search. Por ejemplo, puede buscar en los dispositivos de almacenamiento de bus serie universal (USB), en un dispositivo portátil que usa el protocolo MTP o en un servidor protocolo de transferencia de archivos (FTP) a través de los orígenes de datos de Shell que proporcionan acceso a esos sistemas de almacenamiento. Esto garantiza una mejor experiencia del usuario.

Windows Search tiene una memoria caché de valores de propiedad que se usa en la implementación de Windows Search Service (WSS). Estos valores de propiedad se pueden consultar mediante programación con el proveedor de OLE DB de Windows Search o a través de [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa los elementos de los resultados de la búsqueda y las vistas basadas en consultas. Windows Search recopila y almacena las propiedades que emiten los controladores de filtro o los controladores de propiedades cuando se indiza un elemento como un documento de Word. Este almacén se descarta y se vuelve a generar cuando se vuelve a generar el índice.

Los desarrolladores de terceros pueden crear aplicaciones que consuman los datos en el índice mediante consultas mediante programación y pueden extender los datos del índice para que los tipos de archivo y elemento personalizados los indexe Windows Search. Si desea mostrar los resultados de la consulta en el explorador de Windows, debe implementar un origen de datos de Shell antes de poder crear un controlador de protocolo para extender el índice. Sin embargo, si todas las consultas se realiza mediante programación (a través de OLE DB por ejemplo) y se interpretan mediante el código de la aplicación en lugar del shell, un espacio de nombres de Shell sigue siendo preferible, pero no es necesario.

Se requiere un controlador de protocolo para que Windows obtenga información sobre el contenido de los archivos, como los elementos de las bases de datos o los tipos de archivo personalizados. Aunque Windows Search puede indizar el nombre y las propiedades del archivo, Windows no tiene información sobre el contenido del archivo. Como resultado, estos elementos no se pueden indizar ni exponer en el shell de Windows. Al implementar un controlador de protocolo personalizado, puede exponer estos elementos. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando conseguir, vea "información general de los controladores" en [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md).

> [!Note]  
> Un origen de datos de Shell a veces se conoce como una extensión de espacio de nombres de Shell. Un controlador a veces se conoce como una extensión de shell o un controlador de extensión de Shell.

 

### <a name="user-interface"></a>Interfaz de usuario

En Windows Vista y versiones posteriores, Windows Search se integra en todas las ventanas del explorador de Windows para el acceso instantáneo a la búsqueda. Esto permite a los usuarios buscar rápidamente archivos y elementos por nombre de archivo, propiedades y contenido de texto completo. También se pueden filtrar los resultados para refinar la búsqueda. Estas son algunas características más de Windows Search:

-   Un cuadro de búsqueda instantánea en cada ventana permite el filtrado instantáneo de todos los elementos que están actualmente en la vista. Los cuadros de búsqueda instantánea aparecen en el menú Inicio para buscar programas o archivos y en la esquina superior derecha de todas las ventanas del explorador de Windows para filtrar los resultados mostrados. La búsqueda instantánea también se integra en otras características de Windows, como Windows Media Player, para buscar archivos relacionados.
-   Los documentos se pueden etiquetar con palabras clave para agruparlos por criterios personalizados definidos por el usuario. Las etiquetas son elementos de metadatos asignados por el usuario o las aplicaciones para facilitar la búsqueda de archivos basados en palabras clave que pueden no estar en el nombre o el contenido del elemento. Por ejemplo, un conjunto de imágenes puede etiquetarse como "Arizona vacaciones 2009" para recuperarse rápidamente más adelante buscando cualquiera de las palabras incluidas.
-   Los encabezados de columna mejorados en las vistas del explorador de Windows permiten ordenar y agrupar documentos de diferentes maneras. Por ejemplo, los archivos se pueden ordenar según el nombre, la fecha de modificación, el tipo, el tamaño y las etiquetas. Los documentos también se pueden agrupar de acuerdo con cualquiera de estas propiedades y cada grupo se puede filtrar (ocultar o mostrar) según sea necesario.
-   Los documentos se pueden apilar según el nombre, la fecha de modificación, el tipo, el tamaño y las etiquetas. Las pilas incluyen todos los documentos que tienen la propiedad especificada y se encuentran en cualquier subcarpeta de la carpeta seleccionada.
-   Las búsquedas se pueden guardar (para recuperarlas más adelante) haciendo clic en el botón **Guardar búsqueda** en el panel de búsqueda en el explorador de Windows. Los resultados se volverán a rellenar de forma dinámica en función de los criterios originales cuando se abra la búsqueda guardada. Para obtener instrucciones, consulte [guardar los resultados de la búsqueda](https://windows.microsoft.com/windows-vista/Save-your-search-results).
-   Los controladores de vista previa y los controladores de miniaturas permiten a los usuarios obtener una vista previa de los documentos en el explorador de Windows sin tener que abrir la aplicación que los creó.

## <a name="technical-prerequisites"></a>Requisitos técnicos previos

Antes de empezar a leer la documentación del SDK de Windows Search, debe tener un conocimiento fundamental de los conceptos siguientes:

-   Cómo implementar un origen de datos de Shell.
-   Cómo implementar un controlador.
-   Cómo trabajar en código nativo.

Un origen de datos de Shell es un componente que se utiliza para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos. En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell. Un controlador es un objeto COM (modelo de objetos componentes) que proporciona funcionalidad para un elemento de Shell. Para obtener una lista de los controladores identificados por el escenario de desarrollador que está intentando conseguir, vea "información general de los controladores" en [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md).

Para obtener más información acerca del ensamblado de interoperabilidad del SDK de Windows Search para trabajar con objetos COM expuestos por Windows Search y otros programas que usan código administrado, vea [usar código administrado con datos de Shell y Windows Search](-search-3x-wds-managed-code.md). Sin embargo, tenga en cuenta que los filtros, los controladores de propiedades y los controladores de protocolo deben escribirse en código nativo. Esto se debe a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos. Los desarrolladores que son nuevos en C++ pueden empezar a trabajar con el [Centro para desarrolladores de Visual C++](https://msdn.microsoft.com/vstudio//default.aspx) y el introducción de desarrollo de [Windows](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Descarga y contenido del SDK

Además de cumplir los requisitos técnicos de la lista, también debe descargar el [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para obtener las bibliotecas de Windows Search. Los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contienen ejemplos de código útiles y un ensamblado de interoperabilidad para desarrollar con código administrado. Para obtener más información sobre el uso de los ejemplos de código, vea [ejemplos de código de Windows Search](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Documentación del SDK de Windows Search

El contenido de la documentación del SDK de Windows Search es el siguiente:

-   [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)

    Describe los principales escenarios de desarrollo de Windows Search. Proporciona una lista de controladores identificados por el escenario de desarrollo que está intentando lograr, las directrices del instalador de complementos y las notas de implementación.

-   [Guía del desarrollador de Windows Search](-search-developers-guide-entry-page.md)

    Proporciona explicaciones para [administrar el índice](-search-3x-wds-mngidx-overview.md), [consultar el índice mediante programación](-search-3x-wds-qryidx-overview.md), [extender el índice](-search-3x-wds-extidx-overview.md)y [ampliar los recursos de lenguaje](extending-language-resources-in-windows-search.md).

-   [Referencia de Windows Search](-search-reference-entry-page.md)

    Documenta las siguientes categorías de interfaces de Windows Search: [controladores de protocolos](-search-protocol-handlers-interfaces-entry-page.md), [consultas](-search-querying-interfaces-entry-page.md), [ámbito de rastreo](-search-crawl-scope-interfaces-entry-page.md), [Complementos de datos](-search-data-addins-interfaces-entry-page.md), [Administración de índices](-search-index-mgt-interfaces-entry-page.md)y [notificaciones](-search-notifications-interfaces-entry-page.md). La documentación de referencia también incluye [constantes, enumeraciones](-search-constants-and-enumerations-entry-page.md), [estructuras](-search-structures-entry-page.md), [asignaciones de propiedades](-search-3x-wds-propertymappings.md)y el formato de archivo de [búsqueda guardado](-search-savedsearchfileformat.md).

-   [Ejemplos de código de Windows Search](-search-samples-ovw.md)

    Describe los ejemplos de código de la API de búsqueda que están disponibles.

-   [Búsqueda federada en Windows](-search-federated-search-overview.md)

    Describe la compatibilidad de Windows 7 con la Federación de búsqueda con almacenes de datos remotos mediante tecnologías de OpenSearch que permiten a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows.

-   [Tecnologías de búsqueda relacionadas](-search-3x-wds-sampleentry.md)

    Enumera las tecnologías relacionadas con Windows Search: Enterprise Search, SharePoint Enterprise Search y aplicaciones heredadas como Windows Desktop Search 2. x y Platform SDK: Indexing Service.

-   [Glosario de búsqueda de Windows](search-glossary.md)

    Define los términos esenciales que se usan en las tecnologías de Windows Search y Shell.

## <a name="history-of-windows-search"></a>Historial de Windows Search

Windows Search reemplaza a la búsqueda de escritorio de Windows (WDS), que estaba disponible como complemento para Windows XP y Windows Server 2003. WDS sustituyó el servicio de indexación heredado de versiones anteriores de Windows con mejoras en el rendimiento, la facilidad de uso y la extensibilidad. La nueva plataforma de desarrollo admite requisitos que producen un sistema más seguro y estable. Aunque la nueva plataforma de consulta no es compatible con Microsoft Windows Desktop Search (WDS) 2. x, los filtros y los controladores de protocolo escritos para versiones anteriores de WDS pueden actualizarse para que funcionen con Windows Search. Windows Search también admite un nuevo sistema de propiedades. Para obtener información sobre los filtros, los controladores de propiedades y los controladores de protocolo, vea [extender el índice](-search-3x-wds-extidx-overview.md).

Windows Search está integrado en Windows Vista y versiones posteriores, y está disponible como una actualización redistribuible de WDS 2. x, para admitir los siguientes sistemas operativos:

-   versiones de 32 bits de Windows XP con Service Pack 2 (SP2).
-   Todas las versiones basadas en x64 de Windows XP.
-   Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores.
-   Todas las versiones basadas en x64 de Windows Server 2003.

Los sistemas que ejecutan estos sistemas operativos deben tener instalado Windows Search para poder ejecutar aplicaciones escritas para Windows Search. Para obtener más información, vea [el artículo de KB 917013: Descripción de la búsqueda de escritorio de windows 3,01 y el paquete de interfaz de usuario multilingüe para Windows Desktop search 3,01](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions//bb776815(v=vs.85)).
-   Para obtener más información acerca de [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) y el origen de datos de la carpeta de base de datos, vea la descripción de la \_ constante Str Parse \_ with \_ Properties en [BIND context String Keys](../shell/str-constants.md). Vea también [matrices de asociación](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) y [IPropertySystem:: GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obtener información sobre OLE DB, consulte [información general sobre la programación de OLE DB](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019). Para obtener información sobre el proveedor de datos de .NET Framework para OLE DB, consulte la documentación del [espacio de nombres System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   Para obtener información general sobre los controladores de tipo de archivo (también conocidos como controladores de extensiones de Shell y controladores de búsqueda), consulte [Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md).
-   Para los paneles de mensajes compatibles con la comunidad sobre tecnologías de búsqueda, vea [Foro de MSDN: desarrollo de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Para ver ejemplos de código relacionados, consulte [ejemplos de código de Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Idiomas admitidos por búsqueda de Windows](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 

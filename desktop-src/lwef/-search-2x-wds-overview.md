---
title: Windows Búsqueda de escritorio 2.x
description: Comprenda Windows Desktop Search 2.x. Para Windows versiones posteriores a Windows XP y Windows Server 2003, use Windows Search en su lugar.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3298d668266d913a427c74f605435257c1a4cfba56fae82c809bd9127e7ecf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829105"
---
# <a name="windows-desktop-search-2x"></a>Windows Búsqueda de escritorio 2.x

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Se desaconseja encarecidamente el uso y el desarrollo para las versiones 2.x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).

WDS es un servicio de indexación y una plataforma que proporciona una búsqueda rápida de archivos y datos en diferentes orígenes y ubicaciones de datos. WDS ayuda a los usuarios y otras aplicaciones a encontrar casi cualquier cosa en sus equipos, mensajes de correo electrónico, citas de calendario, fotos, documentos y mucho más. Además, WDS puede devolver resultados de varios orígenes de datos en un entorno de Windows Explorer para que los usuarios puedan obtener rápidamente una vista previa, filtrar y actuar en los resultados de la búsqueda.

WDS indexa los datos dentro de un ámbito de rastreo determinado, las ubicaciones especificadas dentro de un equipo local y la red compartida que el indexador debe rastrear. Este ámbito de rastreo se puede controlar mediante opciones de conjunto de usuarios, API de administración y directivas de grupo, que los administradores de red pueden configurar para controlar los permisos de acceso de usuario y la configuración de indexación. Las directivas de grupo pueden restringir el acceso a determinados recursos de red, así como definir los recursos que se indexarán.

Esta sección contiene los siguientes temas:

-   [Información general](#windows-desktop-search-2x)
    -   [Acerca del indexador WDS](#about-the-wds-indexer)
    -   [Acerca del catálogo de WDS](#about-the-wds-catalog)
    -   [Acerca del motor de búsqueda y los resultados](#about-the-search-engine-and-results)
-   [Desarrollo con WDS](#developing-with-wds)
    -   [Agregar datos al índice con complementos](#adding-data-to-the-index-with-add-ins)
    -   [Consulta del índice](#querying-the-index)
-   [Requisitos de compatibilidad](#compatibility-requirements)
    -   [Requisitos del sistema](#system-requirements)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

### <a name="about-the-wds-indexer"></a>Acerca del indexador WDS

Cuando se instala por primera vez, el indexador rastrea los archivos más comunes orientados al usuario en la carpeta Mis documentos, las carpetas de correo electrónico de Microsoft Outlook y Microsoft Outlook Express y las ubicaciones especificadas en directiva de grupo. Los usuarios también pueden especificar nuevos archivos y ubicaciones para que el indexador incluya (o excluya) en rastreos sucesivos. Cada ubicación incluida se identifica por dirección URL, y el indexador se iniciará en esa dirección URL y recorrerá en iteración recursiva todas las subcarpetas o ubicaciones hasta que se hayan indexado todos los elementos. Un ámbito es un conjunto de direcciones URL. Las API de administración las pueden usar las aplicaciones personalizadas para definir su ámbito de rastreo, un conjunto de direcciones URL que apuntan a rutas de acceso dentro de un protocolo, como para las carpetas de una unidad o para almacenes de correo electrónico `file://` `mapi:// ` DE TIPO OUTLOOK. WDS usa controladores de protocolo para acceder a los almacenes de datos y filtros para analizar e indexar el texto y las propiedades de los elementos. A continuación, estos datos se almacenan en el catálogo.

### <a name="about-the-wds-catalog"></a>Acerca del catálogo de WDS

El catálogo de WDS es un índice de texto y propiedades recopilados de los elementos del correo electrónico, las unidades locales, los recursos de red y otros almacenes de datos locales especificados. El contenido del catálogo se basa en opciones y reglas establecidas por WDS, aplicaciones basadas en la plataforma WDS, preferencias de usuario y directivas de grupo. Hay más de 200 propiedades disponibles para cada elemento indexado, como la fecha de creación, el tamaño y las propiedades específicas del tipo ("From" para los mensajes de correo electrónico). Para obtener una lista de estas propiedades, vea la referencia de esquema [de](-search-2x-wds-schematable.md)WDS .

### <a name="about-the-search-engine-and-results"></a>Acerca del motor de búsqueda y los resultados

Desde la barra de escritorio de WDS o Windows Explorer, los usuarios pueden buscar en el contenido de texto completo y los metadatos de propiedades de los elementos indizados. Los mismos tipos de búsquedas también se pueden iniciar desde la línea de comandos, desde una página web o desde una aplicación personalizada. El motor de búsqueda de WDS busca elementos que coinciden con los criterios de búsqueda y los devuelve como conjuntos de resultados ActiveX Data Objects (ADO) de Microsoft. WDS muestra los elementos que coinciden con los criterios de búsqueda y puede presentar una vista previa completa del elemento. Puede crear aplicaciones para interceptar la consulta de búsqueda, realizar la búsqueda o mostrar el conjunto de resultados.

## <a name="developing-with-wds"></a>Desarrollo con WDS

Hay dos tipos principales de integración con WDS: agregar datos al índice y consultar el contenido del índice para recuperar registros que coincidan con los criterios de búsqueda.

### <a name="adding-data-to-the-index-with-add-ins"></a>Agregar datos al índice con Add-Ins

Básicamente, hay dos tipos de orígenes de datos: almacenes del sistema de archivos y almacenes que no son del sistema de archivos. Un grupo de archivos de Mis documentos es un almacén de sistema de archivos simple. WDS puede buscar información en los archivos almacenados en este tipo de sistema de archivos si puede buscar un filtro para el tipo de archivo. Puede habilitar WDS para indexar un nuevo tipo de archivo propietario si proporciona una implementación de la [**interfaz IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para ese tipo de archivo.

Un almacén que no es de sistema de archivos, como una base de datos, requiere un controlador de protocolo para permitir que WDS navegue e indexe los datos dentro del almacén de datos. Por ejemplo, si tiene un cliente de correo electrónico que almacena su lista de correo electrónico recibido en su propio archivo (por ejemplo, archivos PST en Outlook), puede proporcionar un controlador de protocolo para indexar y buscar cada correo electrónico individual proporcionando un controlador de protocolo. Si el almacén de datos es jerárquico, también deberá implementar una interfaz [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para enumerar los elementos del almacén. Para mejorar la experiencia del usuario, puede implementar una extensión de Shell para proporcionar iconos y menús contextuales desde la vista de resultados.

Actualmente, WDS contiene filtros para más de 200 tipos de elementos (incluidos los elementos de texto no cifrado como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolos y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si ya tiene filtros instalados para los tipos de archivo propietarios, WDS puede usar las interfaces de filtro existentes para indexar estos datos.

### <a name="querying-the-index"></a>Consulta del índice

WDS proporciona a las aplicaciones conjuntos de resultados personalizados de datos del índice en función de cualquiera de los valores de esquema disponibles. Los resultados se devuelven como conjuntos de registros de ADO. Hay cuatro maneras de incorporar consultas WDS en una aplicación, cada una de las que ofrece varios niveles de personalización y solidez.

-   Interfaz ISearchDesktop: las API de esta interfaz se usan para llamar a WDS mediante programación especificando una cadena de consulta, una lista de columnas que se van a devolver, restricciones de ámbito similares a una cláusula WHERE de Lenguaje de consulta estructurado (SQL) y el nombre de la columna por la que se va a ordenar. Estas API están disponibles para código nativo y administrado.
-   Control de ActiveX WDS: este control dibuja la interfaz de búsqueda de WDS y administra la búsqueda y la visualización de resultados. Este método es más fácil que usar las API, pero es menos flexible. Para usar este control en una aplicación  Microsoft Visual Studio, vaya al cuadro de diálogo Elegir elementos del cuadro de  herramientas en el menú Herramientas y agregue "Búsqueda de escritorio de Windows - Visor de resultados" al cuadro de herramientas desde la pestaña **Componentes COM** .  A continuación, agregue el control al formulario en el que desea incluirlo. El control de ActiveX WDS es compatible con WDS 2.x y 3.x Windows XP.
-   Parámetros de la línea de comandos: las aplicaciones pueden llamar al ejecutable de WDS con varios parámetros para buscar y mostrar los resultados. Se abrirá una ventana wds con los resultados mostrados. Esta es la manera más fácil de agregar búsqueda a una aplicación, pero no devuelve a la aplicación que realiza la llamada ninguna información sobre lo que hace el usuario dentro de la ventana wds.
-   Objeto del asistente del explorador WDS (BHO): de forma similar, las páginas web pueden usar la BHO para enviar consultas a WDS o a la aplicación de búsqueda registrada. Después de validar la dirección URL de las páginas web en la lista de dominios seguros de WDS, WDS ejecutará la consulta y mostrará los resultados mediante la interfaz de búsqueda estándar, o bien pasará la consulta a la aplicación de búsqueda registrada.

Los usuarios pueden usar [la sintaxis de](-search-2x-wds-aqsreference.md) consulta avanzada para consultar el catálogo de forma más eficaz mediante el control del ámbito de las búsquedas y la combinación de parámetros de búsqueda con operadores booleanos. Por ejemplo, un usuario podría buscar datos adjuntos en un correo electrónico de John que incluya "programación del proyecto" o "plan de proyecto" con una consulta como la siguiente: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisitos de compatibilidad

WDS 2.6.5 está disponible para Windows 2000, Windows Server 2003 y Windows XP. WDS es una descarga independiente disponible de Microsoft de forma gratuita para uso personal y empresarial. Debe estar instalado y en uso para indexar la cuenta de usuario antes de que las aplicaciones creadas para WDS 2.6.5 funcionen.

### <a name="system-requirements"></a>Requisitos del sistema

Se requiere lo siguiente para usar Windows Desktop Search:

-   Windows Internet Explorer o posterior.
-   Para incluir los mensajes de correo electrónico en el catálogo, debe tener Microsoft Microsoft Outlook 2000 o posterior o Microsoft Outlook Express 6.0 o posterior.
-   La versión preliminar completa de los Microsoft Office de Microsoft en la vista de resultados requiere Office XP o posterior.
-   Procesador Pentium mínimo de 500 MHz (se recomienda 1 GHz).
-   Windows XP, Windows 2000 SP4 o posterior, o Windows Server 2003 Service Pack 1.
-   128 MB como mínimo de RAM (se recomiendan 256 MB).
-   Se recomiendan 500 MB de espacio libre en disco duro. El tamaño del índice depende de la cantidad de contenido que haya indexado.
-   Se recomienda una resolución de pantalla de 1024 x 768.

## <a name="related-topics"></a>Temas relacionados

1.  Consulta del índice

    -   [Llamar a WDS mediante programación (a través de ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Llamada a WDS desde páginas web](-search-2x-wds-browserhelpobject.md)
    -   [Llamada a WDS desde la línea de comandos](-search-2x-wds-fromcommandline.md)

2.  [Extender el índice (información general)](-search-2x-wds-extendingtheindex.md)

    -   [Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Desarrollar controladores de protocolo](-search-2x-wds-phaddins.md)

3.  Referencias generales

    -   [Esquema WDS](-search-2x-wds-schematable.md)
    -   [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
    -   [Tipos percibidos de WDS](-search-2x-wds-perceivedtype.md)

 

 
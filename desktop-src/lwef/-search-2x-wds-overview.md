---
title: Windows Desktop Search 2. x
description: Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de Windows Search.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5131fe700b7b049371625249768b0073d009a87
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105720144"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).

WDS es un servicio de indexación y una plataforma que proporciona una búsqueda rápida de archivos y datos en diferentes ubicaciones y orígenes de datos. WDS ayuda a los usuarios y otras aplicaciones a encontrar prácticamente cualquier elemento en sus equipos, mensajes de correo electrónico, citas del calendario, fotos, documentos y mucho más. Además, WDS puede devolver resultados de varios orígenes de datos en un entorno del explorador de Windows para que los usuarios puedan obtener una vista previa, filtrar y actuar con rapidez en los resultados de la búsqueda.

WDS indexa los datos dentro de un ámbito de rastreo determinado, las ubicaciones especificadas en un equipo local y la red compartida que el indexador debe rastrear. Este ámbito de rastreo se puede controlar mediante opciones de conjunto de usuarios, API de administración y directivas de grupo, que los administradores de red pueden configurar para controlar los permisos de acceso de usuario y la configuración de indización. Las directivas de grupo pueden restringir el acceso a determinados recursos de red, así como definir los recursos que se van a indexar.

Esta sección contiene los siguientes temas:

-   [Información general](#windows-desktop-search-2x)
    -   [Acerca del indexador de WDS](#about-the-wds-indexer)
    -   [Acerca del catálogo de WDS](#about-the-wds-catalog)
    -   [Acerca del motor de búsqueda y los resultados](#about-the-search-engine-and-results)
-   [Desarrollo con WDS](#developing-with-wds)
    -   [Agregar datos al índice con complementos](#adding-data-to-the-index-with-add-ins)
    -   [Consultar el índice](#querying-the-index)
-   [Requisitos de compatibilidad](#compatibility-requirements)
    -   [Requisitos del sistema](#system-requirements)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

### <a name="about-the-wds-indexer"></a>Acerca del indexador de WDS

Cuando se instala por primera vez, el indexador rastrea los archivos más comunes orientados al usuario en la carpeta Mis documentos, las carpetas de correo electrónico de Microsoft Outlook y Microsoft Outlook Express, y las ubicaciones especificadas en directiva de grupo. Los usuarios también pueden especificar nuevos archivos y ubicaciones para que el indexador los incluya (o excluya) en rastreos sucesivos. Cada ubicación incluida se identifica mediante la dirección URL, y el indexador se iniciará en esa dirección URL y recorrerá en iteración de forma recursiva las subcarpetas o ubicaciones hasta que todos los elementos se hayan indizado. Un ámbito es un conjunto de direcciones URL. Las aplicaciones personalizadas pueden usar las API de administración para definir su ámbito de rastreo, un conjunto de direcciones URL que apuntan a rutas de acceso dentro de un protocolo como, por ejemplo, `file://` para carpetas de una unidad o `mapi:// ` para almacenes de correo electrónico MAPI como Outlook. WDS usa controladores de protocolo para tener acceso a los almacenes de datos y filtros para analizar e indexar el texto y las propiedades de los elementos. Estos datos se almacenan en el catálogo.

### <a name="about-the-wds-catalog"></a>Acerca del catálogo de WDS

El catálogo de WDS es un índice de texto y propiedades recopiladas de los elementos del correo electrónico, las unidades locales, los recursos de red y otros almacenes de datos locales especificados. El contenido del catálogo se basa en las opciones y reglas establecidas por WDS, las aplicaciones basadas en la plataforma WDS, las preferencias de usuario y las directivas de grupo. Hay más de 200 propiedades disponibles para cada elemento indizado, como la fecha de creación, el tamaño y las propiedades específicas del tipo ("de" para los mensajes de correo electrónico). Para obtener una lista de estas propiedades, vea la [Referencia del esquema](-search-2x-wds-schematable.md)de WDS.

### <a name="about-the-search-engine-and-results"></a>Acerca del motor de búsqueda y los resultados

Desde la barra de escritorio de WDS o desde el explorador de Windows, los usuarios pueden buscar el contenido de texto completo y los metadatos de propiedad de elementos indizados. También se pueden iniciar los mismos tipos de búsquedas desde la línea de comandos, desde una página web o desde una aplicación personalizada. El motor de búsqueda de WDS localiza los elementos que coinciden con los criterios de búsqueda y los devuelve como conjuntos de resultados de Microsoft Objetos de datos ActiveX (ADO). WDS muestra los elementos que coinciden con los criterios de búsqueda y puede presentar una vista previa enriquecida del elemento. Puede crear aplicaciones para interceptar la consulta de búsqueda, realizar la búsqueda o mostrar el conjunto de resultados.

## <a name="developing-with-wds"></a>Desarrollo con WDS

Hay dos tipos principales de integración con WDS: agregar datos al índice y consultar el contenido del índice para recuperar los registros que coinciden con los criterios de búsqueda.

### <a name="adding-data-to-the-index-with-add-ins"></a>Agregar datos al índice con Add-Ins

Básicamente, hay dos tipos de orígenes de datos: almacenes del sistema de archivos y almacenes del sistema que no son de archivos. Un grupo de archivos de mis documentos es un almacén de sistema de archivos simple. WDS puede buscar información en los archivos almacenados en un sistema de archivos de este tipo si puede localizar un filtro para el tipo de archivo. Puede habilitar WDS para indexar un nuevo tipo de archivo propietario si proporciona una implementación de la interfaz [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para ese tipo de archivo.

Un almacén de sistema que no es de archivos, como una base de datos, requiere un controlador de protocolo para permitir que WDS navegue por los datos del almacén de datos y los indexen. Por ejemplo, si tiene un cliente de correo que almacena la lista de correo electrónico recibido en su propio archivo (como archivos PST en Outlook), puede proporcionar un controlador de protocolo para indexar y buscar cada correo electrónico individual proporcionando un controlador de protocolo. Si el almacén de datos es jerárquico, también tendrá que implementar una interfaz [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para enumerar los elementos del almacén. Para mejorar la experiencia del usuario, puede implementar una extensión de Shell para proporcionar iconos y menús contextuales desde la vista de resultados.

Actualmente, WDS contiene filtros para más de 200 tipos de elementos (incluidos los elementos de texto no cifrado, como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolo y de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si ya tiene filtros instalados para tipos de archivo propietarios, WDS puede usar las interfaces de filtro existentes para indizar estos datos.

### <a name="querying-the-index"></a>Consultar el índice

WDS proporciona a las aplicaciones conjuntos de resultados personalizados de datos del índice en función de los valores de esquema disponibles. Los resultados se devuelven como conjuntos de registros de ADO. Hay cuatro maneras de incorporar consultas de WDS en una aplicación, cada una de las cuales ofrece varios niveles de personalización y solidez.

-   Interfaz ISearchDesktop: las API de esta interfaz se usan para llamar a WDS mediante programación especificando una cadena de consulta, una lista de columnas para devolver, restricciones de ámbito similares a una cláusula WHERE de Lenguaje de consulta estructurado (SQL) y el nombre de la columna por la que se va a ordenar. Estas API están disponibles para código nativo y administrado.
-   Control ActiveX de WDS: este control dibuja la interfaz de búsqueda de WDS y administra la búsqueda y la visualización de los resultados. Este método es más fácil que usar las API pero es menos flexible. Para usar este control en una aplicación Microsoft Visual Studio, vaya al cuadro de diálogo **elegir elementos del cuadro de herramientas** en el menú **herramientas** y agregue "Windows Desktop Search-Results Viewer" al **cuadro de herramientas** en la pestaña **componentes com** . A continuación, agregue el control al formulario en el que desea incluirlo. El control ActiveX de WDS solo es compatible con WDS 2. x y 3. x en Windows XP.
-   Parámetros de la línea de comandos: las aplicaciones pueden llamar al archivo ejecutable de WDS con varios parámetros para buscar y mostrar los resultados. Se abrirá una ventana de WDS con los resultados mostrados. Esta es la manera más fácil de agregar la búsqueda a una aplicación, pero no vuelve a la aplicación que realiza la llamada a cualquier información sobre lo que hace el usuario en la ventana de WDS.
-   Objeto auxiliar de explorador de WDS (BHO): de forma similar, las páginas web pueden usar el BHO para enviar consultas a WDS o a la aplicación de búsqueda registrada. Después de validar la dirección URL de las páginas web con la lista segura de dominio de WDS, WDS ejecutará la consulta y mostrará los resultados mediante la interfaz de búsqueda estándar, o bien pasará la consulta a la aplicación de búsqueda registrada.

Los usuarios pueden usar la [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md) para consultar el catálogo de forma más eficaz mediante el control del ámbito de las búsquedas y la combinación de parámetros de búsqueda con operadores booleanos. Por ejemplo, un usuario podría buscar datos adjuntos en un correo electrónico de John que incluya "programación del proyecto" o "plan del proyecto" con una consulta similar a la siguiente: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisitos de compatibilidad

WDS 2.6.5 solo está disponible para Windows 2000, Windows Server 2003 y Windows XP. WDS es una descarga independiente disponible de Microsoft gratis para uso personal y empresarial. Debe instalarse y usarse para indizar la cuenta de usuario antes de que las aplicaciones compiladas para WDS 2.6.5 funcionen.

### <a name="system-requirements"></a>Requisitos del sistema

Para usar la búsqueda de escritorio de Windows, es necesario lo siguiente:

-   Windows Internet Explorer o posterior.
-   Para incluir los mensajes de correo electrónico en el catálogo, debe tener Microsoft Microsoft Outlook 2000 o posterior, o bien Microsoft Outlook Express 6,0 o posterior.
-   La vista previa completa de los documentos de Microsoft Microsoft Office en la vista de resultados requiere Office XP o posterior.
-   Procesador Pentium 500 MHz mínimo (se recomienda 1 GHz).
-   Windows XP, Windows 2000 SP4 o posterior o Windows Server 2003 Service Pack 1.
-   Mínimo 128 MB de RAM (se recomiendan 256 MB).
-   500 MB de espacio libre en disco duro recomendado. El tamaño del índice depende de la cantidad de contenido que se haya indexado.
-   1024 x 768 se recomienda la resolución de pantalla.

## <a name="related-topics"></a>Temas relacionados

1.  Consultar el índice

    -   [Llamar a WDS mediante programación (a través de ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Llamar a WDS desde páginas web](-search-2x-wds-browserhelpobject.md)
    -   [Llamar a WDS desde la línea de comandos](-search-2x-wds-fromcommandline.md)

2.  [Extender el índice (información general)](-search-2x-wds-extendingtheindex.md)

    -   [Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Desarrollar controladores de protocolo](-search-2x-wds-phaddins.md)

3.  Referencias generales

    -   [Esquema de WDS](-search-2x-wds-schematable.md)
    -   [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
    -   [Tipos percibidos por WDS](-search-2x-wds-perceivedtype.md)

 

 
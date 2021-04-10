---
description: El administrador de ámbito de rastreo (CSM) es un conjunto de interfaces que proporciona métodos para informar al motor de búsqueda de Windows acerca de los contenedores para rastrear y los elementos de esos contenedores que se van a incluir o excluir en el catálogo.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Usar el administrador de ámbito de rastreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153993"
---
# <a name="using-the-crawl-scope-manager"></a>Usar el administrador de ámbito de rastreo

El administrador de ámbito de rastreo (CSM) es un conjunto de interfaces que proporciona métodos para informar al motor de búsqueda de Windows acerca de los contenedores para rastrear y los elementos de esos contenedores que se van a incluir o excluir en el catálogo. Los desarrolladores pueden usar CSM para definir un ámbito de rastreo mediante programación para un nuevo almacén de datos o controlador de protocolo. Los administradores pueden usar CSM para ver los índices de los usuarios, las raíces de búsqueda y las reglas de ámbito.

Esta sección está organizada de la siguiente manera:

-   [¿Qué es el administrador de ámbito de rastreo?](#what-is-the-crawl-scope-manager)
-   [Buscar raíces y reglas de ámbito](#search-roots-and-scope-rules)
    -   [Buscar raíces](#search-roots-and-scope-rules)
    -   [Reglas de ámbito](#scope-rules)
-   [Directivas de grupo admitidas por el administrador de ámbito de rastreo](#group-policies-supported-by-the-crawl-scope-manager)
-   [Temas relacionados](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>¿Qué es el administrador de ámbito de rastreo?

Para comprender el administrador del ámbito de rastreo, debe comprender los siguientes términos:

-   Un *ámbito de rastreo* es un conjunto de direcciones URL que apuntan a almacenes de datos o contenedores (almacenes de datos de correo electrónico, bases de datos, recursos compartidos de archivos de red, etc.) que el indexador rastrea a los elementos de índice. En el caso de un almacén de datos jerárquico, el ámbito de rastreo puede incluir una dirección URL principal, pero excluir una dirección URL secundaria y viceversa. Los elementos dentro del ámbito de rastreo se indizan; los elementos que se encuentran fuera del ámbito de rastreo se omiten.
-   Una *raíz de búsqueda* es la dirección URL de nivel superior que identifica un contenedor o almacén de datos que está asociado a un controlador de protocolo determinado. Las raíces de búsqueda pueden identificar ubicaciones que son específicas de un usuario, que se encuentran en un equipo remoto o que coinciden con un patrón de caracteres comodín. Al agregar un nuevo controlador de almacenamiento de datos o de protocolo, también debe agregar una raíz de búsqueda al ámbito de rastreo.
-   Una *regla de ámbito* es una regla que incluye o excluye las direcciones URL de una raíz de búsqueda que se rastrean e indexan. Por ejemplo, supongamos que desea indizar todo el contenido de la carpeta ProjectFiles, excepto los prototipos de la subcarpeta. Necesitaría una regla de inclusión para file:///C: \\ WorkteamA \\ ProjectFiles \\ y una regla de exclusión para los \\ prototipos File:///C: WorkteamA \\ ProjectFiles \\ \\ .

El **Administrador de ámbito de rastreo (CSM)** es un conjunto de API que le permite agregar, quitar y enumerar las reglas de ámbito y las raíces de búsqueda para el indizador de Windows Search. Si desea que el indexador empiece a rastrear un nuevo contenedor, puede usar CSM para establecer las reglas de ámbito y raíz de búsqueda para las rutas de acceso dentro de las raíces de búsqueda. Por ejemplo, si instala un nuevo controlador de protocolo, puede crear una raíz de búsqueda y agregar una o varias reglas de inclusión. después, el indexador puede iniciar un rastreo para la indexación inicial. CSM ofrece las siguientes interfaces para ayudarle a hacerlo mediante programación.

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

Aunque puede usar las API de CSM para definir un ámbito de rastreo mediante programación, el CSM se diseñó para admitir también usuarios finales. Por ejemplo, supongamos que ha desarrollado un controlador de protocolo para un nuevo almacén de datos y desea permitir que los usuarios o administradores administren qué rutas de acceso deben indexarse. Puede usar el administrador de ámbito de rastreo para establecer una o más raíces de búsqueda (por ejemplo, File:///C: Configurator \\ \\ ) y la interfaz de usuario de búsqueda de Windows para establecer las opciones de indización mostrará cada raíz de búsqueda con una casilla. Los usuarios pueden incluir o excluir la ruta de acceso o los elementos secundarios de dicha ruta de acceso.

## <a name="search-roots-and-scope-rules"></a>Buscar raíces y reglas de ámbito

Las reglas de ámbito y las raíces de búsqueda definen un conjunto de trabajo de direcciones URL que componen el ámbito de rastreo del indexador.

### <a name="search-roots"></a>Buscar raíces

La configuración de una raíz de búsqueda no especifica qué partes de este almacén se deben indizar; simplemente indica que existe un almacén de contenido y está asociado a un controlador de protocolo registrado. La sintaxis de una raíz de búsqueda incluye un protocolo, un identificador de seguridad de sitio o usuario y una ruta de acceso a las ubicaciones que se van a rastrear.

Debe crear nuevas raíces de búsqueda cuando:

-   Instalar un controlador de protocolo o
-   Quiere indexar un nuevo almacén de datos

y

-   ese almacén de datos aún no está en el ámbito de rastreo del indexador.

Consulte [Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md) para obtener instrucciones sobre cómo agregar, quitar y enumerar raíces de búsqueda.

### <a name="scope-rules"></a>Reglas de ámbito

Las reglas de ámbito incluyen o excluyen las direcciones URL de una raíz de búsqueda que se van a rastrear e indexar. Los usuarios finales, la Directiva de grupo o los desarrolladores de terceros pueden establecer las reglas de ámbito. Debe definir las reglas de ámbito mediante programación cuando defina una nueva raíz de búsqueda. Las reglas de ámbito y las raíces de búsqueda comprenden el ámbito de rastreo predeterminado para el almacén de datos y el controlador de protocolo.

> [!Note]  
> Los usuarios con acceso al panel de control pueden modificar el ámbito de rastreo predeterminado. Por lo tanto, cualquier aplicación que ofrezca administración de ámbitos siempre debe obtener las reglas directamente de CSM mediante los métodos de enumeración en lugar de confiar en su propia copia guardada de las reglas del usuario.

 

Consulte [Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md) para obtener instrucciones sobre cómo agregar, quitar, revertir y enumerar reglas de ámbito.

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Directivas de grupo admitidas por el administrador de ámbito de rastreo

Los administradores del sistema pueden definir ámbitos de rastreo en sus organizaciones mediante el uso de directivas de grupo. Estas reglas de directiva de grupo también pueden actuar como reglas predeterminadas, que los usuarios pueden invalidar. Por ejemplo, puede tener un conjunto de directorios indizado para un grupo de usuarios y otro distinto para otro grupo de usuarios, lo que permite a los usuarios anular la selección de estos valores predeterminados. Las reglas de directiva de grupo también pueden actuar como reglas de exclusión forzada que los usuarios no pueden invalidar, evitando que determinados usuarios indexen determinados recursos compartidos de red, por ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Administrar reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[Proceso de indización](-search-indexing-process-overview.md)
</dt> </dl>

 

 

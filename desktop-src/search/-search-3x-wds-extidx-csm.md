---
description: El Administrador del ámbito de rastreo (CSM) es un conjunto de interfaces que proporciona métodos para informar al motor de búsqueda de Windows sobre los contenedores que se rastrearán y los elementos de esos contenedores que se incluirán o excluirán en el catálogo.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Uso de la Administrador del ámbito de rastreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363307"
---
# <a name="using-the-crawl-scope-manager"></a>Uso de la Administrador del ámbito de rastreo

El Administrador del ámbito de rastreo (CSM) es un conjunto de interfaces que proporciona métodos para informar al motor de búsqueda de Windows sobre los contenedores que se rastrearán y los elementos de esos contenedores que se incluirán o excluirán en el catálogo. Los desarrolladores pueden usar el CSM para definir un ámbito de rastreo mediante programación para un nuevo almacén de datos o controlador de protocolo. Los administradores pueden usar el CSM para ver los índices de todos los usuarios, las raíces de búsqueda y las reglas de ámbito.

Esta sección se organiza de la siguiente manera:

-   [¿Cuál es el Administrador del ámbito de rastreo?](#what-is-the-crawl-scope-manager)
-   [Reglas de ámbito y raíces de búsqueda](#search-roots-and-scope-rules)
    -   [Buscar raíces](#search-roots-and-scope-rules)
    -   [Reglas de ámbito](#scope-rules)
-   [Directivas de grupo admitidas por el Administrador del ámbito de rastreo](#group-policies-supported-by-the-crawl-scope-manager)
-   [Temas relacionados](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>¿Cuál es el Administrador del ámbito de rastreo?

Para comprender el Administrador del ámbito de rastreo, debe comprender los términos siguientes:

-   Un *ámbito de* rastreo es un conjunto de direcciones URL que apuntan a almacenes de datos o contenedores (almacenes de datos de correo electrónico, bases de datos, recursos compartidos de archivos de red, entre otros) que el indexador rastrea a elementos de índice. Para un almacén de datos jerárquico, el ámbito de rastreo puede incluir una dirección URL primaria, pero excluir una dirección URL secundaria y viceversa. Los elementos dentro del ámbito de rastreo están indexados; Se omiten los elementos fuera del ámbito de rastreo.
-   Una *raíz de búsqueda* es la dirección URL de nivel superior que identifica un contenedor o almacén de datos asociado a un controlador de protocolo determinado. Las raíces de búsqueda pueden identificar ubicaciones específicas de un usuario, que se encuentran en un equipo remoto o que coinciden con un patrón de caracteres comodín. Al agregar un nuevo almacén de datos o controlador de protocolo, también debe agregar una raíz de búsqueda al ámbito de rastreo.
-   Una *regla de* ámbito es una regla que incluye o excluye las direcciones URL dentro de una raíz de búsqueda para que no se rastreen e indexe. Por ejemplo, supongamos que quiere que todo lo que hay dentro de la carpeta ProjectFiles se indexe excepto la subcarpeta Prototypes. Necesitará una regla de inclusión para file:///C: WorkteamA ProjectFiles y una regla de exclusión \\ \\ para \\ file:///C: \\ WorkteamA \\ \\ ProjectFiles Prototypes \\ .

El **Administrador del ámbito de rastreo (CSM)** es un conjunto de API que le permiten agregar, quitar y enumerar raíces de búsqueda y reglas de ámbito para el indexador Windows Search. Si desea que el indexador comience a rastrear un nuevo contenedor, puede usar el CSM para establecer las reglas de ámbito y raíz de búsqueda para las rutas de acceso dentro de las raíz de búsqueda. Por ejemplo, si instala un nuevo controlador de protocolo, puede crear una raíz de búsqueda y agregar una o varias reglas de inclusión. a continuación, el indexador puede iniciar un rastreo para la indexación inicial. El CSM ofrece las siguientes interfaces para ayudarle a hacerlo mediante programación.

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

Aunque puede usar las API de CSM para definir un ámbito de rastreo mediante programación, el CSM también se diseñó para admitir a los usuarios finales. Por ejemplo, supongamos que ha desarrollado un controlador de protocolo para un nuevo almacén de datos y quiere permitir que los usuarios o administradores administren qué rutas de acceso se deben indexar. Puede usar el Administrador del ámbito de rastreo para establecer una o varias raíces de búsqueda (por ejemplo, file:///C: MyContainer ) y la interfaz de usuario de Windows Search para establecer opciones de indexación mostrará cada raíz de búsqueda con una \\ \\ casilla. A continuación, los usuarios pueden incluir o excluir esa ruta de acceso o los secundarios de esa ruta de acceso.

## <a name="search-roots-and-scope-rules"></a>Reglas de ámbito y raíces de búsqueda

Las raíces de búsqueda y las reglas de ámbito juntos definen un conjunto de direcciones URL que componen el ámbito de rastreo del indexador.

### <a name="search-roots"></a>Buscar raíces

Establecer una raíz de búsqueda no especifica qué partes de este almacén se deben indexar; simplemente indica que existe un almacén de contenido y que está asociado a un controlador de protocolo registrado. La sintaxis de una raíz de búsqueda incluye un protocolo, un identificador de seguridad de sitio o usuario y una ruta de acceso a las ubicación que se rastrearán.

Debe crear nuevas raíces de búsqueda cuando:

-   Instalación de un controlador de protocolo OR
-   Desea indexar un nuevo almacén de datos

y

-   que el almacén de datos aún no está en el ámbito de rastreo del indexador.

Consulte Administración [de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md) para obtener instrucciones sobre cómo agregar, quitar y enumerar raíces de búsqueda.

### <a name="scope-rules"></a>Reglas de ámbito

Las reglas de ámbito incluyen o excluyen las direcciones URL dentro de una raíz de búsqueda para que no se rastreen e indexe. Los usuarios finales, la directiva de grupo o desarrolladores de terceros pueden establecer reglas de ámbito. Debe definir reglas de ámbito mediante programación al definir una nueva raíz de búsqueda. Las raíces de búsqueda y las reglas de ámbito componen el ámbito de rastreo predeterminado para el almacén de datos y el controlador de protocolo.

> [!Note]  
> Los usuarios con acceso a Panel de control pueden modificar el ámbito de rastreo predeterminado. Por lo tanto, cualquier aplicación que ofrece administración de ámbitos siempre debe obtener las reglas directamente desde el CSM mediante los métodos de enumeración en lugar de basarse en su propia copia guardada de las reglas del usuario.

 

Consulte Administración [de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md) para obtener instrucciones sobre cómo agregar, quitar, revertir y enumerar reglas de ámbito.

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Directivas de grupo admitidas por el Administrador del ámbito de rastreo

Los administradores del sistema pueden definir ámbitos de rastreo en sus organizaciones mediante directivas de grupo. Estas reglas de directiva de grupo también pueden actuar como reglas predeterminadas, que los usuarios pueden invalidar. Por ejemplo, puede tener un conjunto de directorios indexados para un grupo de usuarios y un conjunto diferente para otro grupo de usuarios, lo que permite a los usuarios anular la selección de estos valores predeterminados. Las reglas de directiva de grupo también pueden actuar como reglas de exclusión forzada que los usuarios no pueden invalidar, lo que impide que determinados usuarios indexe determinados recursos compartidos de red, por ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[El proceso de indexación](-search-indexing-process-overview.md)
</dt> </dl>

 

 

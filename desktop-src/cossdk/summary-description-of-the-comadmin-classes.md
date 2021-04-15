---
description: La biblioteca COMAdmin (comadmin.dll) proporciona tres clases, cada una de las cuales implementa una interfaz dual COM.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descripción resumida de las clases COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666180"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Descripción resumida de las clases COMAdmin

La biblioteca COMAdmin (comadmin.dll) proporciona tres clases, cada una de las cuales implementa una interfaz dual COM. Los objetos creados a partir de estas clases se utilizan para obtener acceso al catálogo, para representar colecciones en el catálogo y para representar los elementos contenidos dentro de las colecciones.

## <a name="comadmincatalog"></a>COMAdminCatalog

La clase [**COMAdminCatalog**](comadmincatalog.md) representa el propio catálogo. Un objeto creado a partir de **COMAdminCatalog** es el objeto fundamental que se usa en la administración mediante programación. Además de establecer la conexión básica con el servidor de catálogo al crear una instancia, **COMAdminCatalog** proporciona métodos que le permiten hacer lo siguiente:

-   Obtener recopilaciones en el catálogo.
-   Conéctese al servidor de catálogo en un equipo remoto.
-   Instalar, exportar, iniciar, apagar y obtener información relacionada con las aplicaciones COM+.
-   Instalar componentes en aplicaciones COM+ y obtener información sobre los componentes.
-   Iniciar, detener o actualizar los servicios que se ejecutan en la máquina.
-   Actualice, restaure o haga una copia de seguridad de la información del catálogo.

En COM+ 1,0, la clase [**COMAdminCatalog**](comadmincatalog.md) implementa la interfaz [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) . En COM+ 1,5, la clase **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) como su interfaz predeterminada.

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

La clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) representa cualquier colección del catálogo, proporcionando una cadena que asigna un nombre a la colección determinada en el momento de la creación de instancias de objeto. (Las colecciones de catálogos disponibles se denominan en la tabla de [colecciones de administración de com+](com--administration-collections.md)). Los objetos se crean a partir de esta clase al recuperar una colección de nivel superior llamando al método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) del objeto [**COMAdminCatalog**](comadmincatalog.md) . Estos objetos también se crean al recuperar una colección secundaria llamando al método **GetCollection** de su objeto de colección primario. Los objetos **COMAdminCatalogCollection** permiten hacer lo siguiente:

-   Enumerar los elementos incluidos en la colección.
-   Recupera un elemento de la colección.
-   Agregar o quitar elementos de la colección.
-   Guardar o descartar los cambios pendientes realizados en la colección o en los elementos que contiene.
-   Obtener una colección diferente en el catálogo.

La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa la interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) representa cualquier elemento incluido en una colección. Los objetos se crean a partir de esta clase al obtener un elemento a través de la propiedad [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) de un objeto de colección de catálogos. Los objetos creados a partir de la clase **COMAdminCatalogObject** permiten hacer lo siguiente:

-   Obtiene o establece las propiedades admitidas por el elemento que se va a utilizar para representar el objeto.
-   Obtenga información sobre el elemento y sus propiedades.

La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa la interfaz [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso al catálogo de COM+](accessing-the-com--catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 




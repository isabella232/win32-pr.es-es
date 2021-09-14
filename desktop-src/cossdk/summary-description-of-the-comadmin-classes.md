---
description: Hay tres clases proporcionadas por la biblioteca COMAdmin (comadmin.dll), cada una de las cuales implementa una interfaz dual COM.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descripción resumida de las clases COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361638"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Descripción resumida de las clases COMAdmin

Hay tres clases proporcionadas por la biblioteca COMAdmin (comadmin.dll), cada una de las cuales implementa una interfaz dual COM. Los objetos creados a partir de estas clases se usan para obtener acceso al catálogo, representar colecciones en el catálogo y representar los elementos contenidos en las colecciones.

## <a name="comadmincatalog"></a>COMAdminCatalog

La [**clase COMAdminCatalog**](comadmincatalog.md) representa el propio catálogo. Un objeto creado a partir **de COMAdminCatalog** es el objeto fundamental que se usa en la administración mediante programación. Además de establecer la conexión básica con el servidor de catálogo al crear una instancia de él, **COMAdminCatalog** proporciona métodos que le permiten hacer lo siguiente:

-   Obtener colecciones en el catálogo.
-   Conectar al servidor de catálogo en un equipo remoto.
-   Instalar, exportar, iniciar, apagar y obtener información relacionada con las aplicaciones COM+.
-   Instale componentes en aplicaciones COM+ y obtenga información sobre los componentes.
-   Inicie, detenga o actualice los servicios que se ejecutan en la máquina.
-   Actualice, restaure o haga una copia de seguridad de la información del catálogo.

En COM+ 1.0, la [**clase COMAdminCatalog**](comadmincatalog.md) implementa la [**interfaz ICOMAdminCatalog.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) En COM+ 1.5, la clase **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) como su interfaz predeterminada.

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

La [**clase COMAdminCatalogCollection representa**](comadmincatalogcollection.md) cualquier colección del catálogo, al proporcionar una cadena que asigna un nombre a la colección determinada en el momento de la creación de instancias del objeto. (Las colecciones de catálogo disponibles se denominan en la tabla en [Colecciones de administración de COM+).](com--administration-collections.md) Los objetos se crean a partir de esta clase al recuperar una colección de nivel superior mediante una llamada al [**método GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) del [**objeto COMAdminCatalog.**](comadmincatalog.md) Estos objetos también se crean al recuperar una colección secundaria llamando al **método GetCollection** de su objeto de colección primario. **Los objetos COMAdminCatalogCollection** permiten hacer lo siguiente:

-   Enumerar a través de los elementos contenidos en la colección.
-   Recuperar un elemento de la colección.
-   Agregue o quite elementos de la colección.
-   Guarde o descarte los cambios pendientes realizados en la colección o en los elementos que contiene.
-   Obtenga una colección diferente en el catálogo.

La [**clase COMAdminCatalogObject**](comadmincatalogobject.md) implementa la [**interfaz ICatalogCollection.**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

La [**clase COMAdminCatalogObject**](comadmincatalogobject.md) representa cualquier elemento que se encuentra dentro de una colección. Los objetos se crean a partir de esta clase al obtener un elemento a través de la [**propiedad Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) de un objeto de colección de catálogo. Los objetos creados a partir de la clase **COMAdminCatalogObject** permiten hacer lo siguiente:

-   Obtiene o establece las propiedades admitidas por el elemento que se usa para representar el objeto.
-   Obtenga información sobre el elemento y sus propiedades.

La [**clase COMAdminCatalogObject**](comadmincatalogobject.md) implementa la [**interfaz ICatalogObject.**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso al catálogo de COM+](accessing-the-com--catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 




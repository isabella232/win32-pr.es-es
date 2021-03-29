---
title: Implementación del administrador de categorías de componentes
description: A medida que crece el número de componentes disponibles, se hace cada vez más difícil administrar estos componentes. En cuanto a las interfaces que exponen, así como las tareas que realizan, muchos componentes ofrecen una funcionalidad similar.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994580"
---
# <a name="component-categories-manager-implementation"></a>Implementación del administrador de categorías de componentes

A medida que crece el número de componentes disponibles, se hace cada vez más difícil administrar estos componentes. En cuanto a las interfaces que exponen, así como las tareas que realizan, muchos componentes ofrecen una funcionalidad similar.

A menudo es necesario enumerar los componentes que se pueden usar en un contexto determinado. Ejemplos de esto son el cuadro de diálogo **Insertar objeto** que se usa en los documentos compuestos OLE y el cuadro de diálogo **Insertar control** que se usa en los controles OLE. Estos cuadros de diálogo muestran todos los componentes que cumplen (o reclaman) los contratos de interfaz para los documentos o controles compuestos. Estas categorías existentes (documento OLE, control OLE) no implican una firma exacta de la interfaz. Los documentos OLE deben exponer un conjunto determinado de interfaces principales (por ejemplo, [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) o [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)), pero también pueden exponer interfaces adicionales como [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

En el pasado, los componentes se etiquetaron agregando un nombre legible ("insertable", "control", etc.) como una subclave a las **clases HKEY \_ \_ raíz \\ CLSID \\ {...}** clave del registro correspondiente al componente. Esto funciona bien para una definición central de las categorías, pero arriesga los conflictos de nombres cuando muchas entidades independientes definen nuevas categorías. Como en otras áreas de COM, la solución para proporcionar un espacio de nombres extensible se basa en el uso de identificadores únicos globales (GUID). En lugar de usar un nombre legible, se asigna un número único (CATId) a cada categoría.

Otra limitación de la categorización existente es que se limita a expresar las capacidades del propio componente. Muchos componentes requieren ciertas funcionalidades de los contenedores. Cuando se inserta este componente en un contenedor, la inserción puede producir un error o comportarse de forma inesperada, incluso aunque el componente cumpla los contratos que una de sus categorías implica. Para enumerar los componentes que se pueden usar correctamente en determinadas situaciones, se deben tener en cuenta las capacidades del componente y del contenedor.

Debido a estas consideraciones, se realizaron los siguientes cambios en la categorización existente:

-   Las categorías se indican mediante CATID que son identificadores únicos globales.
-   En la subclave **Components** de la clave del registro **\_ \_ \\ CLSID raíz de las clases HKEY** , se desarrollaron dos subclaves independientes, "Categories implementadas" y "Categories Required". Estas subclaves contienen las listas de CATID que proporciona el componente o que el contenedor del componente debe proporcionar.

Para facilitar la administración de las categorías de componentes, las categorías se muestran en una ubicación central en el registro: **\_ clases HKEY categorías de \_ \\ componentes raíz**. Esta clave enumera las categorías instaladas con su CATId y con los nombres localizados y legibles.

Para obtener más información, vea los temas siguientes:

-   [Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
-   [Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
-   [Administrador de categorías de componentes](the-component-categories-manager.md)
-   [Clases y asociaciones predeterminadas](default-classes-and-associations.md)
-   [Definir categorías de componentes](defining-component-categories.md)
-   [Asociar iconos a una categoría](associating-icons-with-a-category.md)

 

 





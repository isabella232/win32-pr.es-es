---
title: Implementación del Administrador de categorías de componentes
description: A medida que aumenta el número de componentes disponibles, cada vez es más difícil administrarlos. En cuanto a las interfaces que exponen, así como las tareas que realizan, muchos componentes ofrecen una funcionalidad similar.
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941ba5f422a4305a3bb6056d1d02648dde3bffc9c9f872fe7f7804ebb90a19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679224"
---
# <a name="component-categories-manager-implementation"></a>Implementación del Administrador de categorías de componentes

A medida que aumenta el número de componentes disponibles, cada vez es más difícil administrarlos. En cuanto a las interfaces que exponen, así como las tareas que realizan, muchos componentes ofrecen una funcionalidad similar.

A menudo es necesario enumerar los componentes que se pueden usar en un contexto determinado. Ejemplos de esto son el **cuadro de diálogo Insertar objeto** usado en documentos compuestos OLE y el cuadro de diálogo Insertar **control** usado en controles OLE. Estos cuadros de diálogo enumera todos los componentes que cumplen (o reclaman cumplir) los contratos de interfaz para los documentos o controles compuestos. Estas categorías existentes (documento OLE, control OLE) no implican una firma de interfaz exacta. Los documentos OLE tienen que exponer un determinado conjunto de interfaces principales (por ejemplo, [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) o [**IPersistStorage),**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)pero también pueden exponer interfaces adicionales como [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).

En el pasado, los componentes se etiquetan agregando un nombre legible ("Insertable", "Control", etc.) como subclave a **HKEY \_ CLASSES ROOT \_ \\ CLSID \\ {...}** Clave del Registro correspondiente al componente. Esto funciona bien para una definición central de categorías, pero corre el riesgo de colisiones de nombres cuando muchas partes independientes definen nuevas categorías. Al igual que en otras áreas de COM, la solución para proporcionar un espacio de nombres extensible reside en el uso de identificadores únicos globales (GUID). En lugar de usar un nombre legible, se asigna un número único (CATID) a cada categoría.

Otra limitación con la categorización existente es que se limita a expresar las funcionalidades del propio componente. Muchos componentes requieren ciertas funcionalidades de los contenedores. Cuando este componente se inserta en un contenedor, la inserción puede producir un error o comportarse de forma inesperada, aunque el componente cumpla los contratos implícitos en una de sus categorías. Para enumerar los componentes que se pueden usar correctamente en determinadas situaciones, se deben tener en cuenta las funcionalidades del componente y del contenedor.

Debido a estas consideraciones, se realizaron los siguientes cambios en la categorización existente:

-   Las categorías se indican mediante CATID que son identificadores únicos globales.
-   En la subclave **Components** de la clave del Registro **HKEY \_ CLASSES ROOT \_ \\ CLSID,** se desarrollaron dos subclaves independientes, "Categorías implementadas" y "Categorías necesarias". Estas subclaves contienen las listas de CATID proporcionadas por el componente o que el contenedor del componente debe proporcionar.

Para facilitar la administración de las categorías de componentes, las categorías se enumeran en un lugar central del Registro: **HKEY \_ CLASSES ROOT \_ Component \\ Categories**. Esta clave enumera las categorías instaladas con su CATID y con nombres localizados y legibles.

Para obtener más información, vea los temas siguientes:

-   [Categorización por funcionalidades de componentes](categorizing-by-component-capabilities.md)
-   [Categorización por funcionalidades de contenedor](categorizing-by-container-capabilities.md)
-   [Administrador de categorías de componentes](the-component-categories-manager.md)
-   [Clases y asociaciones predeterminadas](default-classes-and-associations.md)
-   [Definir categorías de componentes](defining-component-categories.md)
-   [Asociación de iconos a una categoría](associating-icons-with-a-category.md)

 

 





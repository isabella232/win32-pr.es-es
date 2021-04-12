---
title: Definir categorías de componentes
description: Definir categorías de componentes
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269454"
---
# <a name="defining-component-categories"></a>Definir categorías de componentes

El autor de una definición de categoría de componente crea un GUID único (CATId) que se publica junto con la definición. Otras partes conocen la definición de este tipo y pueden hacer uso de las clases admitidas en consecuencia. Al igual que la firma de método de una interfaz, la semántica de una categoría no debe modificarse después de instalarse. Es mejor mantener la compatibilidad con versiones anteriores de la categoría mediante la introducción de un nuevo identificador de categoría con semántica revisada.

Dado que los identificadores de interfaz (IID) y los identificadores de categoría de componente (CATId) existen en diferentes espacios de nombres, parece que si fuera posible usar el mismo GUID para un IID y un CATId. Sin embargo, como los IID se suelen usar para el CLSID del servidor proxy/stub de la interfaz, existe la posibilidad de que se produzcan conflictos. Por lo tanto, no use el mismo GUID para un IID y CATId.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociar iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 





---
title: Definir categorías de componentes
description: Definir categorías de componentes
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369691"
---
# <a name="defining-component-categories"></a>Definir categorías de componentes

El autor de una definición de categoría de componente crea un GUID único (el CATID) que se publica junto con la definición. Otras partes conocen la definición de este tipo y pueden usar sus clases admitidas en consecuencia. Al igual que la firma de método de una interfaz, la semántica de una categoría no debe modificarse después de instalarse. Es mejor mantener la compatibilidad con versiones anteriores de la categoría mediante la introducción de un nuevo identificador de categoría con semántica revisada.

Dado que los identificadores de interfaz (IID) y los identificadores de categoría de componente (CATID) existen en espacios de nombres diferentes, parece como si fuera posible usar el mismo GUID para un IID y un CATID. Sin embargo, dado que los IID se usan a menudo para el CLSID del servidor proxy/stub de la interfaz, existe la posibilidad de conflictos. Por lo tanto, no use el mismo GUID para un IID y CATID.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociación de iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidades de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorización por funcionalidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 





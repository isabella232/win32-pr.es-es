---
title: Navegación jerárquica
description: A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios. Por ejemplo, es posible que un cliente ya tenga información sobre un control de la barra de herramientas, pero que no tenga información sobre los botones contenidos en él.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268754"
---
# <a name="hierarchical-navigation"></a>Navegación jerárquica

A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios. Por ejemplo, es posible que un cliente ya tenga información sobre un control de la barra de herramientas, pero que no tenga información sobre los botones contenidos en él.

La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expone las relaciones jerárquicas entre los objetos. Los clientes pueden desplazarse de un objeto primario a sus elementos secundarios o de un objeto secundario a su elemento primario llamando a [**IAccessible:: get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) o [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 





---
title: Propiedades y métodos de navegación de objetos
description: Los clientes navegan de un objeto a otro mediante métodos como IAccessible accNavigate e IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80631c78e42d9a480992bb40f14d12c0fca8b7c0085ec259daa5550c834d200a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133758"
---
# <a name="object-navigation-properties-and-methods"></a>Propiedades y métodos de navegación de objetos

Los *clientes navegan* de un objeto a otro mediante métodos como [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) [**e IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Estos métodos permiten a los clientes recuperar un identificador secundario o la dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de otro objeto. La navegación permite a los clientes explorar cómo se relacionan los objetos entre sí. Tenga en cuenta que navegar a otro objeto no cambia la selección ni el foco.

La [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporciona propiedades y métodos que admiten los siguientes tipos de navegación:

-   [Navegación jerárquica](hierarchical-navigation.md)
-   [Navegación espacial y lógica](spatial-and-logical-navigation.md)
-   [Navegación a través de las pruebas de impacto y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)

 

 





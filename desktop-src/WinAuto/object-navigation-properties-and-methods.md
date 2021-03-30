---
title: Métodos y propiedades de navegación de objetos
description: Los clientes navegan de un objeto a otro usando métodos como IAccessible accNavigate y IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994125"
---
# <a name="object-navigation-properties-and-methods"></a>Métodos y propiedades de navegación de objetos

Los clientes *navegan* de un objeto a otro usando métodos como [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) y [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Estos métodos permiten a los clientes recuperar un identificador secundario o la dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de otro objeto. La navegación permite a los clientes explorar cómo se relacionan entre sí los objetos. Tenga en cuenta que al navegar a otro objeto no se cambia la selección o el foco.

La interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporciona propiedades y métodos que admiten los siguientes tipos de navegación:

-   [Navegación jerárquica](hierarchical-navigation.md)
-   [Navegación espacial y lógica](spatial-and-logical-navigation.md)
-   [Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)

 

 





---
title: Navegación a través de las pruebas de impacto y la ubicación de la pantalla
description: Para buscar los secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden alcanzar los puntos de prueba en la pantalla.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34911b13a4c9bad2bfd79cb32d5654265878568ad00475ade08a87a23150b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828282"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navegación a través de las pruebas de impacto y la ubicación de la pantalla

Para buscar los secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden alcanzar los puntos de prueba en la pantalla. Hay dos métodos disponibles:

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Uso de IAccessible::accHitTest

Para identificar si un punto está dentro de un objeto, dentro de su elemento secundario o ninguno de ellos, los clientes llaman al método [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) del objeto primario, pasando las coordenadas de pantalla del punto que se va a probar. En la lista siguiente se describen algunos escenarios típicos:

-   Si los elementos secundarios del objeto se superponen en un punto especificado, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera el elemento secundario superior que parece ocupar visualmente el espacio.
-   Si una ventana cubre un elemento secundario, o si el elemento primario recorta el elemento secundario, al probar el punto cubierto se recupera el elemento secundario aunque no esté visible.
-   Si el elemento secundario encontrado en el punto especificado es un objeto accesible, en lugar de un elemento secundario, el método devuelve la interfaz [**IDispatch del**](idispatch-interface.md) elemento secundario.

## <a name="using-iaccessibleacclocation"></a>Uso de IAccessible::accLocation

Para obtener la ubicación de pantalla de un objeto o uno de los secundarios del objeto, los clientes llaman a [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Este método devuelve las coordenadas del rectángulo delimitador del objeto especificado. Si el objeto no tiene forma de rectángulo, el método devuelve las coordenadas del rectángulo más pequeño que abarca todo el objeto.

La ilustración siguiente muestra la relación entre la región de un objeto no rectangular y su rectángulo delimitador.

![ilustración que muestra la región de un objeto norectangular (un círculo) y su rectángulo delimitador.](images/region.gif)

> [!Note]  
> [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) es más preciso que [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) porque permite a los clientes determinar la ubicación de los objetos píxel a píxel en lugar de con rectángulos delimitadores. Esta precisión es útil, por ejemplo, cuando una aplicación recopila información mediante el seguimiento de la ubicación del puntero del mouse.

 

 

 





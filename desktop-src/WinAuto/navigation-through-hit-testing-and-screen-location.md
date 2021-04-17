---
title: Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla
description: Para localizar los elementos secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden presionar puntos de prueba en la pantalla.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656277"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla

Para localizar los elementos secundarios de un objeto o determinar el tamaño de un objeto, los clientes pueden presionar puntos de prueba en la pantalla. Hay dos métodos disponibles:

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>Usar IAccessible:: accHitTest

Para identificar si un punto está dentro de un objeto, dentro de su elemento secundario o ninguno de los clientes, llame al método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) del objeto primario, pasando las coordenadas de pantalla del punto al que se va a realizar la prueba de posicionamiento. En la lista siguiente se describen algunos escenarios típicos:

-   Si los elementos secundarios del objeto se superponen en un punto especificado, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) recupera el elemento secundario de nivel superior que aparece visualmente para ocupar el espacio.
-   Si una ventana cubre un elemento secundario, o si el elemento primario recorta el elemento secundario, la prueba de posicionamiento del punto de cobertura recupera el elemento secundario aunque no esté visible.
-   Si el elemento secundario que se encuentra en el punto especificado es un objeto accesible, en lugar de un elemento secundario, el método devuelve la interfaz [**IDispatch**](idispatch-interface.md) del elemento secundario.

## <a name="using-iaccessibleacclocation"></a>Usar IAccessible:: accLocation

Para obtener la ubicación de la pantalla de un objeto o de uno de los elementos secundarios del objeto, los clientes llaman a [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation). Este método devuelve las coordenadas del rectángulo delimitador del objeto especificado. Si el objeto no tiene la forma de un rectángulo, el método devuelve las coordenadas del rectángulo más pequeño que abarca todo el objeto.

La ilustración siguiente muestra la relación entre la región de un objeto no rectangular y su rectángulo delimitador.

![Ilustración que muestra la región de un objeto no rectangular (un círculo) y su rectángulo delimitador.](images/region.gif)

> [!Note]  
> [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) es más preciso que [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , ya que permite que los clientes determinen la ubicación de los objetos píxel a píxel en lugar de con rectángulos delimitadores. Esta precisión es útil, por ejemplo, cuando una aplicación está recopilando información realizando un seguimiento de la ubicación del puntero del mouse.

 

 

 





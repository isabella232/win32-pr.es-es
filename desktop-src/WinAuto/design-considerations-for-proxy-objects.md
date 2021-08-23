---
title: Consideraciones de diseño para objetos proxy
description: El diseño de objetos accesibles y proxy depende del diseño de los elementos de la interfaz de usuario del servidor. Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes correctamente.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cd96056f89e1efc18da3e299a76e92c85166efd7067e54f972a69eb8786d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830085"
---
# <a name="design-considerations-for-proxy-objects"></a>Consideraciones de diseño para objetos proxy

El diseño de objetos accesibles y proxy depende del diseño de los elementos de la interfaz de usuario del servidor. Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes correctamente.

En la lista siguiente se describen dos posibilidades de diseño:

-   Coloque el código que implementa la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el elemento de interfaz de usuario si el código de la interfaz de usuario es fácilmente extensible. En este caso, el proxy es "ligero" en el sentido de que lo único que hace es supervisar el intervalo de vida del objeto accesible, reenviar las llamadas al objeto accesible y devolver los resultados.
-   Coloque el código que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el objeto proxy. En este caso, el objeto accesible usa funciones internas para obtener información sobre el elemento de interfaz de usuario.

## <a name="trackbar-controls"></a>Controles de barra de seguimiento

Al implementar controles trackbar, use el estilo de barra de seguimiento **TBS \_ REVERSED** para proporcionar información más significativa. Este estilo invierte la escala usada por [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

En el caso de las barras de seguimiento verticales sin este estilo, [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve cero (0) cuando el control de la barra de seguimiento está en la parte superior del control; los valores aumentan a medida que se desliza el control hacia la parte inferior. Con el estilo **TBS \_ REVERSED,** **IAccessible::get \_ accValue** devuelve cien (100) cuando el control de la barra de seguimiento está en la parte superior; los números disminuyen a medida que mueve el control de la barra de seguimiento hacia la parte inferior.

En el caso de las barras de seguimiento horizontales sin este estilo, se devuelve cero (0) cuando el control de la barra de seguimiento está en el extremo izquierdo del control; los valores aumentan a medida que mueve el control de la barra de seguimiento a la derecha. Con el estilo **TBS \_ REVERSED,** [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve cien (100) cuando el control de la barra de seguimiento está a la izquierda; los valores disminuyen a medida que mueve el control de la barra de seguimiento a la derecha.

 

 





---
title: Consideraciones de diseño para objetos proxy
description: El diseño de objetos proxy y accesibles depende del diseño de los elementos de la interfaz de usuario del servidor. Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes de forma adecuada.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075310"
---
# <a name="design-considerations-for-proxy-objects"></a>Consideraciones de diseño para objetos proxy

El diseño de objetos proxy y accesibles depende del diseño de los elementos de la interfaz de usuario del servidor. Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes de forma adecuada.

En la lista siguiente se describen dos posibilidades de diseño:

-   Coloque el código que implementa la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el elemento de la interfaz de usuario si el código de la interfaz de usuario es fácilmente extensible. En este caso, el proxy es "ligero" en el sentido de que todo lo que hace es supervisar la duración del objeto accesible, reenviar las llamadas al objeto accesible y devolver los resultados.
-   Coloque el código que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el objeto proxy. En este caso, el objeto accesible usa funciones internas para obtener información sobre el elemento de la interfaz de usuario.

## <a name="trackbar-controls"></a>Controles TrackBar

Al implementar controles TrackBar, use el estilo de barra de control **TBS \_ invertido** para proporcionar información más significativa. Este estilo invierte la escala usada por [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

En el caso de los trackbars verticales sin este estilo, [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve cero (0) cuando el control de posición de la barra de progreso está en la parte superior del control; los valores aumentan a medida que se desliza el dedo hacia la parte inferior. Con el **estilo \_ invertido de TBS** , **IAccessible:: get \_ accValue** devuelve 100 (100) cuando el control de posición está en la parte superior; los números disminuyen a medida que se mueve el control de barra de desplazamiento hacia la parte inferior.

En el caso de trackbars horizontal sin este estilo, se devuelve cero (0) cuando el control de posición de la barra de desplazamiento está en el extremo izquierdo del control. los valores aumentan a medida que mueve el control de barra de desplazamiento hacia la derecha. Con el **estilo \_ invertido de TBS** , [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve 100 (100) cuando el control de la barra de desplazamiento está a la izquierda; los valores disminuyen cuando se mueve el control de posición de la barra de desplazamiento a la derecha.

 

 





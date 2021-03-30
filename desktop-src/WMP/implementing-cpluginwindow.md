---
title: Implementación de CPluginWindow
description: Implementación de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Complementos de Media Player de Windows, clase CPluginWindow
- complementos, clase CPluginWindow
- Complementos de la interfaz de usuario, clase CPluginWindow
- Complementos de la interfaz de usuario, clase CPluginWindow
- Clase CPluginWindow
- Guía de programación, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774610"
---
# <a name="implementing-cpluginwindow"></a>Implementación de CPluginWindow

La clase CPluginWindow proporciona la interfaz de usuario al complemento. En el caso del complemento de la interfaz de usuario de búsqueda, esta clase contiene el código del botón **Buscar** y el código que inicia la página Buscar cuando se hace clic en el botón.

El asistente proporciona una implementación básica de CPluginWindow en el archivo de encabezado CPluginWindow. h. Para simplificar las cosas, el complemento de la interfaz de usuario de búsqueda modificará este archivo directamente, aunque las adiciones extensas se colocarían normalmente en un archivo CPluginWindow. cpp independiente.

En las secciones siguientes se describe lo que debe hacer para implementar CPluginWindow:

-   [El mapa de mensajes](the-message-map.md)
-   [Constructor](the-constructor.md)
-   [El método OnPaint](the-onpaint-method.md)
-   [Método alcrear](the-oncreate-method.md)
-   [Método de búsqueda](the-onsearch-method.md)
-   [El método LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación de complementos de la interfaz de usuario**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 





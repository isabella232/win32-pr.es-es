---
title: Implementación de CPluginWindow
description: Implementación de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Reproductor de Windows Media complementos, clase CPluginWindow
- plug-ins,CPluginWindow (clase)
- complementos de interfaz de usuario, clase CPluginWindow
- Complementos de interfaz de usuario, clase CPluginWindow
- CPluginWindow (clase)
- guía de programación, complementos de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748140"
---
# <a name="implementing-cpluginwindow"></a>Implementación de CPluginWindow

La clase CPluginWindow proporciona la interfaz de usuario al complemento. En el caso del complemento Search UI, esta clase  contiene el código del botón Buscar y el código que inicia la página de búsqueda cuando se hace clic en el botón.

El asistente proporciona una implementación básica de CPluginWindow en el archivo de encabezado CPluginWindow.h. Para que todo sea sencillo, el complemento search ui modificará este archivo directamente, aunque normalmente se colocarían adiciones extensas en un archivo CPluginWindow.cpp independiente.

En las secciones siguientes se describe lo que debe hacer para implementar CPluginWindow:

-   [El mapa de mensajes](the-message-map.md)
-   [The Constructor](the-constructor.md)
-   [El método OnPaint](the-onpaint-method.md)
-   [El método OnCreate](the-oncreate-method.md)
-   [El método OnSearch](the-onsearch-method.md)
-   [Método LaunchPage](the-launchpage-method.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz de usuario de programación de complementos de Interfaz de usuario**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 





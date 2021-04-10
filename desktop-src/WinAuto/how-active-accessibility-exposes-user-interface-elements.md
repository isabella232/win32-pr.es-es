---
title: Cómo expone Active Accessibility elementos de la interfaz de usuario
description: Microsoft Active Accessibility crea un objeto proxy para cada elemento de la interfaz de usuario que expone.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268762"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Cómo expone Active Accessibility elementos de la interfaz de usuario

Microsoft Active Accessibility crea un objeto *proxy* para cada elemento de la interfaz de usuario que expone. Un objeto proxy actúa como intermediario entre la utilidad de cliente y el elemento de la interfaz de usuario. El propósito del objeto proxy es supervisar el intervalo de vida del elemento de la interfaz de usuario e implementar las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre del elemento de la interfaz de usuario. Los desarrolladores de servidor que crean controles personalizados u otros elementos de interfaz de usuario personalizados también deben crear objetos proxy. Para obtener más información, consulte [crear objetos proxy](creating-proxy-objects.md).

Cuando Microsoft Active Accessibility crea un objeto para exponer un control predefinido o común, realmente crea al menos dos objetos: uno para el control y otro para la ventana que rodea el control. En la mayoría de los casos, estas ventanas principales tienen la [propiedad role](role-property.md) de la [**\_ \_ ventana del sistema de roles**](object-roles.md) y tienen la misma [propiedad nombre](name-property.md) y el nombre de clase de ventana que el control. La información sobre el control que los clientes transmiten a los usuarios finales está contenida en el objeto que Microsoft Active Accessibility crea para exponer el control, no en el objeto primario que expone la ventana que rodea el control.

Para obtener más información, vea los siguientes temas.

-   [Detección de objetos innecesarios](screening-out-unnecessary-objects.md)
-   [Proporcionar la propiedad Name](providing-the-name-property.md)
-   [Asegurarse de que los elementos de la interfaz de usuario se denominan correctamente](ensure-that-ui-elements-are-named-correctly.md)
-   [Elementos de la interfaz de usuario no admitidos](unsupported-user-interface-elements.md)

 

 





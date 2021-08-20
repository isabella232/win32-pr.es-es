---
title: Cómo Active Accessibility expone Interfaz de usuario elementos
description: Microsoft Active Accessibility crea un objeto proxy para cada elemento de la interfaz de usuario que expone.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4260788cc37aa6d4a33fcccb68a51fb61833d753c98ba4ae5dcff89f0d18cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994165"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Cómo Active Accessibility expone Interfaz de usuario elementos

Microsoft Active Accessibility crea un *objeto proxy* para cada elemento de interfaz de usuario que expone. Un objeto proxy actúa como intermediario entre la utilidad de cliente y el elemento de interfaz de usuario. El propósito del objeto proxy es supervisar el intervalo de vida del elemento de interfaz de usuario e implementar las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre del elemento de interfaz de usuario. Los desarrolladores de servidores que crean controles personalizados u otros elementos de interfaz de usuario personalizados también deben crear objetos proxy. Para obtener más información, vea [Creating Proxy Objects](creating-proxy-objects.md).

Cuando Microsoft Active Accessibility crea un objeto para exponer un control predefinido o común, realmente crea al menos dos objetos: uno para el control y otro para la ventana que rodea el control. En la mayoría de los casos, estas ventanas primarias tienen la propiedad [Role](role-property.md) de [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) y tienen la misma propiedad [Name](name-property.md) y el mismo nombre de clase de ventana que el control . La información sobre el control que los clientes transmiten a los usuarios finales se encuentra en el objeto que Microsoft Active Accessibility crea para exponer el control, no en el objeto primario que expone la ventana que rodea el control.

Para obtener más información, vea los temas siguientes:

-   [Filtrado de objetos innecesarios](screening-out-unnecessary-objects.md)
-   [Proporcionar la propiedad Name](providing-the-name-property.md)
-   [Asegurarse de que los elementos de la interfaz de usuario tienen el nombre correcto](ensure-that-ui-elements-are-named-correctly.md)
-   [Elementos de Interfaz de usuario no admitidos](unsupported-user-interface-elements.md)

 

 





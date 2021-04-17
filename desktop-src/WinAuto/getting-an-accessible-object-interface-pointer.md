---
title: Obtener un puntero de interfaz de objeto accesible
description: Las aplicaciones cliente de Microsoft Active Accessibility recuperan punteros de interfaz a objetos accesibles mediante una de las siguientes funciones.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4006bf073075f2aa47a9911565213050e3d11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695710"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Obtener un puntero de interfaz de objeto accesible

Las aplicaciones cliente de Microsoft Active Accessibility recuperan punteros de interfaz a objetos accesibles mediante una de las siguientes funciones.

**AccessibleObjectFromEvent**

Muchos clientes buscan información sobre objetos accesibles específicos que generan eventos. Dado que la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es la "puerta de enlace" a los objetos accesibles, los clientes deben tener una manera fácil de asociar [WinEvents](winevents-overview.md) a la interfaz **IAccessible** del objeto que genera los eventos. Microsoft Active Accessibility proporciona la función [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) específicamente para este fin.

> [!Note]  
> Los clientes con [funciones de enlace en contexto](in-context-hook-functions.md) deben llamar a la función [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) antes de llamar a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

La función [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) acepta gran parte de la misma información que recibe la [*función de enlace*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) de un cliente. Cuando una función de enlace de cliente recibe una notificación de eventos, pasa los parámetros adecuados de los eventos a **AccessibleObjectFromEvent**.

La función recupera la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento de la interfaz de usuario que generó el evento o la interfaz del objeto primario del elemento. Si se devuelve el puntero de interfaz del objeto primario, el cliente llama a las propiedades y los métodos del elemento primario para obtener información sobre el elemento secundario que generó el evento.

**AccessibleObjectFromPoint**

Para recuperar la dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un objeto en un punto especificado de la pantalla, los clientes utilizan la función [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) .

**AccessibleObjectFromWindow**

Para recuperar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un objeto desde un identificador de ventana, los clientes utilizan la función [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

Es posible que los servidores devuelvan punteros de interfaz distintos para el mismo elemento de la interfaz de usuario cada vez que se llame a la función [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . Para determinar si dos punteros hacen referencia al mismo elemento de la interfaz de usuario, los desarrolladores de cliente deben comparar las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto, no los punteros.

 

 
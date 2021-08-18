---
title: Obtener un puntero de interfaz de objeto accesible
description: Microsoft Active Accessibility aplicaciones cliente recuperan punteros de interfaz a objetos accesibles mediante una de las siguientes funciones.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994205"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Obtener un puntero de interfaz de objeto accesible

Microsoft Active Accessibility aplicaciones cliente recuperan punteros de interfaz a objetos accesibles mediante una de las siguientes funciones.

**AccessibleObjectFromEvent**

Muchos clientes buscan información sobre objetos accesibles específicos que generan eventos. Dado que [**la interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es la "puerta de enlace" a los objetos [accesibles,](winevents-overview.md) los clientes deben tener una manera fácil de asociar WinEvents a la interfaz **IAccessible** del objeto que genera los eventos. Microsoft Active Accessibility proporciona la [**función AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) específicamente para este propósito.

> [!Note]  
> Los clientes [con funciones de enlace en contexto](in-context-hook-functions.md) deben llamar a la función [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) antes de llamar [**a AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

La [**función AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) acepta gran parte de la misma información que recibe la función [*de enlace de un*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) cliente. Cuando una función de enlace de cliente recibe una notificación de eventos, pasa los parámetros adecuados de los eventos **a AccessibleObjectFromEvent**.

La función recupera la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento de interfaz de usuario que generó el evento o la interfaz del objeto primario del elemento. Si se devuelve el puntero de interfaz del objeto primario, el cliente llama a las propiedades y métodos del elemento primario para obtener información sobre el elemento secundario que generó el evento.

**AccessibleObjectFromPoint**

Para recuperar la dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un objeto en un punto especificado de la pantalla, los clientes usan la [**función AccessibleObjectFromPoint.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

**AccessibleObjectFromWindow**

Para recuperar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un objeto desde un identificador de ventana, los clientes usan la [**función AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

Es posible que los servidores devuelvan punteros de interfaz distintos para el mismo elemento de interfaz de usuario cada vez que se llama a la función [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) Para determinar si dos punteros hacen referencia al mismo elemento de interfaz de usuario, los desarrolladores de cliente deben comparar las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto, no los punteros.

 

 
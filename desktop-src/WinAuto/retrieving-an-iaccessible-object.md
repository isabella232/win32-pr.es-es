---
title: Recuperar un objeto IAccessible
description: Microsoft Active Accessibility proporciona funciones como AccessibleObjectFromWindow y AccessibleObjectFromPoint que permiten a los clientes recuperar objetos accesibles.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356801"
---
# <a name="retrieving-an-iaccessible-object"></a>Recuperar un objeto IAccessible

Microsoft Active Accessibility proporciona funciones como [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) que permiten a los clientes recuperar objetos accesibles. Estas funciones devuelven un puntero de la interfaz [**IDispatch**](idispatch-interface.md) o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a través del cual los clientes obtienen información sobre el objeto accesible.

Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las otras funciones **AccessibleObjectFrom * * * X* que recuperan una interfaz en un objeto, Microsoft Active Accessibility envía el mensaje de ventana de la ventana de mensajes [**\_ GETOBJECT de WM**](wm-getobject.md) al procedimiento de ventana aplicable dentro de la aplicación correspondiente. Para proporcionar información a los clientes, los servidores deben responder al mensaje de la **\_ GETOBJECT de WM** .

Para recopilar información específica acerca de un elemento de la interfaz de usuario, los clientes deben recuperar primero una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento. Para recuperar el objeto **IAccessible** de un elemento, los clientes pueden utilizar una de las funciones siguientes:

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Para recuperar un puntero de interfaz IAccessible**

1.  El cliente llama a una de las funciones **AccessibleObjectFrom * * * X* .
2.  Oleacc.dll envía un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) al servidor.
3.  El servidor determina qué elemento de la interfaz de usuario corresponde a la solicitud.
4.  El servidor devuelve cero para solicitar un proxy de Oleacc.dll,

    O bien

    Devuelve un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementación nativa). Para ello, haga lo siguiente:

    -   Construye un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento.
    -   Llama a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) para calcular las referencias del puntero del objeto.
    -   Devuelve LRESULT que se va a Oleacc.dll.

5.  Oleacc.dll examina el valor devuelto de [**WM \_ GETOBJECT**](wm-getobject.md).

    Si es cero, Oleacc.dll crea un objeto proxy y lo devuelve al cliente.

    O bien

    Si es distinto de cero, Oleacc.dll llama a [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) para anular las referencias del puntero de objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo y lo devuelve al cliente.

 

 





---
title: Recuperar un objeto IAccessible
description: Microsoft Active Accessibility proporciona funciones como AccessibleObjectFromWindow y AccessibleObjectFromPoint que permiten a los clientes recuperar objetos accesibles.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e490b743799705dd4022f8d3ea6658de2ac9f5d996da736a151bc0c74ee8e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122125"
---
# <a name="retrieving-an-iaccessible-object"></a>Recuperar un objeto IAccessible

Microsoft Active Accessibility proporciona funciones como [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) que permiten a los clientes recuperar objetos accesibles. Estas funciones devuelven un puntero de [**interfaz IDispatch**](idispatch-interface.md) o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a través del cual los clientes obtienen información sobre el objeto accesible.

Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las demás funciones **AccessibleObjectFrom**_X_ que recuperan una interfaz para un objeto , Microsoft Active Accessibility envía el mensaje de ventana [**WM \_ GETOBJECT**](wm-getobject.md) al procedimiento de ventana aplicable dentro de la aplicación adecuada. Para proporcionar información a los clientes, los servidores deben responder al **\_ mensaje GETOBJECT de WM.**

Para recopilar información específica sobre un elemento de interfaz de usuario, los clientes deben recuperar primero una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento. Para recuperar el objeto **IAccessible** de un elemento, los clientes pueden usar una de las siguientes funciones:

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Para recuperar un puntero de interfaz IAccessible**

1.  El cliente llama a una de **las funciones AccessibleObjectFrom**_X._
2.  Oleacc.dll envía un [**mensaje \_ GETOBJECT de WM**](wm-getobject.md) al servidor.
3.  El servidor determina qué elemento de la interfaz de usuario corresponde a la solicitud.
4.  El servidor devuelve cero para solicitar un Oleacc.dll proxy,

    Or

    Devuelve un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementación nativa). Para ello, hace lo siguiente:

    -   Construye un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento .
    -   Llama [**a LresultFromObject para**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) serializar el puntero del objeto.
    -   Devuelve el valor LRESULT que se Oleacc.dll.

5.  Oleacc.dll examina el valor devuelto de [**WM \_ GETOBJECT**](wm-getobject.md).

    Si es cero, Oleacc.dll crea un objeto proxy y lo devuelve al cliente.

    Or

    Si es distinto de cero, Oleacc.dll a [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) para desmarshal el puntero de objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo y lo devuelve al cliente.

 

 





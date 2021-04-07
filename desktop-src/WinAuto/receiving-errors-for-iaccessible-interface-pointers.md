---
title: Recibir errores de punteros de interfaz IAccessible
description: En este tema se describen situaciones en las que podría recibir un error de un puntero de interfaz IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903675"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Recibir errores de punteros de interfaz IAccessible

En este tema se describen situaciones en las que podría recibir un error de un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Las funciones **IAccessible** pueden devolver errores para los punteros de interfaz **IAccessible** cuando un usuario cierra una aplicación a la que pertenece el objeto, o si un usuario descarta un control a través de la interfaz de usuario.

## <a name="user-closes-an-application"></a>El usuario cierra una aplicación

Si un usuario cierra la aplicación que contiene un objeto al que señala el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , todas las llamadas futuras a ese objeto devolverán un código de error. El error, como **Co \_ E \_ OBJNOTCONNECTED**, indicará que el objeto ya no existe. Esto se aplica a todos los punteros de interfaz **IAccessible** .

## <a name="user-dismisses-a-control"></a>El usuario descarta un control

Si un usuario descarta un control (por ejemplo, presionando un botón de método de presionado), los clientes pueden seguir llamando a métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en este objeto porque el objeto no se ha liberado. Sin embargo, las llamadas futuras recibirán mensajes de error.

Esta situación se aplica a las siguientes funciones y métodos:

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 





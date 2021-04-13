---
title: Protección contra reentrada en funciones de enlace
description: Mientras una función de enlace procesa un evento, se pueden desencadenar eventos adicionales, lo que puede hacer que la función de enlace se vuelva a escribir antes de que finalice el procesamiento del evento original.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421174"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Protección contra reentrada en funciones de enlace

Mientras una función de enlace procesa un evento, se pueden desencadenar eventos adicionales, lo que puede hacer que la función de enlace se vuelva a escribir antes de que finalice el procesamiento del evento original. El problema con la reentrada en las funciones de enlace es que los eventos se completan fuera de secuencia, a menos que la función de enlace controle esta situación.

Por ejemplo, considere un caso en el que una función de enlace en un programa lector de pantalla está procesando el evento [**\_ \_ VALUECHANGE del objeto de evento**](event-constants.md) para un control de edición. Si, al procesar el primer evento de cambio de valor, se vuelve a escribir la función de enlace para procesar un evento de cambio de valor subsiguiente, el segundo evento se completa antes del primer evento. Esta situación da lugar a que el lector de pantalla transmita información incorrecta al usuario.

Dado que se interrumpe el procesamiento de eventos, es posible que se reciban eventos adicionales cada vez que la función de enlace llame a una función que provoque que la cola de mensajes del subproceso propietario se compruebe. Esto sucede cuando se llama a cualquiera de los siguientes elementos dentro de la función de enlace:

-   La función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage), [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea), [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)o [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) de Windows
-   Microsoft Active Accessibility Functions [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) u otro método o propiedad del modelo de objetos componentes (com) que cruza los límites del proceso

Dado que las funciones de enlace llaman a métodos y propiedades [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) y [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , no es posible evitar la reentrada. La única solución es que los desarrolladores de cliente agreguen código en la función de enlace que detecte la reentrada y tome las medidas adecuadas si se vuelve a escribir la función de enlace.

 

 
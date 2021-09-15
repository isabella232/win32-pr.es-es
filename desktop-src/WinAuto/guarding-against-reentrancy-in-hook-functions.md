---
title: Protección contra la reenencia en funciones de enlace
description: Mientras una función de enlace procesa un evento, se pueden desencadenar eventos adicionales, lo que puede hacer que la función de enlace vuelva a escribirse antes de que finalice el procesamiento del evento original.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568536"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Protección contra la reenencia en funciones de enlace

Mientras una función de enlace procesa un evento, se pueden desencadenar eventos adicionales, lo que puede hacer que la función de enlace vuelva a escribirse antes de que finalice el procesamiento del evento original. El problema con la reenencia en las funciones de enlace es que los eventos se completan fuera de la secuencia a menos que la función de enlace controle esta situación.

Por ejemplo, considere un caso en el que una función de enlace de un programa de lector de pantalla está procesando el evento [**EVENT \_ OBJECT \_ VALUECHANGE**](event-constants.md) para un control de edición. Si, al procesar el primer evento de cambio de valor, la función de enlace se vuelve a escribir para procesar un evento de cambio de valor posterior, el segundo evento se completa antes del primer evento. Esta situación hace que el lector de pantalla transmita información inexacta al usuario.

Dado que se interrumpe el procesamiento de eventos, se pueden recibir eventos adicionales cada vez que la función de enlace llama a una función que hace que se comprueba la cola de mensajes del subproceso propietario. Esto sucede cuando se llama a cualquiera de los siguientes elementos dentro de la función de enlace:

-   La Windows [**función SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) [**GetMessage,**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**PeekMessage,**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) [**o MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)
-   El Microsoft Active Accessibility funciones [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) u otra propiedad o método del Modelo de objetos componentes (COM) que cruza los límites del proceso

Dado que las funciones de enlace llaman a las propiedades y métodos [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**e IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no es posible evitar la reenlazancia. La única solución es que los desarrolladores cliente agreguen código en la función de enlace que detecte la reentreencia y tomen las medidas adecuadas si se vuelve a escribir la función de enlace.

 

 
---
title: Cómo funciona WM_GETOBJECT
description: Microsoft Active Accessibility envía el mensaje de WM \_ GETOBJECT a la aplicación de servidor adecuada cuando un cliente llama a una de las funciones de AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe287bca68c925cb7be95ff52d2dac547ed097
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359023"
---
# <a name="how-wm_getobject-works"></a>Cómo \_ funciona WM GETOBJECT

Microsoft Active Accessibility envía el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a la aplicación de servidor adecuada cuando un cliente llama a una de las funciones **AccessibleObjectFrom * * * X* . En la lista siguiente se describen los distintos escenarios que se producen:

-   Si la ventana o el control que [**recibe \_ WM GETOBJECT**](wm-getobject.md) implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la ventana devuelve una referencia a la interfaz **IAccessible** mediante [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, junto con la biblioteca del modelo de objetos componentes (COM), realiza el cálculo de referencias adecuado y pasa el puntero de interfaz del servidor de vuelta al cliente.
-   Si la ventana que recibe el mensaje no implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), debe devolver cero.
-   Si la ventana no controla el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) , la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) devuelve cero.

Aunque el servidor devuelva cero, Microsoft Active Accessibility sigue facilitando al cliente información sobre el objeto. Para la mayoría de los objetos proporcionados por el sistema, como cuadros de lista y botones, Microsoft Active Accessibility proporciona información completa. en el caso de otros objetos, la información está limitada. Por ejemplo, Microsoft Active Accessibility no proporciona información para los controles que no tienen un identificador de ventana. Microsoft Active Accessibility devuelve un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de proxy que el cliente utiliza para obtener información sobre el objeto.

Para obtener más información, consulte [el \_ mensaje de WM GETOBJECT](the-wm-getobject-message.md).

 

 
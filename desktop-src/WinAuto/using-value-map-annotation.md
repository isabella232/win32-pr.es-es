---
title: Usar anotación de asignación de valores
description: Para ver el código de ejemplo, consulte ejemplo de anotación de asignación de valores.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420769"
---
# <a name="using-value-map-annotation"></a>Usar anotación de asignación de valores

**Para crear un mapa de valores**

1.  **Cree una cadena de asignación.**

    Una cadena de asignación es una lista de valores numéricos de un control que corresponden a una cadena legible en Unicode. Comienza por "A:" seguido de un número que indica el tipo de índice utilizado. Solo se admiten índices de imagen; por lo tanto, el tipo de índice es siempre 0.

    La cadena va seguida de los pares: index: result. El "índice" es un número que representa un índice de imagen para un List-View o vista de árbol, o el valor de un control deslizante.

    El valor resultante es un número obtenido al asignar la propiedad role o State para una vista de lista o un control de vista de árbol. Estos números se expresan en formato decimal o hexadecimal con un prefijo "0x".

    La cadena de asignación siempre termina con un signo de dos puntos (":").

    A continuación se muestra un ejemplo de una asignación de anotación para las propiedades de estado y de rol de una casilla en una vista de lista o un control de vista de árbol. Hay dos elementos en la vista que representan casillas, y cada uno tiene imágenes correspondientes al estado Checked y Unchecked.

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    Para los valores de rol y estado válidos, vea [funciones de objeto](object-roles.md) y [constantes de estado de objeto](object-state-constants.md).

    El valor de índice puede ser negativo cuando se asignan propiedades para un control deslizante.

    Cuando se asigna una propiedad Value o Description, el resultado es una cadena. Las cadenas no se incluyen entre comillas y los dos puntos actúan como delimitadores.

    Para obtener más información, vea [formato de asignación de anotaciones](value-map-annotation.md).

2.  **Cree el administrador de anotaciones y obtenga un puntero a su** interfaz [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**

    El siguiente es un ejemplo de cómo crear el administrador de anotaciones.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Adjunte la cadena de asignación al control.**

    Llame a [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), pasando el **hWnd** del control y un puntero a la cadena de asignación.

    El parámetro *IdProp* será uno de los siguientes.

    

    | Parámetro                   | Se usa para                                                |
    |-----------------------------|---------------------------------------------------------|
    | MSAAPROPID \_ ROLEMAP         | Para establecer un mapa de roles para los controles de vista de lista o de vista de árbol.  |
    | MSAAPROPID \_ STATEMAP        | Para establecer un mapa de estado para los controles de vista de lista o de vista de árbol. |
    | DESCRIPTIONMAP de la \_ ACC \_ | Para establecer un mapa de descripción para las vistas de lista o de árbol.   |
    | MSAAPROPID \_ VALUEMAP        | Para establecer un mapa de valores en los controles deslizantes.                  |

    

     

4.  **Limpieza.**

    Antes de destruir los controles anotados de asignación de valores (por ejemplo, al controlar [WM \_ Destroy](../winmsg/wm-destroy.md)), debe borrar las propiedades registradas anteriormente y liberar el administrador de anotaciones.

    Para ello, llame a [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) según corresponda y suelte el puntero a [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).

Para ver el código de ejemplo, consulte [ejemplo de anotación de asignación de valores](value-map-annotation-sample.md).

 

 
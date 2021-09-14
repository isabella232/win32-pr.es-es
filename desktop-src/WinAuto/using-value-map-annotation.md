---
title: Usar anotación de mapa de valores
description: Para obtener código de ejemplo, vea Ejemplo de anotación de mapa de valores.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253203"
---
# <a name="using-value-map-annotation"></a>Usar anotación de mapa de valores

**Para crear un mapa de valores**

1.  **Cree una cadena de asignación.**

    Una cadena de asignación es una lista de valores numéricos de un control correspondientes a una cadena legible en Unicode. Comienza con "A:" seguido de un número que indica el tipo de índice utilizado. Solo se admiten índices de imagen; por lo tanto, el tipo de índice siempre es 0.

    La cadena va seguida de pares :index:result. El "índice" es un número que representa un índice de imagen para un List-View o Tree-View, o el valor de un control deslizante.

    El valor resultante es un número obtenido al asignar la propiedad Role o State para una vista de lista o un control de vista de árbol. Estos números se expresan en decimal o hexadecimal con un prefijo "0x".

    La cadena de asignación siempre termina con dos puntos finales (":").

    A continuación se muestra un ejemplo de un mapa de anotaciones para las propiedades Estado y Rol de una casilla en una vista de lista o control de vista de árbol. Hay dos elementos en la vista que representan casillas y cada uno tiene imágenes correspondientes al estado activado y desactivado.

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

    

    Para obtener valores válidos de Rol y Estado, vea [Roles de objeto](object-roles.md) y Constantes de estado de [objeto](object-state-constants.md).

    El valor del índice puede ser negativo al asignar las propiedades de un control deslizante.

    Al asignar una propiedad Value o Description, el resultado es una cadena. Las cadenas no se entrecomillan y los dos puntos actúan como delimitadores.

    Para obtener más información, vea [Annotation Map Format](value-map-annotation.md).

2.  **Cree el administrador de anotaciones y obtenga un puntero a su** interfaz [**IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)

    A continuación se muestra un ejemplo de cómo crear el administrador de anotaciones.

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **Adjunte la cadena de asignación al control .**

    Llame [**a IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), pasando el **HWND** del control y un puntero a la cadena de asignación.

    El *parámetro IdProp* será uno de los siguientes.

    

    | Parámetro                   | Se usa para                                                |
    |-----------------------------|---------------------------------------------------------|
    | MAPA DE ROLES MSAAPROPID \_         | Para establecer un mapa de roles para los controles de vista de lista o vista de árbol.  |
    | MSAAPROPID \_ STATEMAP        | Para establecer un mapa de estado para los controles de vista de lista o vista de árbol. |
    | PROPID \_ ACC \_ DESCRIPTIONMAP | Para establecer un mapa de descripción para vistas de lista o de árbol.   |
    | MSAAPROPID \_ VALUEMAP        | Para establecer un mapa de valores en los controles deslizantes.                  |

    

     

4.  **Limpiar.**

    Antes de destruir los controles anotados de asignación de valores (por ejemplo, al controlar [WM \_ DESTROY),](../winmsg/wm-destroy.md)debe borrar las propiedades registradas previamente y liberar el administrador de anotaciones.

    Para ello, llame a [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) según corresponda y suelte el puntero a [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).

Para obtener código de ejemplo, vea [Ejemplo de anotación de mapa de valores](value-map-annotation-sample.md).

 

 
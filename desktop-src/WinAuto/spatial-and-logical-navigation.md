---
title: Navegación espacial y lógica
description: Los clientes recuperan información sobre un objeto que está cerca o lógicamente cerca de otro objeto dentro del mismo contenedor llamando a IAccessible accNavigate y especificando una de las constantes de navegación.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714433"
---
# <a name="spatial-and-logical-navigation"></a>Navegación espacial y lógica

Los clientes recuperan información sobre un objeto que está cerca o lógicamente cerca de otro objeto dentro del mismo contenedor llamando a [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) y especificando una de las [constantes de navegación](navigation-constants.md).

Con los clientes de *navegación espacial* , navegue a un objeto basado en su ubicación en la pantalla. Los clientes navegan hacia arriba, hacia abajo, a la izquierda o a la derecha desde el objeto actual para obtener información sobre otro objeto dentro del mismo contenedor.

Con los clientes de *navegación lógicos* , navega hasta el objeto que precede lógicamente o sigue a otro objeto, según lo determinado por el servidor. Los clientes navegan a todos los elementos secundarios de un objeto de dos maneras:

-   Inicie la navegación con [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) y, a continuación, llame repetidamente al método con [**NAVDIR \_ Next**](navigation-constants.md).
-   Inicie la navegación con [**NAVDIR \_ LASTCHILD**](navigation-constants.md) y llame repetidamente al método con [**NAVDIR \_ anterior**](navigation-constants.md).

Independientemente de la dirección, la navegación visita cada elemento secundario visible que pertenece al objeto primario. Los elementos secundarios invisibles se pueden omitir con navegación lógica. Además, cada elemento secundario se visita una sola vez y la navegación no se repite. Es decir, el método produce un error si un cliente intenta navegar antes del primer objeto o después del último objeto.

La navegación espacial y lógica está relacionada. Por ejemplo, en una barra de herramientas horizontal, al llamar al método con [**NAVDIR \_ right**](navigation-constants.md) deberían producirse los mismos resultados que al llamar al método con [**NAVDIR \_ Next**](navigation-constants.md).

El objeto inicial de la navegación es el objeto **propio o uno de los elementos secundarios del objeto, excepto cuando** se especifica [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LASTCHILD**](navigation-constants.md) ; en este caso, la navegación debe comenzar por el propio objeto.

Si un cliente navega desde un objeto accesible a un elemento de la interfaz de usuario relacionado, o si el miembro **lVal** de *varStart* es **CHILDID \_ Self** y el marcador especificado en *navDir* es cualquier marcador de navegación excepto [**navDir \_ FIRSTCHILD**](navigation-constants.md) o [**navDir \_ LASTCHILD**](navigation-constants.md), el resultado en *pvarEnd* es un identificador secundario o una interfaz [**IDispatch**](idispatch-interface.md) . Si *pvarEnd* contiene un identificador secundario, los clientes primero deben obtener un puntero a la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento primario para navegar desde este elemento de la interfaz de usuario o para obtener más información sobre él. Para obtener el objeto primario, los clientes llaman a la propiedad [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del objeto relacionado o al objeto inicial de la navegación.

Tenga en cuenta que los clientes deben tener información sobre todos los objetos flotantes mediante una llamada a la función [**EnumChildWindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) . Dado que un objeto flotante no se recorta a su elemento primario, los clientes no tienen información sobre la relación jerárquica entre dos objetos cerca de otro en la pantalla.

El gráfico siguiente es un ejemplo de un objeto flotante que no se recorta a su elemento primario.

![captura de pantalla de la ventana abierta flotando encima de una ventana más grande de Microsoft Developer Studio](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Establecer el orden en la navegación lógica

En la navegación lógica, los desarrolladores que diseñan los objetos establecen las relaciones entre ellos. La navegación lógica es más subjetiva que la navegación espacial. Además, el orden en la navegación lógica no es el mismo que el orden que se usa con los identificadores secundarios.

En el caso de los objetos que tienen ubicaciones de pantalla, los desarrolladores de servidor deben establecer el orden de navegación de la forma en que la mayoría de los usuarios considerarían lógicos. Por ejemplo, en países o regiones de habla inglesa, esto significa una ordenación de izquierda a derecha y de arriba a abajo.

El orden de navegación lógico debe estar en paralelo en el orden de navegación del teclado. Por ejemplo, un cuadro de diálogo contiene los botones **Aceptar** y **Cancelar** y algunos controles de edición. Un cliente que llama a [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para desplazarse al objeto siguiente o anterior de ese cuadro de diálogo se mueve en el mismo orden que un usuario que presiona tab o Mayús + Tab para mover el foco entre elementos.

En el caso de los objetos que no tienen ubicaciones de pantalla definidas, el orden lógico lo deciden los desarrolladores de servidores y los desarrolladores de cliente no deben realizar suposiciones sobre él. Por ejemplo, es aceptable que los objetos no visibles, como los objetos que solo están ocultos temporalmente, se intercalan con objetos visibles.

 

 
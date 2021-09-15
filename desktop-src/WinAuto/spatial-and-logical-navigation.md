---
title: Navegación espacial y lógica
description: Los clientes recuperan información sobre un objeto que está espacial o lógicamente cerca de otro objeto dentro del mismo contenedor llamando a IAccessible accNavigate y especificando una de las constantes de navegación.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567368"
---
# <a name="spatial-and-logical-navigation"></a>Navegación espacial y lógica

Los clientes recuperan información sobre un objeto que está espacial o lógicamente cerca de otro objeto dentro del mismo contenedor llamando a [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) y especificando una de las constantes de [navegación](navigation-constants.md).

Con *la navegación espacial,* los clientes navegan a un objeto en función de su ubicación en la pantalla. Los clientes navegan hacia arriba, hacia abajo, a la izquierda o a la derecha desde el objeto actual para obtener información sobre otro objeto dentro del mismo contenedor.

Con *los clientes de* navegación lógica, navegue hasta el objeto que precede o sigue lógicamente a otro objeto, determinado por el servidor. Los clientes navegan a todos los secundarios de un objeto de dos maneras:

-   Inicie la navegación con [**NAVDIR \_ FIRSTCHILD y,**](navigation-constants.md) a continuación, llame repetidamente al método [**con NAVDIR \_ NEXT**](navigation-constants.md).
-   Inicie la navegación [**con NAVDIR \_ LASTCHILD y**](navigation-constants.md) llame repetidamente al método con [**NAVDIR \_ PREVIOUS**](navigation-constants.md).

Independientemente de la dirección, la navegación visita cada elemento secundario visible que pertenece al objeto primario. Los elementos secundarios invisibles se pueden omitir con la navegación lógica. Además, cada elemento secundario se visita una sola vez y la navegación no se recorre en bucle. Es decir, se produce un error en el método si un cliente intenta navegar antes del primer objeto o después del último objeto.

La navegación espacial y lógica están relacionadas. Por ejemplo, en una barra de herramientas horizontal, la llamada al método con [**NAVDIR \_ RIGHT**](navigation-constants.md) debe producir los mismos resultados que llamar al método [**con NAVDIR \_ NEXT**](navigation-constants.md).

El objeto inicial de la navegación es el propio objeto o uno de los elementos secundarios del **objeto,** excepto cuando se especifica [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LASTCHILD;**](navigation-constants.md) en este caso, la navegación debe comenzar desde el propio objeto.

Si un cliente navega desde un objeto accesible a un elemento de interfaz de usuario relacionado, o si el miembro **lVal** de *varStart* es **CHILDID \_ SELF** y la marca especificada en *navDir* es cualquier marca de navegación excepto [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) o [**NAVDIR \_ LASTCHILD,**](navigation-constants.md)el resultado en *pvarEnd* es un identificador secundario o una [**interfaz IDispatch.**](idispatch-interface.md) Si *pvarEnd* contiene un identificador secundario, los clientes deben obtener primero un puntero a la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento primario para navegar desde este elemento de interfaz de usuario o para obtener más información sobre él. Para obtener el objeto primario, los clientes llaman a la propiedad [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) del objeto relacionado o al objeto inicial de la navegación.

Tenga en cuenta que los clientes deben tener información sobre todos los objetos flotantes llamando a [**la función EnumChildWindows.**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) Dado que un objeto flotante no se recorta a su elemento primario, los clientes no tienen información sobre la relación jerárquica entre dos objetos cercanos entre sí en la pantalla.

El gráfico siguiente es un ejemplo de un objeto flotante que no se recorta a su elemento primario.

![captura de pantalla de la ventana abierta flotante sobre una ventana de Microsoft Developer Studio más grande](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Establecimiento del orden en la navegación lógica

En la navegación lógica, los desarrolladores que diseñan los objetos establecen las relaciones entre ellos. La navegación lógica es más subjetiva que la navegación espacial. Además, el orden en la navegación lógica no es el mismo que el que se usa con los iD secundarios.

En el caso de los objetos que tienen ubicaciones de pantalla, los desarrolladores de servidores deben establecer el orden de navegación de la manera en que la mayoría de los usuarios considerarían lógico. En países o regiones de habla inglesa, por ejemplo, esto significa una ordenación de izquierda a derecha, de arriba a abajo.

El orden de navegación lógico debe ser el orden de navegación del teclado paralelo. Por ejemplo, un cuadro de diálogo contiene los botones de inserción **Aceptar** y **Cancelar** y algunos controles de edición. Un cliente que llama a [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para navegar al objeto siguiente o anterior de ese cuadro de diálogo se mueve en el mismo orden que un usuario que presiona TAB o MAYÚS+TAB para mover el foco entre los elementos.

En el caso de los objetos que no tienen ubicaciones de pantalla definidas, los desarrolladores de servidores deciden el orden lógico y los desarrolladores de cliente no deben hacer suposiciones al respecto. Por ejemplo, es aceptable que los objetos no visibles, como los objetos que solo están ocultos temporalmente, se intersen con objetos visibles.

 

 
---
title: Implementación de un Interfaz de usuario
description: En esta sección se describen algunas de las tareas asociadas a la implementación de una interfaz de usuario para una Windows aplicación.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7967474781e180ab29a42fce6884cc391515eef0211107852659eace3490e712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702345"
---
# <a name="implementing-a-user-interface"></a>Implementación de un Interfaz de usuario

En esta sección se describen algunas de las tareas asociadas a la implementación de una interfaz de usuario para una Windows aplicación.

-   [Prototipo](#prototype)
-   [Construir](#construct)
-   [Simplificar](#simplify)
    -   [Reducir, reutilizar, Declutter](#reduce-reuse-declutter)
    -   [La mejor interfaz de usuario es sin interfaz de usuario](#the-best-ui-is-no-ui)
    -   [Menos interfaz de usuario es mejor interfaz de usuario](#less-ui-is-better-ui)
    -   [La interfaz de usuario coherente es una buena interfaz de usuario](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototipo

Las interfaces de usuario (UI) deben diseñarse a partir de la lista de escenarios y requisitos de usuario que se identificaron en el paso de análisis de usuarios.

Los prototipos pueden ser tan simples como los bocetos de lápiz o tan complejos como las simulaciones de pantalla interactivas. Mantenga todo el trabajo anterior, ya que puede ser útil al mostrar a las partes interesadas las alternativas que se consideraron y explicar por qué se descartaron.

Intente limitar este paso a dos o tres prototipos como máximo. Los prototipos no tienen que ser exhaustivos; solo tienen que simular de forma eficaz la experiencia de uso de la aplicación real.

Demostrar los prototipos y realizar un seguimiento de los comentarios de los usuarios para ayudar a identificar las tendencias generales de facilidad de uso. Si es posible, descarte los prototipos menos correctos e incorpore tantos comentarios útiles como sea posible en uno o varios de los prototipos restantes. Repita este proceso a medida que el tiempo y los recursos lo permitan.

Hay varias herramientas de creación de prototipos disponibles, como [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) en Microsoft Expression Studio 3, el editor de diseño de Microsoft Visual Studio e incluso Microsoft Paint.

## <a name="construct"></a>Construcción

Al implementar la interfaz de usuario para una aplicación, tenga en cuenta lo siguiente:

-   Estructura de comandos

    Determine si se debe implementar una estructura de comandos tradicional basada en menús y barras de herramientas, o una estructura de comandos alternativa basada en el marco Windows cinta de opciones. Para obtener más información, vea [Menús,](../menurc/menus.md) [barras de herramientas](../controls/toolbar-control-reference.md)y Windows marco de la cinta de [opciones](../windowsribbon/-uiplat-windowsribbon-entry.md).

-   Windows y cuadros de diálogo

    En función del diseño de la interfaz de usuario y del trabajo de creación de prototipos, implemente las ventanas de aplicación, incluidas la ventana principal, las ventanas secundarias, los cuadros de diálogo y los cuadros de mensaje. Siga las directrices de UX para determinar qué estilos y controles usar en las ventanas y los cuadros de diálogo. Para obtener más información, [vea Windows](../winmsg/windows.md), Cuadros [de diálogo](../dlgbox/dialog-boxes.md)y Windows [controles](../controls/window-controls.md).

-   Controles personalizados

    Cree nuevos controles personalizados solo si no puede obtener la funcionalidad que desea de uno de los controles Windows estándar. Los nuevos controles personalizados son muy costosos de desarrollar y requieren trabajo adicional para que sean accesibles. Si la aplicación requiere controles personalizados, asegúrese de que están expuestos adecuadamente a las tecnologías de asistencia. Para obtener más información, vea [Controles personalizados](../controls/user-controls-intro.md) [y Windows Automation API](../winauto/windows-automation-api-portal.md).

-   Compatibilidad con dispositivos de entrada de usuario estándar

    La mayoría Windows aplicaciones necesitan admitir la entrada del usuario a través del teclado y el mouse. La capacidad de navegar y acceder a toda la funcionalidad de la aplicación solo a través del teclado es especialmente importante para los usuarios con discapacidades visuales o con problemas de movilidad. Para obtener más información, vea [Entrada de usuario](../inputdev/user-input.md) y el libro electrónico Software de ingeniería para [accesibilidad](https://www.microsoft.com/download/details.aspx?id=19262).

-   Estilos visuales, animaciones y efectos visuales

    Windows incluye varias tecnologías que puede usar para agregar interés visual y diferenciar la interfaz de usuario de la de otras aplicaciones. Entre ellas se incluyen la especificación de los estilos visuales de los controles, la adición de animaciones a los elementos de la interfaz de usuario y la implementación de diversos efectos visuales en la interfaz de usuario. Para obtener más información, [vea Visual Styles](../controls/themes-overview.md), Windows Animation [Manager](../uianimation/-main-portal.md)y [Administrador de ventanas de escritorio](../dwm/dwm-overview.md).

## <a name="simplify"></a>Simplificación de 

Una experiencia de usuario correcta depende del enfoque, la perspectiva y las suposiciones del desarrollador durante el proceso de diseño. Lograr una comprensión básica de cómo la audiencia de destino puede usar una aplicación requiere la capacidad de pensar ampliamente, más allá de las restricciones de lo que se adapta a las necesidades del desarrollador. Invertir este tiempo, esfuerzo e investigación al principio de un proyecto pagará dividendos al final.

### <a name="reduce-reuse-declutter"></a>Reducir, reutilizar, Declutter

Las características solo mejoran un producto si se usan realmente. En muchos casos, la proliferación de características puede introducir complejidad con la adición de más iconos, elementos de menú, barras de herramientas y cuadros de diálogo que interfieren con la eficacia y la productividad en lugar de agregar valor.

### <a name="the-best-ui-is-no-ui"></a>La mejor interfaz de usuario es sin interfaz de usuario

La interfaz de usuario implica que el usuario tiene que interactuar con la aplicación para que suceda algo. En el caso ideal, no es necesaria ninguna interacción. Desde la perspectiva del usuario, solo funciona. Si se puede agregar una característica que elimina de forma segura una interacción del usuario, hace que la experiencia del usuario sea significativamente mejor.

### <a name="less-ui-is-better-ui"></a>Menos interfaz de usuario es mejor interfaz de usuario

En muchos casos, no es posible quitar completamente la interacción de la interfaz de usuario de la experiencia del usuario. Sin embargo, mientras menos interacción del usuario requiera una aplicación, mejor.

Identifique las actividades más comunes y esenciales que realizarán los usuarios con la aplicación y haga que esas funciones sea la más destacada en la interfaz de usuario. Relegue otras funciones y actividades a un estado menor, ya sea visual, jerárquicamente o a través de la configuración opcional de la aplicación y las preferencias del usuario.

-   Reemplazar en lugar de agregar

    La conservación de la regla de interfaz de usuario indica que se agrega algo solo cuando se puede quitar algo. Esta regla obliga a un desarrollador a pensar críticamente en una nueva característica teniendo en cuenta el impacto que la característica tiene en toda la experiencia del usuario.

    No se deben promover nuevas características porque son nuevas: no confunda el marketing con la facilidad de uso. Para ayudar a los usuarios a encontrar nuevas  características en el producto, agregue un elemento al menú Ayuda que describa los cambios que se han producido desde la última versión de la aplicación.

-   El usuario es un recurso limitado

    Cuanto más funcionalidad se exponga en cualquier momento, más difícil será para un usuario encontrar la funcionalidad que necesita.

-   It's Rude to Interrupt

    Cuando una aplicación muestra un cuadro de diálogo, obliga al usuario a detener lo que está haciendo y prestar atención a otra cosa. Si es posible, quite la necesidad de un cuadro de diálogo completamente evitando casos de error y otras experiencias de usuario perjudiciales. Para obtener más información sobre las directrices de mensaje, vea [Mensajes](https://msdn.microsoft.com/library/dd535525.aspx).

-   Simple puede ser eficaz

    Una interfaz de usuario simple no implica una falta de funcionalidad. Normalmente, el resultado de una interfaz de usuario más sencilla es una curva de aprendizaje acortada, una mayor eficacia y una productividad mejorada. Esto permite a un usuario aumentar su competencia con la aplicación.

### <a name="consistent-ui-is-good-ui"></a>La interfaz de usuario coherente es una buena interfaz de usuario

Por lo general, se recomienda procurar la coherencia en toda la interfaz de usuario de una aplicación. Proporcionar una interfaz de usuario coherente permite que un usuario sea más eficaz con una aplicación en un tiempo mucho más corto. Pueden aplicar sus conocimientos existentes de la aplicación a distintas situaciones y usar funcionalidades desconocidas con confianza.

En raras ocasiones, la coherencia no proporciona ninguna ventaja al usuario e incluso puede degradar la experiencia del usuario. No haga que la interfaz de usuario sea coherente si esa coherencia afecta a la capacidad de realizar una tarea. La coherencia en sí misma no garantiza la facilidad de uso. Es un error pensar que la coherencia en la interfaz dará lugar a un buen diseño.

Por ejemplo, la interfaz de usuario del juego de vídeo suele ser muy específica del tipo de juego. Intentar diseñar una interfaz de usuario genérica que funcione bien para dos juegos especializados, uno que requiera una rueda de ruedas y otro que funcione mejor con un botón y un botón, probablemente no vaya a ser correcto para ninguno de los dos juegos. En el mejor de los casos, es probable que se alcance un punto medio que no sea bueno para ninguno de los dos.

Tener buenos datos sobre cómo se usan las cosas es la clave para tomar esta decisión. Tenga claros los ventajas y desventajas de cada desventaja (velocidad frente a confiabilidad, facilidad de aprendizaje frente a dominio experto, coherencia global frente a optimización local) y tome las mejores decisiones para la característica en relación con todo el producto.

El diseño es elegir cómo producir un error: la optimización de una cosa significa que se producirá un error en otra. La clave para un buen diseño de la interfaz de usuario es poder decidir qué características de la aplicación son las más importantes y cuáles se pueden cortar.

 

 
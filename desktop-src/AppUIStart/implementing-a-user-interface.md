---
title: Implementar una interfaz de usuario
description: En esta sección se describen algunas de las tareas asociadas con la implementación de una interfaz de usuario para una aplicación Windows.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359173"
---
# <a name="implementing-a-user-interface"></a>Implementar una interfaz de usuario

En esta sección se describen algunas de las tareas asociadas con la implementación de una interfaz de usuario para una aplicación Windows.

-   [Prototipo](#prototype)
-   [Construir](#construct)
-   [Simplificar](#simplify)
    -   [Reducción, reutilización, desaglomeración](#reduce-reuse-declutter)
    -   [La mejor interfaz de usuario no es una interfaz de usuario](#the-best-ui-is-no-ui)
    -   [Menos UI es una interfaz de usuario mejor](#less-ui-is-better-ui)
    -   [La interfaz de usuario coherente es una interfaz de usuario buena](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototipo

Las interfaces de usuario (IU) deben diseñarse en la lista de escenarios de usuario y requisitos que se identificaron en el paso de análisis de usuario.

Los prototipos pueden ser tan sencillos como los bocetos de lápiz o tan complejos como los bocetos de pantalla interactivos. Mantenga todo el trabajo anterior, ya que puede ser útil al mostrar a las partes interesadas las alternativas que se tuvieron en cuenta y explicar por qué se descartaron.

Intente limitar este paso a dos o tres prototipos como máximo. Los prototipos no tienen que ser exhaustivas; solo tienen que simular eficazmente la experiencia del uso de la aplicación real.

Muestre los prototipos y realice un seguimiento de los comentarios de los usuarios para ayudar a identificar las tendencias generales de facilidad de uso. Si es posible, descarte los prototipos menos correctos e incorpore tantos comentarios como sea posible en uno o varios de los prototipos restantes. Repita este proceso a medida que el tiempo y los recursos lo permitan.

Hay varias herramientas de prototipo disponibles, entre las que se incluyen [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) en Microsoft Expression Studio 3, el editor de diseño de Microsoft Visual Studio e incluso Microsoft Paint.

## <a name="construct"></a>Construcción

Cuando implemente la interfaz de usuario para una aplicación, tenga en cuenta lo siguiente:

-   Estructura de comandos

    Determine si desea implementar una estructura de comandos tradicional basada en menús y barras de herramientas, o una estructura de comandos alternativa basada en el marco de la cinta de opciones de Windows. Para obtener más información, vea [menús](../menurc/menus.md), [barras de herramientas](../controls/toolbar-control-reference.md)y marco de [la cinta](../windowsribbon/-uiplat-windowsribbon-entry.md)de opciones de Windows.

-   Ventanas y cuadros de diálogo

    En función del diseño de la interfaz de usuario y el trabajo de prototipo, implemente las ventanas de la aplicación, incluida la ventana principal, las ventanas secundarias, los cuadros de diálogo y los cuadros de mensaje. Siga las directrices de la experiencia del usuario para determinar qué estilos y controles usar en las ventanas y los cuadros de diálogo. Para obtener más información, vea [ventanas](../winmsg/windows.md), [cuadros de diálogo](../dlgbox/dialog-boxes.md)y controles de [Windows](../controls/window-controls.md).

-   Controles personalizados

    Cree nuevos controles personalizados solo si no puede obtener la funcionalidad que desea de uno de los controles estándar de Windows. Los nuevos controles personalizados son muy costosos de desarrollar y requieren trabajo adicional para que sean accesibles. Si su aplicación requiere controles personalizados, asegúrese de que están expuestos adecuadamente a las tecnologías de asistencia. Para obtener más información, vea [controles personalizados](../controls/user-controls-intro.md) y [API de automatización de Windows](../winauto/windows-automation-api-portal.md).

-   Compatibilidad con dispositivos de entrada de usuario estándar

    La mayoría de las aplicaciones de Windows necesitan admitir la entrada del usuario a través del teclado y el mouse. La capacidad de navegar y tener acceso a toda la funcionalidad de la aplicación a través del teclado por sí solo es importante para los usuarios que tienen deficiencias visuales o que tienen problemas de movilidad. Para obtener más información, consulte la [entrada de usuario](../inputdev/user-input.md) y el [libro electrónico de ingeniería de accesibilidad](https://www.microsoft.com/download/details.aspx?id=19262).

-   Estilos visuales, animaciones y efectos visuales

    Windows incluye varias tecnologías que puede usar para agregar interés visual y establecer la interfaz de usuario aparte de la de otras aplicaciones. Esto incluye especificar los estilos visuales de los controles, agregar animaciones a los elementos de la interfaz de usuario e implementar varios efectos visuales en la interfaz de usuario. Para obtener más información, vea [estilos visuales](../controls/themes-overview.md), [Administrador de animaciones de Windows](../uianimation/-main-portal.md)y [Administrador de ventanas de escritorio](../dwm/dwm-overview.md).

## <a name="simplify"></a>Simplificación de 

Una experiencia de usuario correcta depende del enfoque, la perspectiva y las suposiciones del desarrollador durante el proceso de diseño. La obtención de una comprensión básica de cómo una aplicación puede ser utilizada por la audiencia de destino requiere la capacidad de pensar en general, además de las restricciones de lo que se adapta a las necesidades del desarrollador. Invertir este tiempo, esfuerzo e investigación al principio de un proyecto pagará los dividendos al final.

### <a name="reduce-reuse-declutter"></a>Reducción, reutilización, desaglomeración

Las características solo mejoran un producto si se usan realmente. En muchos casos, la proliferación de características puede incluir complejidad con la adición de más iconos, elementos de menú, barras de herramientas y cuadros de diálogo que interfieren con la eficacia y la productividad en lugar de agregar valor.

### <a name="the-best-ui-is-no-ui"></a>La mejor interfaz de usuario no es una interfaz de usuario

La interfaz de usuario implica que el usuario tiene que interactuar con la aplicación para hacer algo. En el caso ideal, no es necesario realizar ninguna interacción. Desde la perspectiva del usuario, solo funciona. Si se puede Agregar una característica que quita de forma segura una interacción del usuario, mejora significativamente la experiencia del usuario.

### <a name="less-ui-is-better-ui"></a>Menos UI es una interfaz de usuario mejor

En muchos casos, no es posible quitar la interacción de la interfaz de usuario completamente de la experiencia del usuario. Sin embargo, el mejor interacción del usuario que necesita una aplicación es el mejor.

Identifique las actividades más comunes y básicas que los usuarios realizarán con la aplicación y haga que esas funciones sean las más destacadas en la interfaz de usuario. Relegar otras funciones y actividades a un estado inferior visualmente, jerárquicamente o a través de configuraciones de aplicación y preferencias de usuario opcionales.

-   Reemplazar en lugar de agregar

    La conservación de la regla de IU indica que solo se agrega algo cuando se puede quitar algo. Esta regla obliga a un desarrollador a pensar de forma crítica sobre una nueva característica teniendo en cuenta el impacto que la característica tiene en toda la experiencia del usuario.

    No se deben promover nuevas características porque son nuevas: no confunda el marketing con la facilidad de uso. Para ayudar a los usuarios a encontrar nuevas características en el producto, agregue un elemento al menú **ayuda** que describe los cambios que se han producido desde la última versión de la aplicación.

-   El usuario es un recurso limitado

    Cuanto más funcionalidad se exponga en un momento dado, más difícil será que un usuario encuentre la funcionalidad que necesitan.

-   Es forzada a interrumpir

    Cuando una aplicación muestra un cuadro de diálogo, obliga al usuario a detener todo lo que está haciendo y prestar atención a otra cosa. Si es posible, elimine la necesidad de un cuadro de diálogo por completo evitando los casos de error y otras experiencias de usuario perjudiciales. Para obtener más información acerca de las directrices de mensajes, vea [mensajes](https://msdn.microsoft.com/library/dd535525.aspx).

-   Simple puede ser eficaz

    Una interfaz de usuario simple no implica una falta de funcionalidad. Normalmente, el resultado de una interfaz de usuario más sencilla es una curva de aprendizaje abreviada, una mayor eficiencia y una mayor productividad. Esto permite a los usuarios aumentar su competencia con la aplicación.

### <a name="consistent-ui-is-good-ui"></a>La interfaz de usuario coherente es una interfaz de usuario buena

Por lo general, se recomienda procurar la coherencia en toda la interfaz de usuario de la aplicación. Proporcionar una interfaz de usuario coherente permite a los usuarios ser más expertos con una aplicación en un tiempo mucho más corto. Pueden aplicar su conocimiento existente de la aplicación a diferentes situaciones y usar una funcionalidad desconocida con confianza.

En raras ocasiones, la coherencia no aporta ninguna ventaja al usuario y puede incluso degradar la experiencia del usuario. No haga que la interfaz de usuario sea coherente si esa coherencia dificulta la capacidad de realizar una tarea. La coherencia en sí mismo no garantiza la facilidad de uso. Es un error pensar que la coherencia en la interfaz dará lugar a un buen diseño.

Por ejemplo, la interfaz de usuario del juego de vídeo suele ser muy específica del tipo de juego. Al intentar diseñar una interfaz de usuario genérica que funcione bien para dos juegos especializados, uno que requiera una rueda de gobierno y otro que funcione mejor con un joystick y botones, es probable que no se realice correctamente para cualquier juego. Es posible que, en el mejor de los medios, se logre que no sea adecuado para ninguno de ellos.

Tener buenos datos sobre cómo se usan los elementos es la clave para tomar esta decisión. Tenga claro las ventajas y desventajas de cada compromiso (velocidad frente a confiabilidad, facilidad de aprendizaje frente a la competencia experta, coherencia global frente a la optimización local) y tome las mejores decisiones para la característica con respecto a todo el producto.

El diseño está optando por error: la optimización de una cosa significa error en otro. La clave para un buen diseño de la interfaz de usuario es poder decidir qué características de la aplicación son las más importantes y cuáles se pueden cortar.

 

 
---
title: Cuadros de grupo
description: Un cuadro de grupo es un marco rectangular etiquetado que rodea un conjunto de controles relacionados. Un cuadro de grupo es una manera de mostrar las relaciones visualmente; Además de proporcionar una clave de acceso para un grupo de controles, no proporciona ninguna funcionalidad.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267516"
---
# <a name="group-boxes"></a>Cuadros de grupo

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Un cuadro de grupo es un marco rectangular etiquetado que rodea un conjunto de controles relacionados. Un cuadro de grupo es una manera de mostrar las relaciones visualmente; Además de proporcionar una clave de acceso para un grupo de controles, no proporciona ninguna funcionalidad.

![captura de pantalla del cuadro de grupo que contiene casillas ](images/ctrl-group-boxes-image1.png)

Un cuadro de grupo típico.

> [!Note]  
> Las instrucciones relacionadas [con el diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Aunque los cuadros de grupo son un medio visual sólido para indicar relaciones, su uso en exceso agrega desorden visual y reduce en gran medida el espacio disponible en una superficie. Son visualmente pesadas y deben usarse con moderación, solo cuando no hay una solución mejor.

Una tendencia de diseño en Windows es una apariencia más sencilla y limpia mediante la eliminación de líneas innecesarias.

Para decidir si un cuadro de grupo es necesario, tenga en cuenta estas preguntas:

-   **¿Hay más de un control en el grupo?** Si no es así, use una etiqueta de texto sin formato en su lugar. Una excepción poco frecuente es usar un cuadro de grupo con un único control para mantener la coherencia con otros cuadros de grupo en la misma superficie.

**Incorrecto:** ![ captura de pantalla del cuadro de grupo que contiene un cuadro de texto ](images/ctrl-group-boxes-image2.png)

En este ejemplo, el cuadro de grupo solo tiene un control.

-   **¿Están relacionados los controles? ¿La presentación de la relación agrega claridad?** Si no es así, presente los controles por separado fuera de un cuadro de grupo.
-   **¿Están todos los controles dentro del grupo?** Si es así, indique la relación en la superficie más grande, como el cuadro de diálogo primario o la página.

**Incorrecto:** ![ captura de pantalla del cuadro de grupo que contiene todos los controles ](images/ctrl-group-boxes-image3.png)

En este ejemplo, todos los controles (además de los botones de confirmación) del cuadro de diálogo están dentro del cuadro de grupo.

-   **¿Puede comunicar de forma eficaz las relaciones mediante el diseño por sí solo?** Si es así, use [el diseño](vis-layout.md) en su lugar. Puede colocar controles relacionados entre sí y colocar espaciado adicional entre controles no relacionados. También puede usar encabezados y sangría para mostrar relaciones jerárquicas.

![ilustración de cuatro iconos que muestran cuatro grupos de tareas ](images/ctrl-group-boxes-image4.png)

En este ejemplo, el diseño por sí solo se usa para mostrar las relaciones de control.

-   **¿Puede comunicar eficazmente las relaciones mediante un separador?** Si es así, use un separador en su lugar. Un separador es una línea horizontal que unifica los controles que hay debajo. Los separadores proporcionan un aspecto más sencillo y limpio. Sin embargo, a diferencia de los cuadros de grupo, funcionan mejor cuando abarcan todo el ancho de la superficie.
    -   **Desarrolladores:** Puede implementar un separador con un rectángulo grabado con un alto de uno.

![Captura de pantalla que muestra los controles de correo electrónico separados por separadores de rectángulos entrelazados.](images/ctrl-group-boxes-image5.png)

En este ejemplo, los separadores etiquetados se usan para mostrar las relaciones de control.

![captura de pantalla de los controles separados por separadores ](images/ctrl-group-boxes-image6.png)

En este ejemplo, se usan separadores sin etiquetar para mostrar relaciones de control.

-   **¿Puede comunicar de forma eficaz las relaciones sin texto?** Si es así, considere la posibilidad de usar elementos [gráficos](vis-graphic.md) como fondos o agregadores.

## <a name="guidelines"></a>Directrices

-   **No anidar cuadros de grupo.** Use el diseño para mostrar las relaciones dentro de un cuadro de grupo.

**Incorrecto:** ![ captura de pantalla de un cuadro de grupo dentro de un cuadro de grupo ](images/ctrl-group-boxes-image7.png)

En este ejemplo, los cuadros de grupo anidados tienen como resultado un desorden visual innecesario.

**Correcto:** ![ captura de pantalla de los mismos controles dentro de un cuadro de grupo ](images/ctrl-group-boxes-image8.png)

En este ejemplo, se muestra la misma relación de control mediante el diseño en su lugar.

-   No coloque controles en etiquetas de cuadro de grupo.
    -   **Excepción:** Puede usar una casilla como etiqueta de cuadro de grupo si todos los controles dentro de la casilla están habilitados y deshabilitados por la casilla.

**Incorrecto:** ![ captura de pantalla de la lista desplegable en una etiqueta de cuadro de grupo ](images/ctrl-group-boxes-image9.png)

En este ejemplo, una lista desplegable se coloca incorrectamente en un cuadro de grupo. En este ejemplo se deben usar [pestañas](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) en su lugar.

-   **No deshabilite los cuadros de grupo.** Para indicar que un grupo de controles no se aplica actualmente, deshabilite todos los controles del cuadro de grupo, pero no el propio cuadro de grupo. Este enfoque es más accesible y puede ser compatible de forma coherente con todos los marcos de interfaz de usuario.

## <a name="labels"></a>Etiquetas

-   Etiquete todos los cuadros de grupo.
-   No asigne una clave de acceso a la etiqueta. Esto no es necesario y dificulta la asignación de las demás claves de acceso. En su lugar, asigne claves de acceso a los controles dentro del cuadro de grupo.
    -   **Excepción:** Si una superficie tiene muchos controles, puede que no haya suficientes claves de acceso disponibles. Si es así, reduzca el número de claves de acceso asignándolos a cuadros de grupo en lugar de a los controles dentro de los cuadros de grupo.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   Escriba la etiqueta con un sustantivo o una frase de sustantivo, no como una frase, y no use signos de puntuación finales, incluidos los dos puntos.
-   Use expresiones paralelas para etiquetas de cuadro de grupo dentro de la misma superficie.
-   Mantenga las etiquetas de cuadro de grupo concisas. No use texto informativo como etiqueta. Sin embargo, puede tener texto informativo en el cuadro de grupo.
-   No repita la etiqueta del cuadro de grupo en las etiquetas de control dentro del cuadro. Por ejemplo, si el cuadro de grupo tiene la etiqueta Alineación, etiquete los botones de opción Izquierda, Derecha, entre otros, no Alineación izquierda o Alineación derecha.
-   No haga referencia a los cuadros de grupo en el texto de la interfaz de usuario.

## <a name="documentation"></a>Documentación

Al hacer referencia a cuadros de grupo:

-   Consulte los cuadros de grupo solo en el programador y otra documentación técnica. Para el cuadro de grupo, use dos palabras minúsculas.
-   En cualquier otro lugar, no es necesario incluir el nombre del cuadro de grupo en un procedimiento a menos que un cuadro de diálogo contenga más de una opción con el mismo nombre. En tales casos, use en con el nombre del cuadro de grupo.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en **Efectos**, seleccione **Oculto.**

 

 
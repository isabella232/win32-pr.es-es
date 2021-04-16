---
title: Cuadros de grupo
description: Un cuadro de grupo es un marco rectangular con etiqueta que rodea un conjunto de controles relacionados. Un cuadro de grupo es una forma de mostrar las relaciones visualmente; Además de proporcionar una clave de acceso para un grupo de controles, no proporciona ninguna funcionalidad.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104557699"
---
# <a name="group-boxes"></a>Cuadros de grupo

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Un cuadro de grupo es un marco rectangular con etiqueta que rodea un conjunto de controles relacionados. Un cuadro de grupo es una forma de mostrar las relaciones visualmente; Además de proporcionar una clave de acceso para un grupo de controles, no proporciona ninguna funcionalidad.

![captura de pantalla del cuadro de grupo que contiene casillas ](images/ctrl-group-boxes-image1.png)

Cuadro de grupo típico.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Aunque los cuadros de grupo son un medio visual seguro de indicar relaciones, si se sobreutilizan, se agrega confusión visual y se reduce en gran medida el espacio disponible en una superficie. Son visualmente pesadas y deben usarse con moderación, solo cuando no hay una solución mejor.

Una tendencia de diseño en Windows es un aspecto más sencillo y más limpio eliminando las líneas innecesarias.

Para decidir si es necesario un cuadro de grupo, tenga en cuenta estas preguntas:

-   **¿Hay más de un control en el grupo?** En caso contrario, utilice una etiqueta de texto sin formato. Una excepción poco frecuente es utilizar un cuadro de grupo con un solo control para mantener la coherencia con otros cuadros de grupo en la misma superficie.

**Incorrecto:** ![ captura de pantalla del cuadro de grupo que contiene un cuadro de texto ](images/ctrl-group-boxes-image2.png)

En este ejemplo, el cuadro de grupo tiene solo un control.

-   **¿Están relacionados los controles? ¿Muestra la relación agregar claridad?** En caso contrario, presente los controles por separado fuera de un cuadro de grupo.
-   **¿Todos los controles están dentro del grupo?** Si es así, indique la relación en la superficie más grande, como la página o el cuadro de diálogo primario.

**Incorrecto:** ![ captura de pantalla del cuadro de grupo que contiene todos los controles ](images/ctrl-group-boxes-image3.png)

En este ejemplo, todos los controles (aparte de los botones de confirmación) del cuadro de diálogo se encuentran dentro del cuadro de grupo.

-   **¿Puede comunicarse de forma eficaz las relaciones usando solo el diseño?** Si es así, utilice el [diseño](vis-layout.md) en su lugar. Puede colocar controles relacionados junto a otros y colocar el espaciado adicional entre los controles no relacionados. También puede usar los encabezados y la sangría para mostrar las relaciones jerárquicas.

![figura de cuatro iconos que muestran cuatro grupos de tareas ](images/ctrl-group-boxes-image4.png)

En este ejemplo, el diseño solo se usa para mostrar las relaciones de control.

-   **¿Puede comunicar eficazmente las relaciones mediante un separador?** En ese caso, utilice un separador en su lugar. Un separador es una línea horizontal que unifica los controles que hay debajo de él. Los separadores proporcionan un aspecto más sencillo y más limpio. Sin embargo, a diferencia de los cuadros de grupo, funcionan mejor cuando abarcan el ancho completo de la superficie.
    -   **Desarrolladores:** Puede implementar un separador con un rectángulo grabado con un alto de uno.

![Captura de pantalla que muestra los controles de correo electrónico que se separan mediante separadores de rectángulo grabados.](images/ctrl-group-boxes-image5.png)

En este ejemplo, se utilizan separadores etiquetados para mostrar las relaciones de control.

![captura de pantalla de controles que se separan mediante separadores ](images/ctrl-group-boxes-image6.png)

En este ejemplo, se utilizan separadores sin etiquetar para mostrar las relaciones de control.

-   **¿Puede comunicarse de forma eficaz las relaciones sin texto?** Si es así, considere la posibilidad de usar elementos gráficos como el [fondo](vis-graphic.md) o los agregadores.

## <a name="guidelines"></a>Directrices

-   **No anide cuadros de grupo.** Use el diseño para mostrar las relaciones dentro de un cuadro de grupo.

**Incorrecto:** ![ captura de pantalla de un cuadro de grupo dentro de un cuadro de grupo ](images/ctrl-group-boxes-image7.png)

En este ejemplo, los cuadros de grupo anidados producen un desorden visual innecesario.

**Correcto:** ![ captura de pantalla de los mismos controles dentro de un cuadro de grupo ](images/ctrl-group-boxes-image8.png)

En este ejemplo, se muestra la misma relación de control utilizando el diseño en su lugar.

-   No coloque controles en etiquetas de cuadro de grupo.
    -   **Excepción:** Puede utilizar una casilla de verificación como etiqueta de cuadro de grupo si todos los controles del cuadro están habilitados y deshabilitados por la casilla.

**Incorrecto:** ![ captura de pantalla de la lista desplegable de una etiqueta de cuadro de grupo ](images/ctrl-group-boxes-image9.png)

En este ejemplo, una lista desplegable se coloca incorrectamente en un cuadro de grupo. En su lugar, en este ejemplo se deben usar [pestañas](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) .

-   **No deshabilite los cuadros de grupo.** Para indicar que actualmente no se aplica un grupo de controles, deshabilite todos los controles del cuadro de grupo, pero no el propio cuadro de grupo. Este enfoque es más accesible y puede ser compatible de forma coherente con todos los marcos de interfaz de usuario.

## <a name="labels"></a>Etiquetas

-   Etiquete todos los cuadros de grupo.
-   No asigne una clave de acceso a la etiqueta. Esto no es necesario y hace que las demás claves de acceso sean más difíciles de asignar. En su lugar, asigne las teclas de acceso a los controles del cuadro de grupo.
    -   **Excepción:** Si una superficie tiene muchos controles, puede que no haya suficientes claves de acceso disponibles. Si es así, reduzca el número de claves de acceso asignándoles los cuadros de grupo en lugar de los controles de los cuadros de grupo.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Escriba la etiqueta con un sustantivo o un nombre, no como una frase, y no use signos de puntuación de cierre, incluidos los dos puntos.
-   Use frases paralelas para las etiquetas de cuadro de grupo dentro de la misma superficie.
-   Mantenga las etiquetas del cuadro de grupo concisos. No use texto informativo como etiqueta. Sin embargo, puede tener texto de instrucciones en el cuadro de grupo.
-   No repita la etiqueta del cuadro de grupo en las etiquetas de control del cuadro. Por ejemplo, si el cuadro de grupo tiene la etiqueta alineación, etiquete los botones de opción izquierda, derecha, etc., no alinear a la izquierda ni alinear a la derecha.
-   No haga referencia a los cuadros de grupo en el texto de la interfaz de usuario.

## <a name="documentation"></a>Documentación

Al hacer referencia a los cuadros de Grupo:

-   Haga referencia a los cuadros de grupo solo en el programador y en otra documentación técnica. En cuadro de grupo, use dos palabras en minúsculas.
-   En cualquier otro lugar, no es necesario incluir el nombre del cuadro de grupo en un procedimiento a menos que un cuadro de diálogo contenga más de una opción con el mismo nombre. En tales casos, use en con el nombre del cuadro de grupo.
-   Siempre que sea posible, dé formato a la etiqueta usando texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en **efectos**, seleccione **oculto**.

 

 
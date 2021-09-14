---
title: Controles deslizantes (conceptos básicos de diseño)
description: Con un control deslizante, los usuarios pueden elegir entre un intervalo continuo de valores.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267487"
---
# <a name="sliders-design-basics"></a>Controles deslizantes (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un control deslizante, los usuarios pueden elegir entre un intervalo continuo de valores. Un control deslizante tiene una barra que muestra el intervalo y un indicador que muestra el valor actual. Las marcas de graduación opcionales muestran valores.

![ilustración que muestra barras, controles deslizantes y marcas de graduación ](images/ctrl-sliders-image1.png)

Un control deslizante típico.

> [!Note]  
> Las directrices relacionadas [con el](vis-layout.md) diseño se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Use un control deslizante cuando desee que los usuarios puedan establecer valores contiguos definidos (como volumen o brillo) o un intervalo de valores discretos (como la configuración de resolución **de pantalla).**

Un control deslizante es una buena opción si sabes que los usuarios ven el valor como una cantidad relativa y no como un valor numérico. Por ejemplo, al ajustar el volumen, los usuarios piensan en términos de bajo o medio, y no piensan que deben ajustar el valor de volumen en 2 o 5.

Para decidirte, intenta responder a estas preguntas:

-   **¿El valor de configuración parece una cantidad relativa?** Si no es así, use [botones de radio](ctrl-radio-buttons.md)o [una lista desplegable](/windows/desktop/uxguide/ctrl-drop) o de selección [única.](ctrl-list-boxes.md)
-   **¿El valor de configuración es un valor numérico exacto y conocido?** Si es así, use un [cuadro de texto numérico](ctrl-text-boxes.md).
-   **¿Sería bueno que el usuario obtuviera una respuesta inmediata sobre el efecto de los cambios realizados en la configuración?** Si es así, usa un control deslizante. Por ejemplo, los usuarios pueden elegir un color más fácilmente si ven de forma inmediata el efecto de los cambios en los valores de matiz, saturación o luminosidad.
-   **¿La configuración tiene un intervalo de cuatro o más valores?** Si no es así, usa botones de radio.
-   **¿El usuario puede cambiar el valor?** Los controles deslizantes están destinados a la interacción del usuario. Si un usuario no puede cambiar nunca el valor, use en su lugar un cuadro de [texto de solo lectura.](ctrl-text-boxes.md)

Si es posible un control deslizante o un cuadro de texto numérico, use un cuadro de texto numérico si:

-   El espacio en pantalla es limitado.
-   Es probable que un usuario prefiera usar el teclado.

Usa el control deslizante si:

-   Los usuarios van a sacar provecho de una respuesta instantánea.

## <a name="guidelines"></a>Directrices

-   **Usa una orientación natural.** Por ejemplo, si el control deslizante representa un valor del mundo real que normalmente se muestra en vertical (como la temperatura), usa una orientación vertical.
-   **Oriente el control deslizante para reflejar la referencia cultural de los usuarios.** Por ejemplo, las referencia culturales occidental se leen de izquierda a derecha, por lo que para los controles deslizantes horizontales, coloque el extremo inferior del intervalo a la izquierda y el extremo superior a la derecha. Para las referencia culturales que leen de derecha a izquierda, haga lo contrario.
-   **Ajuste el tamaño del control para que un usuario pueda establecer fácilmente el valor deseado.** En el caso de opciones con valores discretos, asegúrate de que al usuario le resulte fácil seleccionar cualquier valor mediante el mouse.
-   **Considere la posibilidad de usar una escala no lineal si el intervalo de valores es grande y es probable que los usuarios seleccionen valores en un extremo del intervalo.** Por ejemplo, el valor de tiempo puede ser 1 minuto, 1 hora, 1 día o 1 mes.
-   **Siempre que sea práctico, enviar comentarios inmediatos mientras o después un usuario realiza una selección.** Por ejemplo, microsoft Windows de control de volumen para indicar el volumen de audio resultante.
-   **Usa etiquetas para mostrar el intervalo de valores.**

    **Excepción:** Si el control deslizante está orientado verticalmente y la etiqueta superior es Máximo, Alto, Más o equivalente, puede omitir las demás etiquetas, ya que el significado es claro.

    ![figura de un control deslizante vertical ](images/ctrl-sliders-image2.png)

    En este ejemplo, la orientación vertical del control deslizante hace que las etiquetas de intervalo sean innecesarias.

-   **Use marcas de graduación cuando los usuarios necesiten conocer el valor aproximado de la configuración.**
-   **Use marcas de graduación y una etiqueta de valor cuando los usuarios necesiten conocer el valor exacto de la configuración que elijan.** Use siempre una etiqueta de valor si un usuario necesita conocer las unidades para tener sentido a la configuración.

    ![figura del control deslizante que muestra el número de píxeles seleccionados ](images/ctrl-sliders-image3.png)

    En este ejemplo, se usa una etiqueta para indicar claramente el valor seleccionado.

-   **En el caso de los controles deslizantes orientados horizontalmente, coloque las marcas de graduación debajo del control deslizante.** En el caso de los controles deslizantes orientados verticalmente, coloque marcas de graduación a la derecha para las culturas occidental. para las referencia culturales que leen de derecha a izquierda, haga lo contrario.
-   **Coloque la etiqueta de valor completamente bajo el control deslizante para que la relación esté clara.**

    **Incorrecto:**

    ![figura de una etiqueta que es más larga que su control deslizante ](images/ctrl-sliders-image4.png)

    En este ejemplo, la etiqueta de valor no está alineada bajo el control deslizante.

-   **Al deshabilitar un control deslizante, deshabilite también las etiquetas asociadas.**
-   **No use un control deslizante y un cuadro de texto numérico para la misma configuración.** Use solo el control más adecuado.

    **Excepción:** Use ambos controles cuando el usuario necesite comentarios inmediatos y la capacidad de establecer un valor numérico exacto.

-   **No uses un control deslizante como indicador de progreso.**
-   **No cambie el tamaño del indicador deslizante del tamaño predeterminado.**

    **Incorrecto:**

    ![figura del control deslizante que es menor que el valor predeterminado ](images/ctrl-sliders-image5.png)

    En este ejemplo, se usa un tamaño menor que el predeterminado.

    **Correcto:**

    ![ilustración que muestra el control deslizante predeterminado ](images/ctrl-sliders-image6.png)

    En este ejemplo, se usa el tamaño predeterminado.

-   **No etiquete todas las marcas de graduación.**

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![figura de ajuste de tamaño y espaciado recomendados del control deslizante ](images/ctrl-sliders-image7.png)

Ajuste de tamaño y espaciado recomendados para los controles deslizantes.

## <a name="labels"></a>Etiquetas

### <a name="slider-labels"></a>Etiquetas de control deslizante

-   Use una etiqueta de texto estático que termine con dos puntos o una etiqueta de cuadro de grupo sin signo de puntuación final.
-   Asigne una clave de acceso única a cada etiqueta. Para obtener instrucciones de asignación, vea [Teclado](inter-keyboard.md).
-   Use mayúsculas de estilo de frase.
-   Coloque la etiqueta del control deslizante a la izquierda del control deslizante o superior y alineada con el borde izquierdo del control deslizante (o su identificador de intervalo izquierdo, si está presente).

### <a name="range-labels"></a>Etiquetas de intervalo

-   Etiqueta los dos extremos del intervalo del control deslizante, a menos que la orientación vertical haga que resulte innecesario.
-   Use solo word, si es posible, para cada etiqueta.
-   No uses puntuación final.
-   Asegúrate de que las etiquetas sean descriptivas y estén paralelas. Ejemplos: Máximo/Mínimo, Más/Menos, Bajo/Alto, Suave/Fuerte.
-   Use mayúsculas de estilo de frase.
-   No asigne claves de acceso.

### <a name="value-labels"></a>Etiquetas de valor

-   Si necesitas una etiqueta de valor, muéstrala debajo del control deslizante.
-   Centra el texto en relación con el control e incluye las unidades (como pueden ser píxeles).

    ![figura de la etiqueta centrada bajo el control deslizante ](images/ctrl-sliders-image8.png)

    En este ejemplo, la etiqueta de valor se centra bajo el control deslizante e incluye las unidades.

## <a name="documentation"></a>Documentación

Al hacer referencia a los controles deslizantes:

-   Use el texto exacto de la etiqueta, incluida su mayúscula, e incluya el control deslizante de palabras. No incluya el carácter de subrayado ni los dos puntos de la clave de acceso.
-   Para describir la interacción del usuario, use move.
-   Cuando sea posible, formatee la etiqueta con texto en negrita. De lo contrario, coloque la etiqueta entre comillas solo si es necesario para evitar confusiones.

Ejemplo: Para aumentar la resolución de pantalla, mueva el control deslizante **Resolución de** pantalla a la derecha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Glosario](glossary.md)
</dt> </dl>

 

 
---
title: Controles de giro
description: Con un control de número, los usuarios pueden hacer clic en los botones de flecha para cambiar incrementalmente el valor dentro de su cuadro de texto numérico asociado.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b97f5acc8a3f904df3a868274356e5337f5cc9280a5eed81693d92ce9bf9a37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217401"
---
# <a name="spin-controls"></a>Controles de giro

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un control de número, los usuarios pueden hacer clic en los botones de flecha para cambiar incrementalmente el valor dentro de su cuadro [de texto numérico asociado.](ctrl-text-boxes.md) El término cuadro de número hace referencia a la combinación de un cuadro de texto y su control de número asociado.

![captura de pantalla del control de número y el cuadro de texto ](images/ctrl-spin-controls-image1.png)

Un cuadro de giro típico.

A menudo, los usuarios prefieren controles de número porque pueden realizar cambios sin mover las manos del mouse. Cuando el control de número se empareja con un cuadro de texto, los usuarios pueden escribir o pegar la entrada directamente en el cuadro de texto, por lo que el uso del control de número es opcional.

Aunque los controles de número se usan para la entrada numérica, la entrada no tiene que ser un número entero puro. La entrada puede ser números decimales y puede tener signos negativos, delimitadores (como dos puntos o guiones) y modificadores de unidad.

> [!Note]  
> Las instrucciones relacionadas con [los cuadros de](ctrl-text-boxes.md) texto y el [diseño](vis-layout.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se usa el control para la entrada numérica?** Si no es así, use otro control, como [una lista](/windows/desktop/uxguide/ctrl-drop) desplegable o un control [deslizante,](ctrl-sliders.md)para seleccionar entre un conjunto fijo de valores. Use barras de desplazamiento para desplazarse.
-   **¿Los usuarios creen que el valor es una cantidad relativa, no un valor numérico?** Si es así, use un control deslizante en su lugar. Use cuadros de número solo para valores numéricos exactos conocidos. Por ejemplo, al ajustar el volumen, los usuarios piensan en términos de bajo o medio, y no piensan que deben ajustar el valor de volumen en 2 o 5.
-   **¿El control está emparejado con un cuadro de texto?** Si no es así, no lo use. Los controles de número no deben usarse solos ni con otros tipos de controles además de un cuadro de texto.

    **Incorrecto:**

    ![captura de pantalla del control de número, gráfico, sin cuadro de texto ](images/ctrl-spin-controls-image2.png)

    En este ejemplo, se usa un control de giro para controlar un gráfico dinámico.

-   **¿Son válidos los intervalos de valores contiguos?** Si no es así, use una lista desplegable de valores válidos en su lugar.

    ![captura de pantalla de la lista desplegable ](images/ctrl-spin-controls-image3.png)

    En este ejemplo, no todos los números de unidad de disco son válidos, por lo que una lista desplegable es una mejor opción.

-   **¿Es práctico usar el control de número?** El uso de un control de giro es práctico para:

    -   Escribir un número pequeño, normalmente por debajo de 100.
    -   Realizar pequeños cambios en un valor existente o predeterminado.

    Aunque los controles de número se pueden usar para cualquier entrada numérica, son ineficaces en situaciones distintas de estas.

-   **¿Es útil el control de número?** ¿Se usa el control en un contexto en el que es probable que los usuarios estén usando el mouse? Si no es así, considere un control de giro opcional.
-   **¿Son las listas desplegables de controles del mismo nivel?** Si hay otras listas desplegables, considere la posibilidad de usar una lista desplegable para mantener la coherencia.

    ![captura de pantalla del cuadro de diálogo con listas desplegables ](images/ctrl-spin-controls-image4.png)

    En este ejemplo, se podría usar un cuadro de giro, pero se usa una lista desplegable para mantener la coherencia.

-   **¿Son los usuarios táctiles o de lápiz un destino principal?** Si es así, considere la posibilidad de usar una lista desplegable en su lugar. Los botones de flecha de un control de número son demasiado pequeños para su uso eficaz con una entrada táctil o un lápiz.

Si es posible un control deslizante o un cuadro de giro, use un cuadro de giro si:

-   El espacio en pantalla es limitado.
-   Es probable que un usuario prefiera usar el teclado.

Usa el control deslizante si:

-   Los usuarios van a sacar provecho de una respuesta instantánea.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Use controles de giro siempre que sean prácticos y útiles.** Consulte [¿Es este el control correcto?](#is-this-the-right-control)

    -   **Excepción:** Para ser coherentes con otros cuadros de texto en la misma interfaz de usuario (UI), use controles de número incluso si no siempre son prácticos.

    **Correcto:**

    ![captura de pantalla de los controles de número de mes, día y año ](images/ctrl-spin-controls-image5.png)

    En este ejemplo, se usa un control de número con el control year para mantener la coherencia, aunque no siempre sea práctico.

    **Incorrecto:**

    ![captura de pantalla del control de número de dirección IP ](images/ctrl-spin-controls-image6.png)

    En este ejemplo, el control de número es inutilizable.

-   **Haga siempre que un control de número sea el "compañero" del cuadro de texto.** Al hacerlo, el control de número se coloca dentro del cuadro de texto.

    **Correcto:**

    ![captura de pantalla del control de número colocado dentro del cuadro de texto ](images/ctrl-spin-controls-image7.png)

    **Incorrecto:**

    ![captura de pantalla del control de número colocado fuera del cuadro de texto ](images/ctrl-spin-controls-image8.png)

    En el ejemplo correcto, el control de número se coloca dentro de su cuadro de texto asociado.

-   **Deshabilite un control de giro cuando su cuadro de texto asociado esté deshabilitado.** El control de número es un método de entrada complementario, nunca el único método de entrada.

### <a name="values"></a>Valores

-   **Defina el botón superior para aumentar el valor en una unidad y el botón inferior para reducirlo en una unidad.** Normalmente, la unidad es una, pero debe ser el cambio más pequeño común en el valor. Idealmente, el control de número debe cubrir todos los valores válidos y debería ser más conveniente que escribir en el texto.

    ![captura de pantalla del control de número "márgenes" ](images/ctrl-spin-controls-image9.png)

    En este ejemplo, al hacer clic en un control de número se cambian los valores en .1, que es el menor cambio común en el valor. El uso de una unidad más pequeña cubriría el intervalo de valores válidos, pero haría que los controles de número no se pueden usar.

-   **Use el control de número para limitar la entrada a valores válidos.** El uso de un control de número nunca debería dar lugar a un valor incorrecto.
-   **Al final de un intervalo de valores válidos, reinicie el intervalo.** La metáfora del control de número es que el usuario gira una rueda de valores, de ahí este comportamiento parecido a la rueda.
    -   **Excepción:** No reinicie el intervalo si es seguro que el valor resultante es incorrecto.

        ![captura de pantalla del control de número "número de copias" ](images/ctrl-spin-controls-image10.png)

        En este ejemplo, al hacer clic en el botón de flecha abajo no se reinicia el intervalo (yendo al valor máximo) porque es seguro que ese valor es incorrecto.

-   **Use texto en lugar de valores numéricos especiales.** Permitir a los usuarios girar a estos valores especiales en lugar de tener que conocerlos y escribirlos.

    ![captura de pantalla del control de número "suspensión después (nunca)" ](images/ctrl-spin-controls-image11.png)

    En este ejemplo, Nunca es un valor especial, pero los usuarios pueden girar hasta él.

-   **Si el valor tiene delimitadores, el cuadro de texto asociado debe tener varios puntos de foco de entrada.** Esto permite manipular individualmente los segmentos numéricos.

    ![captura de pantalla del control de número de tiempo, minutos seleccionados ](images/ctrl-spin-controls-image12.png)

    En este ejemplo, el control de número afecta a los valores de horas, minutos, segundos y A.M./P.M., lo que tenga el foco.

-   **Si el valor tiene unidades, use el control de número para cambiar esas unidades también.**

    ![captura de pantalla del control de número de tiempo, "a.m." Seleccionado ](images/ctrl-spin-controls-image13.png)

    En este ejemplo, el control de número se puede usar para cambiar las unidades.

## <a name="labels"></a>Etiquetas

-   Aplique las [directrices de etiquetado del cuadro](ctrl-text-boxes.md) de texto para etiquetar el cuadro de texto asociado. Los controles de giro nunca se etiquetan directamente.

## <a name="documentation"></a>Documentación

Al hacer referencia a controles de giro:

-   No consulte los controles de giro en la documentación del usuario. En su lugar, consulte la etiqueta del cuadro de texto asociado.
-   Consulte controles de giro y cuadros de giro solo en programación y otra documentación técnica.

Ejemplo: en el **cuadro Fecha,** escriba o seleccione la parte de la fecha que desea cambiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Glosario](glossary.md)
</dt> </dl>

 

 
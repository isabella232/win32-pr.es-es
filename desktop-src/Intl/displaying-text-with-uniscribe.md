---
description: Las aplicaciones pueden usar las funciones de LA API de Uniscribe para admitir la tipografía y la visualización y edición de texto internacional. Uniscribe usa el párrafo como unidad para la presentación de texto y la funcionalidad Uniscribe debe usarse para todo el párrafo.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Mostrar texto con Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17caf7e7880a61bdf9afbaf6db5b60065b01d3d3960f2ed5629a007aa304b7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949610"
---
# <a name="displaying-text-with-uniscribe"></a>Mostrar texto con Uniscribe

Las aplicaciones pueden usar las funciones de LA API de Uniscribe para admitir la tipografía y la visualización y edición de texto internacional. Uniscribe usa el párrafo como unidad para la presentación de texto y la funcionalidad Uniscribe debe usarse para todo el párrafo.

Cuando se usa Uniscribe para mostrar texto, una aplicación debe pasar por un proceso de formato ("diseño"), normalmente mediante Uniscribe. La aplicación divide un párrafo de texto en cadenas de caracteres con el mismo estilo, denominado "ejecuciones". El estilo viene determinado por la implementación determinada, pero normalmente incluye atributos como fuente, tamaño y color. Al definir ejecuciones, la aplicación también puede aplicar otra información, como los datos de idioma y configuración regional que se mantienen para su uso con herramientas léxicas. Por ejemplo, una aplicación podría tratar como una ejecución independiente un fragmento en un texto principalmente en inglés que se representa en francés.

Una vez que ha determinado las ejecuciones de todos los párrafos, la aplicación divide cada párrafo en cadenas que tienen el mismo script y dirección ("elementos"). La aplicación aplica la información del elemento para generar ejecuciones que son únicas en script y dirección y se encuentran completamente dentro de un único elemento ("intervalos").

El desglose de un elemento en intervalos es un poco arbitrario, aunque un intervalo debe constar de una o varias agrupaciones de caracteres consecutivas definidas por script e indivisibles, denominadas "clústeres". Para los idiomas europeos, un clúster normalmente corresponde a un carácter de página de códigos único o punto de código Unicode, y consta de un único [glifo](uniscribe-glossary.md). Sin embargo, en lenguajes como el tailandés, un clúster es una agrupación de glifos y corresponde a varios caracteres consecutivos o puntos de código. Por ejemplo, un clúster tailandés podría contener una consonante, una voz y una marca de tono. Para no interrumpir los clústeres, la aplicación normalmente debe usar los intervalos más largos que puede o usar su propia información léxica para interrumpir los intervalos en lugares que no están en medio de un clúster.

Cuando haya identificado los clústeres de cada intervalo, la aplicación debe determinar el tamaño de cada clúster. Usa Uniscribe para sumar los clústeres para determinar el tamaño de cada intervalo. A continuación, la aplicación suma los tamaños de los intervalos hasta que desbordan una línea, es decir, alcanzan el margen. El intervalo que desborda la línea se divide entre la línea actual y la siguiente. Para cada línea, la aplicación crea un mapa de la posición visual a la posición lógica de cada intervalo. A continuación, la aplicación da forma a los puntos de código de cada intervalo en glifos, que posteriormente puede colocar y representar.

Una aplicación realiza el diseño de texto solo una vez. Posteriormente, guarda los glifos y las posiciones con fines de presentación o los genera cada vez que muestra el texto, con la velocidad frente a la memoria. Una aplicación típica implementa el proceso de diseño una vez y, a continuación, genera los glifos y las posiciones cada vez que muestra el texto.

Una aplicación que usa [scripts complejos](uniscribe-glossary.md) tiene los siguientes problemas con un enfoque sencillo para el diseño y la presentación.

-   El ancho de un carácter de script complejo depende de su contexto. No es posible guardar los anchos en tablas simples.
-   La separación entre palabras en scripts como el tailandés requiere compatibilidad con diccionarios. Por ejemplo, no se usa ningún carácter separador entre palabras tailandesas.
-   El árabe, hebreo, persa, urdu y otros idiomas de texto bidireccional requieren reordenación antes de mostrarse. [](uniscribe-glossary.md)
-   A menudo se requiere algún tipo de asociación de fuentes para usar fácilmente scripts complejos.

El hecho de que Uniscribe use el párrafo como unidad de presentación ayuda a la aplicación a tratar adecuadamente estos problemas de script complejos.

> [!Note]  
> Uniscribe debe usarse para un párrafo completo, incluso si las secciones del párrafo no son scripts complejos.

 

Como se muestra en la tabla siguiente, Uniscribe versión 1.6 o posterior admite varias funciones que aprovechan las etiquetas OpenType. Se pueden sustituir por las funciones de Uniscribe normales correspondientes. Por lo general, las aplicaciones deben funcionar completamente con funciones de un conjunto u otro y no deben intentar "combinar y combinar" funciones.



| Función Uniscribe normal             | Función OpenType equivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Diseño de texto mediante Uniscribe

La aplicación puede usar los pasos siguientes para establecer un párrafo de texto con Uniscribe. En este procedimiento se da por supuesto que la aplicación ya ha dividido el párrafo en ejecuciones.

1.  Llame a [**ScriptRecordDigitSubstitution solo**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) al iniciar o al recibir un [**mensaje WM \_ SETTINGCHANGE.**](../winmsg/wm-settingchange.md)
2.  (Opcional) Llame [**a ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) para determinar si el párrafo requiere un procesamiento complejo.
3.  (Opcional) Si usa Uniscribe para controlar el texto bidireccional o la sustitución de dígitos, llame a [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) para preparar las estructuras [**\_ SCRIPT CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) y SCRIPT [**\_ STATE**](/windows/win32/api/usp10/ns-usp10-script_state) como entradas para [**ScriptItemize.**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) Si omite este paso, pero sigue requiriendo la sustitución de dígitos, sustituya los dígitos nacionales por Unicode U+0030 a U+0039 (dígitos europeos). Para obtener información sobre la sustitución de dígitos, vea [Formas de dígitos.](digit-shapes.md)
4.  Llame [**a ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para dividir el párrafo en elementos. Si no usa Uniscribe para la sustitución de dígitos y se conoce el orden bidireccional, por ejemplo, debido al diseño de teclado usado para escribir el carácter, llame a **ScriptItemize**. En la llamada, proporcione punteros null para las [**estructuras \_ SCRIPT CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) y SCRIPT [**\_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state) Esta técnica genera elementos solo mediante el motor de modelado y los elementos se pueden reordenar mediante la información del motor.
    > [!Note]  
    > Normalmente, las aplicaciones que solo funcionan con scripts de izquierda a derecha y sin sustitución de dígitos deben pasar punteros nulos para las estructuras [**SCRIPT \_ CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) [**y SCRIPT \_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state)

     

5.  Combine la información del elemento con la información de ejecución para generar intervalos.
6.  Llame [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para identificar clústeres y generar glifos.
7.  Si [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) devuelve el código USP E SCRIPT NOT IN FONT o S OK con la salida que contiene glifos que faltan, seleccione caracteres \_ de otra \_ \_ \_ \_ \_ fuente. Sustituya otra fuente o deshabilite la forma estableciendo el miembro **eScript** de la estructura [**SCRIPT \_ ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) pasado a **ScriptShape** en SCRIPT \_ UNDEFINED. Para obtener más información, vea [Using Font Fallback](using-font-fallback.md).
8.  Llame [**a ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar [anchos avanzados](uniscribe-glossary.md) y posiciones x e y para los glifos de cada intervalo sucesivo. Este es el primer paso para el que el tamaño del texto se convierte en una consideración.
9.  Sumar los tamaños de intervalo hasta que se desborda la línea.
10. Break the range on a word boundary by using the **fSoftBreak** and **fWhiteSpace** members in the logical attributes. Para interrumpir la ejecución de un clúster de caracteres único, use la información devuelta mediante una llamada a [**ScriptBreak.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)
    > [!Note]  
    > Decida si el primer punto de código de un intervalo debe ser un punto de interrupción de palabras porque el último carácter del intervalo anterior lo requiere. Por ejemplo, si un intervalo termina en una coma, considere que el primer carácter del intervalo siguiente es un punto de interrupción de palabras.

     

11. Repita los pasos del 6 al 10 para cada línea del párrafo. Sin embargo, si se ha roto la última ejecución en la línea, llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cambiar la forma de la parte restante de la ejecución como la primera ejecución en la línea siguiente.

## <a name="display-text-using-uniscribe"></a>Mostrar texto mediante Uniscribe

La aplicación puede seguir estos pasos para mostrar un párrafo de texto. En este procedimiento se supone que la aplicación ya ha diseñado el texto y no ha guardado los glifos y las posiciones del proceso de diseño. Si la velocidad es un problema, la aplicación puede guardar los glifos y las posiciones del procedimiento de diseño e iniciarse en el paso 2 del procedimiento de visualización.

> [!Note]  
> La aplicación puede omitir el paso 2 si el texto no contiene caracteres de scripts de derecha a izquierda, no contiene caracteres de control bidireccional y usa un nivel de incrustación base de izquierda a derecha.

 

1.  Para cada ejecución, haga lo siguiente:
    1.  Si el estilo ha cambiado desde la última ejecución, actualice el identificador al contexto del dispositivo publicando y obteniendo de nuevo.
    2.  Llame [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para generar glifos para la ejecución.
    3.  Llame [**a ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar un ancho de avance y un desplazamiento x,y para cada glifo.
2.  Haga lo siguiente para establecer el orden visual correcto para las ejecuciones en la línea:
    1.  Extraiga una matriz de niveles de [inserción bidireccional,](uniscribe-glossary.md)uno por intervalo. El nivel de inserción lo ofrece (SCRIPT \_ ITEM) si.( ANÁLISIS \_ DE SCRIPT) a. (SCRIPT) \_ STATE) s.uBidiLevel.
    2.  Pase esta matriz a [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) para generar un mapa de posiciones visuales a posiciones lógicas.
3.  (Opcional) Para justificar el texto, llame a [**ScriptJustify o**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) use conocimientos especializados del texto.
4.  Use el mapa de objeto visual a lógico para mostrar las ejecuciones en orden visual. A partir del final izquierdo de la línea, llame [**a ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para mostrar la ejecución dada por la primera entrada del mapa. Para cada entrada posterior del mapa, llame a **ScriptTextOut** para mostrar la ejecución indicada a la derecha de la ejecución mostrada anteriormente.

    Si omite el paso 2, comience en el extremo izquierdo de la línea y llame a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para mostrar la primera ejecución lógica y, a continuación, para mostrar cada ejecución lógica a la derecha de la ejecución anterior.

5.  Repita los pasos anteriores para todas las líneas del párrafo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 

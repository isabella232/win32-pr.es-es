---
description: Las aplicaciones pueden usar las funciones de la API de Uniscribe para admitir la tipografía y la visualización y edición de texto internacional. Uniscribe utiliza el párrafo como unidad para la presentación de texto, y la funcionalidad de la función de debe usarse para todo el párrafo.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Mostrar texto con Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baeb9a2be4d00efaa2681097ddefe3a6de4c576b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361231"
---
# <a name="displaying-text-with-uniscribe"></a>Mostrar texto con Uniscribe

Las aplicaciones pueden usar las funciones de la API de Uniscribe para admitir la tipografía y la visualización y edición de texto internacional. Uniscribe utiliza el párrafo como unidad para la presentación de texto, y la funcionalidad de la función de debe usarse para todo el párrafo.

Cuando se usa para la presentación de texto, una aplicación debe pasar por un proceso de formato ("diseño"), que normalmente usa Uniscribe. La aplicación divide un párrafo de texto en cadenas de caracteres con el mismo estilo, denominado "ejecuciones". El estilo está determinado por la implementación concreta, pero normalmente incluye tales atributos como fuente, tamaño y color. En la definición de ejecuciones, la aplicación también puede aplicar otra información, como los datos de idioma y de configuración regional que se mantienen para su uso con las herramientas léxicas. Por ejemplo, una aplicación puede tratar como una ejecución independiente en un texto en inglés que se representa en francés.

Una vez que ha determinado las ejecuciones de todos los párrafos, la aplicación divide cada párrafo en cadenas que tienen el mismo script y dirección ("elementos"). La aplicación aplica la información de los elementos para generar ejecuciones que son únicas en el script y en la dirección y que están completamente dentro de un solo elemento ("intervalos").

El desglose de un elemento en rangos es algo arbitrario, aunque un intervalo debe constar de una o varias agrupaciones de caracteres indivisibles, definidas por el script consecutivas, denominadas "clústeres". En el caso de los idiomas europeos, un clúster normalmente corresponde a un solo carácter de página de códigos o punto de código Unicode, y consta de un único [glifo](uniscribe-glossary.md). Sin embargo, en idiomas como el tailandés, un clúster es una agrupación de glifos y corresponde a varios caracteres consecutivos o puntos de código. Por ejemplo, un clúster tailandés podría contener una consonante, una vocal y una marca de tono. Para que no interrumpa los clústeres, la aplicación normalmente debería usar los intervalos más largos, o bien usar su propia información léxica para dividir entre intervalos en lugares que no están en el medio de un clúster.

Cuando haya identificado los clústeres en cada intervalo, la aplicación debe determinar el tamaño de cada clúster. Utiliza Uniscribe para sumar los clústeres con el fin de determinar el tamaño de cada intervalo. A continuación, la aplicación suma los tamaños de los intervalos hasta que desbordan una línea, es decir, alcanzan el margen. El intervalo que desborda la línea se divide entre la línea actual y la línea siguiente. Para cada línea, la aplicación crea un mapa desde la posición visual hasta la posición lógica para cada intervalo. A continuación, la aplicación forma las formas de los puntos de código de cada intervalo en glifos, que se pueden colocar y representar posteriormente.

Una aplicación solo realiza el diseño de texto una vez. Después, guarda los glifos y las posiciones para mostrarlos o los genera cada vez que muestra el texto, con la máxima velocidad frente a la memoria. Una aplicación típica implementa el proceso de diseño una vez y, después, genera los glifos y posiciones cada vez que se muestra el texto.

Una aplicación que usa [scripts complejos](uniscribe-glossary.md) tiene los siguientes problemas con un enfoque sencillo para el diseño y la presentación.

-   El ancho de un carácter de script complejo depende de su contexto. No es posible guardar los anchos en tablas simples.
-   La división entre palabras en scripts como tailandés requiere compatibilidad con diccionarios. Por ejemplo, no se usa ningún carácter separador entre las palabras tailandesas.
-   Árabe, hebreo, persa, urdu y otros idiomas de [texto bidireccionales](uniscribe-glossary.md) requieren reordenación antes de la presentación.
-   A menudo se requiere algún tipo de Asociación de fuentes para usar fácilmente scripts complejos.

El hecho de que Uniscribe use el párrafo como unidad de pantalla ayuda a la aplicación a tratar adecuadamente con estos problemas complejos de scripts.

> [!Note]  
> Se debe usar Uniscribe para un párrafo completo, incluso si las secciones del párrafo no son scripts complejos.

 

Tal y como se muestra en la tabla siguiente, la versión 1,6 o superior de Uniscribe admite varias funciones que aprovechan las ventajas de las etiquetas OpenType. Se pueden sustituir por las funciones de normales correspondientes. Por lo general, las aplicaciones deben trabajar completamente con funciones de un conjunto o el otro, y no deben intentar "mezclar y coincidir" funciones.



| Uniscribe (función) normal             | Función OpenType equivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Disposición de texto mediante Uniscribe

La aplicación puede usar los pasos siguientes para diseñar un párrafo de texto con Uniscribe. En este procedimiento se supone que la aplicación ya ha dividido el párrafo en ejecuciones.

1.  Llame a [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) solo cuando se inicie o cuando reciba un mensaje de [**\_ SETTINGCHANGE de WM**](../winmsg/wm-settingchange.md) .
2.  Opta Llame a [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) para determinar si el párrafo requiere procesamiento complejo.
3.  Opta Si utiliza Uniscribe para controlar la sustitución de texto bidireccional o de dígitos, llame a [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) para preparar las estructuras de [**\_ control de script**](/windows/win32/api/usp10/ns-usp10-script_control) y de [**\_ Estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) como entradas en [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). Si se omite este paso pero todavía se requiere la sustitución de dígitos, sustituya los dígitos nacionales para Unicode U + 0030 a U + 0039 (dígitos europeos). Para obtener información sobre la sustitución de dígitos, consulte [formas de dígitos](digit-shapes.md).
4.  Llame a [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para dividir el párrafo en elementos. Si no se usa la función Uniscribe para la sustitución de dígitos y se conoce el orden bidireccional, por ejemplo, debido a la distribución del teclado usada para escribir el carácter, llame a **ScriptItemize**. En la llamada, proporcione punteros NULL para las estructuras de [**\_ control de script**](/windows/win32/api/usp10/ns-usp10-script_control) y de [**\_ Estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) . Esta técnica genera elementos solo mediante el uso del motor de modelado y los elementos se pueden reordenar con la información del motor.
    > [!Note]  
    > Normalmente, las aplicaciones que funcionan solo con scripts de izquierda a derecha y sin ninguna sustitución de dígitos deben pasar punteros NULL para las estructuras de [**\_ control de script**](/windows/win32/api/usp10/ns-usp10-script_control) y de [**\_ Estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) .

     

5.  Combine la información del elemento con la información de ejecución para generar intervalos.
6.  Llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para identificar los clústeres y generar glifos.
7.  Si [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) devuelve el script de código USP \_ E \_ no está \_ \_ en \_ la fuente o es \_ correcto con la salida que contiene los glifos que faltan, seleccione caracteres de una fuente diferente. Puede sustituir otra fuente o deshabilitar la forma estableciendo el miembro **eScript** de la estructura de [**\_ análisis de scripts**](/windows/win32/api/usp10/ns-usp10-script_analysis) pasada a **ScriptShape** en un script \_ sin definir. Para obtener más información, vea [usar la reserva de fuentes](using-font-fallback.md).
8.  Llame a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar [anchos de avance](uniscribe-glossary.md) y posiciones x e y para los glifos en cada intervalo sucesivo. Este es el primer paso para el que el tamaño del texto se considera una consideración.
9.  Sumar los tamaños de intervalo hasta que la línea se desborda.
10. Divida el intervalo en un límite de palabras usando los miembros **fSoftBreak** y **fWhiteSpace** en los atributos lógicos. Para interrumpir un clúster de un solo carácter de la ejecución, use la información que se devuelve mediante una llamada a [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).
    > [!Note]  
    > Decida si el primer punto de código de un intervalo debe ser un punto de separación de palabras porque el último carácter del intervalo anterior lo requiere. Por ejemplo, si un intervalo finaliza en una coma, considere el primer carácter del siguiente intervalo para que sea un punto de separación de palabras.

     

11. Repita los pasos 6 a 10 para cada línea del párrafo. Sin embargo, si se interrumpe la última ejecución en la línea, llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cambiar la forma de la parte restante de la ejecución como la primera ejecución en la línea siguiente.

## <a name="display-text-using-uniscribe"></a>Mostrar texto mediante Uniscribe

La aplicación puede usar los pasos siguientes para mostrar un párrafo de texto. En este procedimiento se supone que la aplicación ya ha diseñado el texto y no ha guardado los glifos y posiciones del proceso de diseño. Si la velocidad es un problema, la aplicación puede guardar los glifos y posiciones del procedimiento de diseño y comenzar en el paso 2 del procedimiento de visualización.

> [!Note]  
> La aplicación puede omitir el paso 2 Si el texto no contiene caracteres de scripts de derecha a izquierda, no contiene caracteres de control bidireccionales y usa un nivel de incrustación de base de izquierda a derecha.

 

1.  Para cada ejecución, haga lo siguiente:
    1.  Si el estilo ha cambiado desde la última vez que se ejecutó, actualice el identificador al contexto del dispositivo mediante la liberación y la obtención de este.
    2.  Llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para generar glifos para la ejecución.
    3.  Llame a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar un ancho de avance y un desplazamiento x, y para cada glifo.
2.  Haga lo siguiente para establecer el orden visual correcto para las ejecuciones en la línea:
    1.  Extraiga una matriz de [niveles de incrustación](uniscribe-glossary.md)bidireccional, uno por intervalo. El nivel de incrustación se proporciona mediante (elemento de SCRIPT \_ ) si. ( \_Análisis de script). (SCRIPT \_ STATE) s. uBidiLevel.
    2.  Pase esta matriz a [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) para generar un mapa de posiciones visuales para las posiciones lógicas.
3.  Opta Para justificar el texto, llame a [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) o use un conocimiento especializado del texto.
4.  Use el mapa visual-to-Logical para mostrar las ejecuciones en orden visual. A partir del extremo izquierdo de la línea, llame a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para mostrar la ejecución proporcionada por la primera entrada en el mapa. Para cada entrada subsiguiente del mapa, llame a **ScriptTextOut** para mostrar la ejecución indicada a la derecha de la ejecución mostrada anteriormente.

    Si se omite el paso 2, empiece en el extremo izquierdo de la línea y llame a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para mostrar la primera ejecución lógica y, a continuación, muestre cada ejecución lógica a la derecha de la ejecución anterior.

5.  Repita los pasos anteriores para todas las líneas del párrafo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 

---
title: Cuadros de búsqueda
description: Con un cuadro de búsqueda, los usuarios pueden localizar rápidamente objetos o texto específicos dentro de un conjunto grande de datos mediante el filtrado o el resaltado de las coincidencias.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003292"
---
# <a name="search-boxes"></a>Cuadros de búsqueda

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un cuadro de búsqueda, los usuarios pueden localizar rápidamente objetos o texto específicos dentro de un conjunto grande de datos mediante el filtrado o el resaltado de las coincidencias. No hay ningún control de búsqueda estándar, pero debe procurar que las características de búsqueda de su programa sean coherentes con las de Windows.

Hay dos tipos de búsquedas:

-   **Búsqueda instantánea**, donde los resultados se muestran inmediatamente a medida que el usuario escribe. No es necesario hacer clic en ningún botón, por lo que el símbolo de búsqueda de lupa se muestra como un gráfico, no como un botón.

    ![Captura de pantalla que muestra un cuadro de búsqueda instantánea con una llamada "prompt" que señala al cuadro de búsqueda y una llamada de "buscar símbolo" que apunta al gráfico de lupa.](images/ctrl-search-boxes-image1.png)

    Un cuadro de búsqueda típico con búsqueda instantánea. La búsqueda se ejecuta automáticamente en cada pulsación de tecla.

-   **Búsqueda normal**, donde se realiza una búsqueda cuando el usuario hace clic en el botón Buscar. El símbolo de búsqueda de lupa se muestra en un botón.

    ![captura de pantalla de un cuadro de búsqueda normal ](images/ctrl-search-boxes-image2.png)

    Un cuadro de búsqueda típico mediante la búsqueda normal. Los usuarios hacen clic en un botón para realizar la búsqueda.

    Puede proporcionar uno o ambos tipos de opciones de búsqueda para los usuarios.

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Son difíciles de encontrar los objetos específicos?** Esto puede suceder cuando:
    -   Hay muchos objetos.
    -   Los objetos no se encuentran en una sola ubicación. La búsqueda es especialmente útil para buscar objetos en árboles.
    -   Los datos de búsqueda son difíciles de encontrar (por ejemplo, metadatos).
-   **¿Los usuarios necesitan encontrar texto específico dentro de los documentos?**
-   **¿La característica devuelve los resultados de búsqueda relevantes en un plazo de cinco segundos?** Si no es así, puede proporcionar una característica de búsqueda, pero usar un diseño alternativo que proporcione comentarios visibles para adaptarse a las búsquedas de larga duración, como un cuadro de diálogo de búsqueda.

## <a name="design-concepts"></a>Conceptos de diseño

La búsqueda es un primer paso fundamental en muchos escenarios: los usuarios deben buscar objetos para poder usarlos. Los usuarios están guardando más objetos en discos duros cada vez más grandes, pero la exploración de objetos no se escala bien. La búsqueda debe ser una parte sencilla, coherente y confiable de la experiencia del usuario.

Cuadros de búsqueda en Windows:

-   Forman parte de todas las ventanas del explorador, por lo que son fáciles de encontrar y reconocer.
-   Tienen una apariencia y un comportamiento coherentes.
-   Son eficientes y rápidos, lo que da lugar a resultados instantáneos en el modo de búsqueda instantánea.

Un cuadro de búsqueda se usa en Windows en estos lugares:

-   Exploradores
-   Experiencias (Microsoft Windows Media Player, Galería fotográfica de Windows, Windows Internet Explorer)
-   Menú Inicio (para buscar programas y archivos recientes)
-   Página principal del panel de control (para buscar elementos y tareas del panel de control)
-   Ayuda (para buscar temas de ayuda relevantes)

### <a name="look-and-feel"></a>Apariencia y funcionamiento

La sensación de buscar en Windows se ha mejorado significativamente mediante la compatibilidad con la búsqueda instantánea. Tener resultados instantáneos hace que Windows sea más eficaz y directo.

En el explorador de Windows y las ventanas de aplicación, la búsqueda se encuentra en la esquina superior derecha si se trata de un punto de entrada adicional. En este caso, los usuarios buscan un mecanismo de búsqueda cuando no encuentran lo que buscan en la ventana. Sin embargo, si la búsqueda es el punto de entrada principal, se centra en la parte superior de la ventana.

El botón buscar está conectado visualmente a un cuadro de búsqueda. Para minimizar el espacio, se usa un [símbolo del sistema](ctrl-text-boxes.md) opcional dentro de un cuadro de búsqueda en lugar de una etiqueta. El mensaje puede ser una instrucción (por ejemplo, escribir para buscar) o indicar el ámbito de la búsqueda (por ejemplo, buscar imágenes).

![captura de pantalla de un cuadro de búsqueda instantánea ](images/ctrl-search-boxes-image3.png)

Sin etiquetas y botones independientes, la búsqueda instantánea en Windows tiene una apariencia ligera.

Si realiza una búsqueda correcta, se crea una página virtual de los resultados de la búsqueda y se agrega a la pila de retroceso y a la barra de direcciones. Los usuarios tienen varias formas de restaurar la página original y borrar un cuadro de búsqueda, como hacer clic en atrás, hacer clic en la página original en la barra de direcciones, presionar ESC o borrar el cuadro de búsqueda.

Los usuarios también pueden borrar simplemente el cuadro de búsqueda sin restaurar una página anterior de resultados. En el modo de búsqueda instantánea, aparece un botón Borrar cuando el usuario comienza a escribir. una "x" reemplaza el símbolo de búsqueda de lupa. Al mantener el mouse, la "x" obtiene un aspecto del botón y se puede hacer clic en él.

![captura de pantalla de un cuadro de búsqueda con un icono ' x ' ](images/ctrl-search-boxes-image4.png)

El usuario puede borrar el cuadro de búsqueda si hace clic en "x" en el extremo derecho del control.

En el modo de búsqueda normal, el botón Borrar es opcional. Los usuarios pueden resultarle útil, por ejemplo, si una búsqueda tarda mucho tiempo en completarse. Los usuarios pueden hacer clic en la "x" para detener la búsqueda en curso. Si ya se ha completado una búsqueda, los usuarios pueden hacer clic en la "x" para borrar el cuadro de búsqueda.

## <a name="guidelines"></a>Directrices

### <a name="location"></a>Location

-   En las ventanas de la aplicación, busque búsqueda en la esquina superior derecha.
-   En ventanas emergentes, busque buscar siempre que sea más sensato y práctico.
-   **Excepción:** Si la búsqueda suele ser la primera cosa que realizan los usuarios en una ventana (el punto de entrada principal), se centra en la parte superior de la ventana.

### <a name="look"></a>Vere

-   Use los gráficos del botón de búsqueda estándar. Hay tres versiones:
    -   **Solo símbolo de búsqueda de lupa (no hay ningún botón al mantener el mouse).** Se usa para la búsqueda instantánea.
    -   **Símbolo de búsqueda de lupa con el botón.** Use cuando sea necesario hacer clic en el botón para iniciar la búsqueda.
    -   **Símbolo de búsqueda de lupa con el botón y la flecha desplegable.** Agregue una flecha desplegable cuando los usuarios puedan cambiar el ámbito o cuando haya otras opciones de configuración disponibles.
        -   En el caso de la búsqueda instantánea, use solo una flecha desplegable y muestre un botón al mantener el mouse.
        -   En el caso de la búsqueda normal, muestre la flecha desplegable de un botón.

![figura de cuadros de búsqueda instantánea en diferentes Estados ](images/ctrl-search-boxes-image5.png)

Especificaciones visuales para la búsqueda instantánea.

![figura de cuadros de búsqueda normales en diferentes Estados ](images/ctrl-search-boxes-image6.png)

Especificaciones visuales para la búsqueda normal.

-   No use una etiqueta; en su lugar, use un símbolo del sistema opcional. Si los usuarios tienden a suponer que la búsqueda es una búsqueda de archivos genérica, utilice el símbolo del sistema para dar el ámbito. De lo contrario, utilice el tipo para buscar o una frase similar y concisa.

    ![captura de pantalla del símbolo "escribir en la búsqueda" ](images/ctrl-search-boxes-image7.png)

    ![captura de pantalla del símbolo del sistema "Buscar todos los gadgets" ](images/ctrl-search-boxes-image8.png)

    En estos ejemplos, los mensajes de texto breves ayudan a los usuarios a trabajar con la búsqueda.

### <a name="interaction"></a>Interacción

-   **En el foco de entrada, seleccione automáticamente cualquier texto escrito anteriormente.** Esto permite a los usuarios escribir una nueva búsqueda escribiendo o para modificar la búsqueda anterior colocando el símbolo de intercalación usando las teclas de dirección.

    ![captura de pantalla del cuadro de búsqueda con texto resaltado ](images/ctrl-search-boxes-image9.png)

    En este ejemplo, el texto escrito anteriormente se selecciona en el foco de entrada.

-   **Asigne el método abreviado de teclado para el cuadro de búsqueda a Ctrl + E.**

### <a name="functionality"></a>Funcionalidad

-   **Permita la búsqueda instantánea siempre que sea posible.** Proporcione búsquedas normales e instantáneas si hay escenarios en los que la búsqueda regular merece el tiempo de espera adicional.
-   Las búsquedas normales deben devolver resultados relevantes en un plazo de cinco segundos y la búsqueda instantánea debe devolver los resultados en dos segundos. Después de este punto, es posible que la búsqueda continúe rellenando los resultados menos relevantes a lo largo del tiempo, siempre y cuando el programa responda y los usuarios puedan realizar otras tareas. Es posible que tenga que indexar los datos de búsqueda para garantizar esta capacidad de respuesta.
-   Si proporciona los modos de búsqueda normal e instantánea, los resultados de la búsqueda instantánea deben ser un subconjunto de los resultados de búsqueda normales.
-   Todas las búsquedas están basadas en el prefijo (no hay ninguna subcadena ni búsqueda de sufijos). El uso de caracteres comodín finales es opcional y no afecta a los resultados. Si se especifican varias palabras, use o busque.
-   Una búsqueda correcta agrega una página virtual con los resultados de la búsqueda a la pila de retroceso y a la barra de direcciones. Varias búsquedas dan como resultado una sola página virtual, por lo que si hace clic en atrás siempre se devuelve la página original.
-   Si es necesario para la escala, clasifique los resultados de la búsqueda por relevancia.
-   Una búsqueda en blanco devuelve la página original.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![figura del tamaño y espaciado del cuadro de búsqueda instantánea ](images/ctrl-search-boxes-image10.png)

Ajuste de tamaño y espaciado recomendados para la búsqueda instantánea.

![figura del tamaño y espaciado del cuadro de búsqueda normal ](images/ctrl-search-boxes-image11.png)

Ajuste de tamaño y espaciado recomendados para la búsqueda normal.

## <a name="text"></a>Texto

-   Para la redacción del mensaje en el cuadro de búsqueda, conviértalo en una instrucción (por ejemplo, escriba para buscar) o indique el ámbito de la búsqueda (por ejemplo, busque imágenes).
-   El texto del mensaje debe ser breve. Basta con una sola palabra o frase corta.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación o puntos suspensivos de finalización.

## <a name="documentation"></a>Documentación

-   Haga referencia a este control como el cuadro de búsqueda. Poner en mayúscula la letra inicial de la primera palabra; No ponga en mayúscula la primera letra de Box.
-   Consulte los dos tipos de búsqueda como búsqueda instantánea y búsqueda normal. Poner en mayúscula la primera letra de búsqueda instantánea; No ponga en mayúscula la letra inicial de la búsqueda normal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Glosario](glossary.md)
</dt> </dl>

 

 
---
title: Cuadros de búsqueda
description: Con un cuadro de búsqueda, los usuarios pueden localizar rápidamente objetos o texto específicos dentro de un gran conjunto de datos mediante el filtrado o resaltado de coincidencias.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 71e0ce45e2fd0b84b0abda9462f2cb42c945790e93ea06e7dfc6ece0f65ffd65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842981"
---
# <a name="search-boxes"></a>Cuadros de búsqueda

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un cuadro de búsqueda, los usuarios pueden localizar rápidamente objetos o texto específicos dentro de un gran conjunto de datos mediante el filtrado o resaltado de coincidencias. No hay ningún control de búsqueda estándar, pero debe procurar que las características de búsqueda del programa sean coherentes con las de Windows.

Hay dos tipos de búsquedas:

-   **Búsqueda instantánea,** donde los resultados se muestran inmediatamente como los tipos de usuario. No es necesario hacer clic en ningún botón, por lo que el símbolo de búsqueda de lupa se muestra como gráfico, no como botón.

    ![Captura de pantalla que muestra un cuadro de búsqueda instantánea con una llamada "Preguntar" que apunta al cuadro de búsqueda y una llamada "Símbolo de búsqueda" que apunta al gráfico de lupa.](images/ctrl-search-boxes-image1.png)

    Un cuadro de búsqueda típico que usa la búsqueda instantánea. La búsqueda se ejecuta automáticamente en cada pulsación de tecla.

-   **Búsqueda normal,** donde se realiza una búsqueda cuando el usuario hace clic en el botón de búsqueda. El símbolo de búsqueda de lupa se muestra en un botón.

    ![captura de pantalla de un cuadro de búsqueda normal ](images/ctrl-search-boxes-image2.png)

    Un cuadro de búsqueda típico que usa la búsqueda normal. Los usuarios hacen clic en un botón para realizar la búsqueda.

    Puede proporcionar a los usuarios uno o ambos tipos de opciones de búsqueda.

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Son difíciles de encontrar objetos específicos?** Esto puede suceder cuando:
    -   Hay muchos objetos .
    -   Los objetos no se encuentran en una sola ubicación. La búsqueda es especialmente útil para buscar objetos en árboles.
    -   Los datos de búsqueda son difíciles de encontrar (por ejemplo, metadatos).
-   **¿Los usuarios necesitan encontrar texto específico en los documentos?**
-   **¿La característica devuelve los resultados de búsqueda pertinentes en un plazo de cinco segundos?** Si no es así, puede proporcionar una característica de búsqueda, pero usar un diseño alternativo que proporcione comentarios visibles para dar cabida a búsquedas de larga duración, como un cuadro de diálogo de búsqueda.

## <a name="design-concepts"></a>Conceptos de diseño

La búsqueda es un primer paso fundamental en muchos escenarios: los usuarios deben encontrar objetos para poder usarlos. Los usuarios están guardando cada vez más objetos en discos duros cada vez más grandes, pero la exploración de objetos no se escala bien. La búsqueda debe ser una parte sencilla, coherente y confiable de la experiencia del usuario.

Cuadros de búsqueda en Windows:

-   Forman parte de todas las ventanas del Explorador, por lo que son fáciles de encontrar y reconocer.
-   Tener una apariencia y un comportamiento coherentes.
-   Son eficaces y rápidas, lo que ofrece resultados instantáneos en el modo de búsqueda instantánea.

Se usa un cuadro de búsqueda Windows en estos lugares:

-   Exploradores
-   Experiencias (Microsoft Reproductor de Windows Media, Windows Galería de fotos, Windows Internet Explorer)
-   menú Inicio (para buscar programas y archivos recientes)
-   Panel de control página principal (para buscar elementos y tareas del panel de control)
-   Ayuda (para buscar temas de Ayuda pertinentes)

### <a name="look-and-feel"></a>Look and feel

La sensación de búsqueda en Windows mejora significativamente al admitir la búsqueda instantánea. Tener resultados instantáneos hace que Windows sea más eficaz y directo.

En Windows explorador y ventanas de aplicación, la búsqueda se encuentra en la esquina superior derecha si es un punto de entrada complementario. En este caso, los usuarios buscan un mecanismo de búsqueda cuando no encuentran lo que buscan en la ventana. Sin embargo, si Search es el punto de entrada principal, se centra en la parte superior de la ventana.

El botón Buscar está conectado visualmente a un cuadro de búsqueda. Para minimizar el espacio, se usa un [mensaje](ctrl-text-boxes.md) opcional dentro de un cuadro de búsqueda en lugar de una etiqueta. El aviso puede ser una instrucción (por ejemplo, Tipo de búsqueda) o indicar el ámbito de la búsqueda (por ejemplo, Buscar imágenes).

![captura de pantalla de un cuadro de búsqueda instantánea ](images/ctrl-search-boxes-image3.png)

Sin etiquetas y botones independientes, la búsqueda instantánea en Windows tiene un aspecto ligero.

Al realizar una búsqueda correcta, se crea una página virtual de los resultados de la búsqueda y se agrega a la pila atrás y a la barra de direcciones. Los usuarios tienen varias maneras de restaurar la página original y borrar un cuadro de búsqueda, como hacer clic en Atrás, hacer clic en la página original en la barra de direcciones, presionar Esc o desactivar el cuadro De búsqueda.

Los usuarios también pueden borrar simplemente el cuadro de búsqueda sin restaurar una página anterior de resultados. En el modo de búsqueda instantánea, aparece un botón Borrar después de que el usuario empiece a escribir. una "x" reemplaza el símbolo de búsqueda de lupa. Al mantener el puntero, la "x" obtiene un aspecto de botón y se puede hacer clic en él.

![captura de pantalla de un cuadro de búsqueda con un icono "x" ](images/ctrl-search-boxes-image4.png)

El usuario puede borrar el cuadro de búsqueda haciendo clic en "x" en el extremo derecho del control.

En el modo de búsqueda normal, el botón Borrar es opcional. Los usuarios pueden resultar útiles, por ejemplo, si una búsqueda tarda mucho tiempo en completarse. Los usuarios pueden hacer clic en la "x" para detener la búsqueda en curso. Si ya se ha completado una búsqueda, los usuarios pueden hacer clic en la "x" para borrar el cuadro buscar.

## <a name="guidelines"></a>Directrices

### <a name="location"></a>Ubicación

-   Para las ventanas de aplicación, busque Buscar en la esquina superior derecha.
-   En el caso de las ventanas emergentes, busque Buscar siempre que sea más razonable y conveniente.
-   **Excepción:** Si la búsqueda suele ser lo primero que hacen los usuarios en una ventana (el punto de entrada principal), centre esta en la parte superior de la ventana.

### <a name="look"></a>Mira

-   Use los gráficos del botón de búsqueda estándar. Hay tres versiones:
    -   **Solo símbolo de búsqueda de lupa (sin botón al mantener el puntero).** Use para la búsqueda instantánea.
    -   **Símbolo de búsqueda de lupa con botón.** Use cuando sea necesario hacer clic en el botón para iniciar la búsqueda.
    -   **Símbolo de búsqueda de lupa con botón y flecha desplegable.** Agregue una flecha desplegable cuando los usuarios puedan cambiar el ámbito o cuando haya otras opciones disponibles.
        -   En Búsqueda instantánea, use solo una flecha desplegable y muestre un botón al mantener el puntero.
        -   Para una búsqueda normal, muestre la flecha desplegable en un botón.

![figura de cuadros de búsqueda instantánea en distintos estados ](images/ctrl-search-boxes-image5.png)

Especificaciones visuales para la búsqueda instantánea.

![figura de cuadros de búsqueda normales en distintos estados ](images/ctrl-search-boxes-image6.png)

Especificaciones visuales para la búsqueda normal.

-   No use una etiqueta; use un símbolo del sistema opcional en su lugar. Si los usuarios tienden a asumir que la búsqueda es una búsqueda de archivos genérica, use el símbolo del sistema para proporcionar el ámbito. De lo contrario, use Tipo para buscar o una frase similar y concisa.

    ![captura de pantalla del símbolo del sistema "type to search" ](images/ctrl-search-boxes-image7.png)

    ![captura de pantalla del símbolo del sistema "buscar todos los guiones" ](images/ctrl-search-boxes-image8.png)

    En estos ejemplos, breves mensajes textuales ayudan a los usuarios a trabajar con Search.

### <a name="interaction"></a>Interacción

-   **En el foco de entrada, seleccione automáticamente cualquier texto especificado previamente.** Esto permite a los usuarios escribir una nueva búsqueda escribiendo o modificar la búsqueda anterior colocando el cursor de cursor mediante las teclas de dirección.

    ![captura de pantalla del cuadro de búsqueda con texto resaltado ](images/ctrl-search-boxes-image9.png)

    En este ejemplo, el texto especificado previamente está seleccionado en el foco de entrada.

-   **Asigne el método abreviado de teclado para que el cuadro de búsqueda sea Ctrl+E.**

### <a name="functionality"></a>Funcionalidad

-   **Admitir la búsqueda instantánea siempre que sea posible.** Proporcione búsquedas periódicas e instantáneas si hay escenarios en los que la búsqueda normal merece la pena el tiempo de espera adicional.
-   Las búsquedas normales deben devolver los resultados pertinentes en un plazo de cinco segundos y la búsqueda instantánea debe devolver resultados en dos segundos. Después de este punto, la búsqueda puede seguir rellenando resultados menos relevantes con el tiempo, siempre y cuando el programa responda y los usuarios puedan realizar otras tareas. Es posible que tenga que indexar los datos de búsqueda para garantizar esta capacidad de respuesta.
-   Si proporciona los modos de búsqueda normal e instantánea, los resultados de búsqueda instantánea deben ser un subconjunto de los resultados de búsqueda normales.
-   Todas las búsquedas se basan en prefijos (sin subcadena ni búsqueda de sufijos). El uso de caracteres comodín finales es opcional y no afecta a los resultados. Si se introducen varias palabras, use la búsqueda OR.
-   Una búsqueda correcta agrega una página virtual con los resultados de la búsqueda a la barra Pila atrás y Dirección. Varias búsquedas tienen como resultado una sola página virtual, por lo que al hacer clic en Atrás siempre se devuelve la página original.
-   Si es necesario para la escala, clasifice los resultados de la búsqueda por relevancia.
-   Una búsqueda en blanco devuelve la página original.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![figura de tamaño y espaciado del cuadro de búsqueda instantánea ](images/ctrl-search-boxes-image10.png)

Tamaño y espaciado recomendados para la búsqueda instantánea.

![figura de tamaño y espaciado normales del cuadro de búsqueda ](images/ctrl-search-boxes-image11.png)

Tamaño y espaciado recomendados para la búsqueda normal.

## <a name="text"></a>Texto

-   Para la redacción del símbolo del sistema en el cuadro Buscar, conséctela como una instrucción (por ejemplo, Escriba para buscar) o indique el ámbito de la búsqueda (por ejemplo, Buscar imágenes).
-   El texto del aviso debe ser breve. Una sola palabra o frase corta debe ser suficiente.
-   Use mayúsculas de estilo de frase.
-   No use signos de puntuación finales ni puntos suspensivos.

## <a name="documentation"></a>Documentación

-   Consulte este control como cuadro de búsqueda. Capitalice la letra inicial de la primera palabra; no escriba en mayúsculas la letra inicial del cuadro.
-   Consulte los dos tipos de búsqueda como Búsqueda instantánea y Búsqueda normal. Uso de mayúsculas y minúsculas en la letra inicial de Búsqueda instantánea; no capitalice la letra inicial de la búsqueda normal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Glosario](glossary.md)
</dt> </dl>

 

 
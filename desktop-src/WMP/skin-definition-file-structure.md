---
title: Estructura del archivo de definición de máscara
description: Estructura del archivo de definición de máscara
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Reproductor de Windows Media máscaras, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c708e46f93e2d00820015a04b0f467da2deafe59e4dbafb0b9e4f3fb8660271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995285"
---
# <a name="skin-definition-file-structure"></a>Estructura del archivo de definición de máscara

El archivo de definición de máscara debe seguir una estructura específica. Empiece con un **elemento THEME,** cree uno o varios elementos **VIEW** y, a continuación, defina cada elemento **VIEW** con los elementos de la interfaz de usuario adecuados para el tipo de vista que desea usar.

## <a name="theme-elements"></a>ELEMENTOS THEME

En el nivel superior, debe iniciar el archivo de definición de máscara con el **elemento THEME** y cerrar con él.


```C++
<THEME>
    ...
</THEME>

```



El **elemento THEME** es el elemento raíz de la máscara. Solo puede haber un **elemento THEME** en un archivo de definición de máscara y debe estar en el nivel superior. **Los** elementos THEME tienen atributos de ambiente y específicos, aunque la mayoría de las veces no será necesario usarlos. Para obtener más información sobre estos atributos, vea la [Referencia de programación de máscaras](skin-programming-reference.md).

## <a name="view-elements"></a>Elementos VIEW

Cada **THEME** debe tener al menos un **elemento VIEW.** El **elemento VIEW** rige la imagen determinada que se ve en la pantalla. Es posible que quiera tener más de una vista, por lo que puede cambiar de un lado a otro. Por ejemplo, es posible que quiera tener una vista grande para trabajar con listas de reproducción, una vista media para ver visualizaciones y una pequeña vista que se ajuste a una esquina de la pantalla.

Si va a crear varias vistas, querrá asegurarse de  que cada vista tiene un valor de atributo de identificador único que se usará para identificar la vista. Debe definir el atributo **backgroundImage** o la vista no tendrá ninguna imagen inicial. Si no desea mostrar una imagen rectangular, es probable que quiera usar el atributo **clippingColor** para definir las áreas de la máscara que no se mostrarán y probablemente quiera establecer el atributo **titleBar** del elemento **VIEW.**

Cada **elemento VIEW** también puede tener uno o varios elementos **SUBVIEW.** Un **elemento SUBVIEW** es similar a **view** y se puede usar para partes de la máscara que quiera mover, ocultar o mostrar. Por ejemplo, se podría usar un elemento **SUBVIEW** para crear una bandeja deslizante que sale de la máscara para mostrar un igualador gráfico. **Los elementos SUBVIEW** se pueden alinear con **VIEW** y tener otras relaciones especiales con **view**.

## <a name="initializing-windows-media-player"></a>Inicializar Reproductor de Windows Media

Puede establecer ciertas propiedades iniciales de Reproductor de Windows Media mediante los elementos **PLAYER**, **SETTINGS** **y CONTROLS.** Por ejemplo, podría establecer el volumen en un nivel inicial o dar un valor predeterminado para un nombre de archivo.

El código siguiente muestra cómo establecer el valor **de dirección URL** en una máscara:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Si quisiera establecer el atributo **autoStart** de **SETTINGS** en False, usaría el código siguiente:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Tenga en cuenta que **el elemento SETTINGS** está anidado dentro del elemento **PLAYER.**

Con estos elementos, se pueden especificar los siguientes atributos y eventos en tiempo de diseño:

**Atributos del elemento PLAYER**

-   **url**
-   **de respuesta**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **Error**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtalterschange**

**Atributos del elemento SETTINGS**

-   **Autostart**
-   **equilibrar**
-   **Baseurl**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **Mudo**
-   **playCount**
-   **Tasa**
-   **volume**

## <a name="controls-element-attributes"></a>Atributos del elemento CONTROLS

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Otros Interfaz de usuario elementos

Una vez que haya definido los elementos **THEME** **y VIEW,** debe rellenar **la vista** con elementos específicos de la interfaz de usuario. No es necesario usar todos los elementos disponibles en una máscara, solo los que necesita.

Si el usuario puede ver un elemento, se denomina control . Los controles siguientes están disponibles para las máscaras:

-   Botones
-   Controles deslizantes, controles deslizantes personalizados y barras de progreso
-   Cuadros de texto
-   Ventanas de vídeo
-   Ventanas de visualización
-   Ventanas de lista de reproducción
-   Ventanas de subvista

Además, se pueden usar varios elementos para definir aún más Reproductor de Windows Media acciones, pero requieren elementos visuales como botones o controles deslizantes:

-   Configuración de vídeo
-   Equalizer Configuración
-   Configuración de visualización

## <a name="buttons"></a>Botones

Los botones son la parte más popular de una máscara. Puede usar botones para desencadenar acciones como reproducir, detener, salir, minimizar y cambiar a una vista diferente. Reproductor de Windows Media proporciona al creador de máscaras dos tipos de elementos de botón: **el elemento BUTTON** y el elemento **BUTTONGROUP.** Además, hay varios tipos predefinidos de botones.

-   **Elemento BUTTON.** El **elemento BUTTON** se usa para botones individuales. Si usa el **elemento BUTTON,** debe proporcionar una imagen para cada botón y definir la ubicación exacta donde desea que el botón aparezca en relación con la imagen de fondo. Una de las ventajas del elemento **BUTTON** es que puede cambiar la imagen del botón dinámicamente.
-   **Elemento BUTTONGROUP.** El **elemento BUTTONGROUP** se usa para grupos de botones. De hecho, debe incluir cada elemento **BUTTONGROUP** con un par de **etiquetas BUTTONGROUP.** El uso de grupos de botones es más fácil que usar botones individuales porque no es necesario especificar la ubicación exacta de cada botón. En su lugar, proporcione un mapa de imagen independiente que defina las acciones que tendrán lugar cuando el mouse mantenga el puntero sobre un área del fondo o haga clic en ella. El uso de mapas de imágenes es fácil porque puede tomar el arte que creó para el fondo y copiarlo en una capa de asignación en el programa de edición de gráficos. El uso del programa de edición de gráficos es más rápido y preciso que intentar definir exactamente dónde debe colocarse un botón individual en el fondo.
-   **Botones predefinidos.** Hay varios botones predefinidos. Por ejemplo, puede usar un botón PLAYELEMENT para reproducir archivos multimedia digitales y un ELEMENTO STOPELEMENT para detener la reproducción. Vea [Elemento BUTTONGROUP](buttongroup-element.md) y [Elemento BUTTON en](button-element.md) la Referencia de programación de máscaras. IMAGEBUTTON [se](imagebutton.md) puede usar para mostrar imágenes que pueden cambiar en respuesta a eventos específicos.

## <a name="sliders"></a>Controles deslizantes

Los controles deslizantes son útiles para trabajar con información que cambia con el tiempo. Por ejemplo, puede usar un control deslizante para indicar la cantidad de música que ya se ha reproducdo para un archivo multimedia determinado. Los controles deslizantes pueden ser horizontales o verticales, lineales o circulares, o cualquier forma que se pueda pensar. Los controles deslizantes se incluyen en tres variedades: controles deslizantes, barras de progreso y controles deslizantes personalizados.

-   **Deslizadores.** Puede usar el elemento **SLIDER para** los controles de volumen o para permitir que el usuario se mueva a otra parte del contenido multimedia.
-   **Barras de progreso.** Las barras de progreso son similares a los controles deslizantes. Las barras de progreso están diseñadas para mostrar gráficamente el porcentaje de un proceso determinado que se ha completado, pero no para un proceso con el que el usuario querrá interactuar. Por ejemplo, puede usar una barra de progreso para indicar el progreso del almacenamiento en búfer.
-   **Controles deslizantes personalizados.** Se proporciona funcionalidad de control deslizante personalizado para que pueda crear controles como botones o crear mecanismos de control inusuales. Por ejemplo, si desea crear un control de volumen que se ajuste alrededor de la máscara, puede hacerlo con un control deslizante personalizado. Para configurar el control deslizante personalizado, debe crear un mapa de imágenes que contenga imágenes de escala de grises para definir las ubicaciones de los valores en el control deslizante. Esto es relativamente fácil de hacer con un programa de edición de gráficos que admite capas.

## <a name="text"></a>Texto

Puede usar el elemento **TEXT** para mostrar texto en la máscara, como títulos de canciones.

## <a name="video"></a>Vídeo

Puede mostrar vídeo en la máscara. El **elemento VIDEO** permite establecer el tamaño y la posición de la ventana de vídeo.

También puede permitir que el usuario cambie la configuración del vídeo con el **elemento VIDEOSETTINGS.** Por ejemplo, puede crear controles para ajustar el brillo del vídeo.

Si no proporciona un elemento de vídeo y el contenido contiene vídeo, Reproductor de Windows Media volverá al modo completo y no se mostrará la máscara.

## <a name="equalizer-settings"></a>Equalizer Configuración

Puede establecer el filtrado para bandas de frecuencia de audio específicas mediante el **elemento EQUALIZERSETTINGS.** Puede aumentar los sonidos, ajustar los triples y configurar los sonidos para que coincidan con los oídos o la sala.

## <a name="visualizations"></a>Visualizaciones

Puede mostrar visualizaciones en la máscara. Las visualizaciones son efectos visuales que cambian con el tiempo a medida que el audio se reproduce Reproductor de Windows Media. El **elemento EFFECTS** determina dónde se reproducirán las visualizaciones, qué tamaño tendrá la ventana y qué visualizaciones se reproducirán.

## <a name="playlists"></a>Listas

Puede usar el elemento **PLAYLIST** para permitir que el usuario seleccione un elemento de una lista de reproducción específica.

## <a name="subviews"></a>Subvistas

Puede usar el elemento **SUBVIEW para** mostrar conjuntos secundarios de controles de interfaz, como una lista de reproducción o controles de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 





---
title: Estructura del archivo de definición de máscara
description: Estructura del archivo de definición de máscara
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Aspectos de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075989"
---
# <a name="skin-definition-file-structure"></a>Estructura del archivo de definición de máscara

El archivo de definición de máscara debe seguir una estructura específica. Empiece con un elemento de **tema** , cree uno o varios elementos de **vista** y, a continuación, defina cada elemento de **vista** con los elementos de la interfaz de usuario adecuados para el tipo de vista que desee usar.

## <a name="theme-elements"></a>Elementos de tema

En el nivel superior, debe iniciar el archivo de definición de máscara con el elemento de **tema** y cerrar con él.


```C++
<THEME>
    ...
</THEME>

```



El elemento **Theme** es el elemento raíz de la máscara. Solo puede haber un elemento de **tema** en un archivo de definición de máscara y debe estar en el nivel superior. Los elementos de **tema** tienen atributos específicos y de ambiente, aunque la mayoría de las veces no necesitará usarlos. Para obtener más información sobre estos atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.

## <a name="view-elements"></a>Elementos de vista

Cada **tema** debe tener al menos un elemento de **vista** . El elemento de **vista** rige la imagen determinada que se ve en la pantalla. Puede que desee tener más de una vista, de modo que pueda cambiar de una a otra. Por ejemplo, puede que desee tener una vista grande para trabajar con listas de reproducción, una vista mediana para ver visualizaciones y una vista pequeña que quepa en una esquina de la pantalla.

Si va a crear varias vistas, querrá asegurarse de que cada vista tiene un valor de atributo de **identificador** único que se utilizará para identificar la vista. Debe definir el atributo **BackgroundImage** o la vista no tendrá ninguna imagen de inicio. Si no desea mostrar una imagen rectangular, probablemente querrá usar el atributo **clippingColor** para definir las áreas de la máscara que no se mostrarán, y es probable que desee establecer el atributo **TitleBar** del elemento de **vista** .

Cada elemento de **vista** también puede tener uno o más elementos de **vista previa** . Un elemento de **subvista** es similar a una **vista** y se puede usar para las partes de la máscara que desea desplazar, ocultar o mostrar. Por ejemplo, un elemento de una **subvista** podría usarse para crear una bandeja deslizante que extrae de la máscara para mostrar un ecualizador gráfico. Los elementos de la vista **previa** se pueden alinear con la **vista** y tienen otras relaciones especiales con la **vista**.

## <a name="initializing-windows-media-player"></a>Inicializar Media Player de Windows

Puede establecer ciertas propiedades iniciales de Windows Media Player mediante los elementos **Player**, **Settings** y **Controls** . Por ejemplo, puede establecer el volumen en un nivel inicial o asignar un valor predeterminado a un nombre de archivo.

En el código siguiente se muestra cómo establecer el valor de la **dirección URL** en una máscara:


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



Si desea establecer el atributo **autoStart** de **Settings** en false, usaría el código siguiente:


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



Tenga en cuenta que el elemento **Settings** está anidado dentro del elemento **Player** .

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
-   **Mtatuschange**

**Atributos del elemento SETTINGs**

-   **Automáticamente**
-   **balancea**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **silenciar**
-   **playCount**
-   **Rate**
-   **volume**

## <a name="controls-element-attributes"></a>Atributos del elemento CONTROLs

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>Otros elementos de la interfaz de usuario

Una vez que haya definido los elementos de **vista** y **tema** , debe rellenar la **vista** con elementos específicos de la interfaz de usuario. No tiene que utilizar todos los elementos disponibles en una máscara, solo los que necesita.

Si el usuario puede visualizar un elemento, se denomina control. Los siguientes controles están disponibles para las máscaras:

-   Botones
-   Controles deslizantes, controles deslizantes personalizados y barras de progreso
-   Cuadros de texto
-   Ventanas de vídeo
-   Ventanas de visualización
-   Ventanas de lista de reproducción
-   Ventanas de subvista

Además, se pueden utilizar varios elementos para definir con mayor precisión las acciones de Media Player de Windows, pero requieren elementos visuales como botones o controles deslizantes:

-   Configuración de vídeo
-   Configuración del ecualizador
-   Configuración de visualización

## <a name="buttons"></a>Botones

Los botones son la parte más popular de una máscara. Puede usar botones para desencadenar acciones como reproducir, detener, salir, minimizar y cambiar a vista diferente. Windows Media Player proporciona el creador de la máscara con dos tipos de elementos Button: el elemento **Button** y el elemento **BUTTONGROUP** . Además, hay varios tipos de botones predefinidos.

-   **Elemento BUTTON.** El elemento **Button** se usa para botones individuales. Si usa el elemento de **botón** , debe proporcionar una imagen para cada botón y definir la ubicación exacta en la que desea que aparezca el botón en relación con la imagen de fondo. Una de las ventajas del elemento **Button** es que puede cambiar dinámicamente la imagen del botón.
-   **Elemento BUTTONGROUP.** El elemento **BUTTONGROUP** se usa para grupos de botones. De hecho, debe incluir cada elemento **BUTTONGROUP** con un par de etiquetas **BUTTONGROUP** . El uso de grupos de botones es más fácil que usar botones individuales, ya que no es necesario especificar la ubicación exacta de cada botón. En su lugar, se proporciona un mapa de imágenes independiente que define las acciones que tendrán lugar cuando se mantenga el mouse sobre un área en el fondo. El uso de mapas de imagen es fácil porque puede tomar el arte que ha creado para el fondo y copiarlo en una capa de asignación en el programa de edición de gráficos. Usar el programa de edición de gráficos es más rápido y preciso que intentar definir exactamente dónde se debe colocar un botón individual en el fondo.
-   **Botones predefinidos.** Hay varios botones predefinidos. Por ejemplo, puede usar un botón PLAYELEMENT para reproducir archivos multimedia digitales y un STOPELEMENT para detener la reproducción. Vea elemento [BUTTONGROUP](buttongroup-element.md) y el [elemento Button](button-element.md) en la referencia de programación de la máscara. El [IMAGEBUTTON](imagebutton.md) se puede usar para mostrar imágenes que pueden cambiar en respuesta a eventos específicos.

## <a name="sliders"></a>Controles deslizantes

Los controles deslizantes son útiles para trabajar con información que cambia con el tiempo. Por ejemplo, puede usar un control deslizante para indicar la cantidad de música que ya ha jugado para un archivo multimedia determinado. Los controles deslizantes pueden ser horizontales o verticales, lineales o circulares, o cualquier forma que pueda considerar. Los controles deslizantes tienen tres variedades: controles deslizantes, barras de progreso y controles deslizantes personalizados.

-   **Controles deslizantes.** Puede usar el elemento **Slider** para controles de volumen o para permitir que el usuario se mueva a otra parte del contenido multimedia.
-   **Barras de progreso.** Las barras de progreso son similares a los controles deslizantes. Las barras de progreso están diseñadas para mostrar gráficamente el porcentaje de un proceso determinado que se ha completado, pero no para un proceso con el que el usuario desea interactuar. Por ejemplo, puede que desee usar una barra de progreso para indicar el progreso del almacenamiento en búfer.
-   **Controles deslizantes personalizados.** Se proporciona funcionalidad de control deslizante personalizado para que pueda crear controles, como botones, o crear mecanismos de control inusuales. Por ejemplo, si desea crear un control de volumen que se ajuste alrededor de la máscara, puede hacerlo con un control deslizante personalizado. Para configurar el control deslizante personalizado, debe crear un mapa de imágenes que contenga imágenes de escala de grises para definir las ubicaciones de los valores en el control deslizante. Esto es relativamente fácil de hacer con un programa de edición de gráficos que admita capas.

## <a name="text"></a>Texto

Puede usar el elemento de **texto** para mostrar texto en la máscara, como títulos de canciones.

## <a name="video"></a>Vídeo

Puede mostrar vídeo en la máscara. El elemento de **vídeo** le permite establecer el tamaño y la posición de la ventana de vídeo.

También puede permitir que el usuario cambie la configuración de vídeo con el elemento de **configuración** de videojuegos. Por ejemplo, puede crear controles para ajustar el brillo del vídeo.

Si no se proporciona un elemento de vídeo y el contenido contiene vídeo, Windows Media Player volverá al modo completo y no se mostrará la máscara.

## <a name="equalizer-settings"></a>Configuración del ecualizador

Puede establecer el filtrado para bandas de frecuencia de audio específicas mediante el elemento **EQUALIZERSETTINGS** . Puede aumentar el valor de graves, retocar el agudo y configurar sus sonidos para que se adapten a sus oídos o a su salón.

## <a name="visualizations"></a>Visualizaciones

Puede mostrar visualizaciones en la máscara. Las visualizaciones son efectos visuales que cambian con el tiempo a medida que el audio se reproduce a través de Windows Media Player. El elemento **Effects** determina dónde se reproducirán las visualizaciones, el tamaño de la ventana y las visualizaciones que se reproducirán.

## <a name="playlists"></a>Reproducción

Puede usar el elemento de **lista de reproducción** para permitir que el usuario seleccione un elemento de una lista de reproducción específica.

## <a name="subviews"></a>Subvistas

Puede utilizar el elemento de la **subvista** para mostrar los conjuntos secundarios de controles de interfaz, como una lista de reproducción o un control de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 





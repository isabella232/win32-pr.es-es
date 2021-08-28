---
description: Las siguientes constantes especifican el conjunto válido de propiedades de Windows del analizador de adquisición de imágenes (WIA).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes de propiedad de elemento WIA del analizador (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 008a806ccaebd595fe7a67ff8f98e6a9385b0bf2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882703"
---
# <a name="scanner-wia-item-property-constants"></a>Constantes de propiedad de elemento WIA del analizador

Las siguientes constantes especifican el conjunto válido de propiedades de Windows del analizador de adquisición de imágenes (WIA).

El prefijo "WIA IPS" indica una propiedad item para dispositivos scanner y es la convención de nomenclatura usada \_ \_ en C/C++. Con fines de scripting, estas constantes usan el prefijo "ScannerPicture" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante o valor</th>
<th >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskdeskdesk</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
<br/> Activa o desactiva el escritorio automático.<br/> Opcional solo para WIA_CATEGORY_FEEDER.<br/> Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Active el escritorio automático.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Desactive el escritorio automático.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </dl></td>
<td ><p>Los valores de brillo de la imagen disponibles en el analizador.</p>
<p>Contiene la configuración de brillo de hardware actual para el dispositivo. Una aplicación establece esta propiedad en el valor de brillo del hardware. El minidriver crea y mantiene esta propiedad.</p>
<p>Los valores se deben asignar en un intervalo de -1000 a 1000, donde 1000 corresponde al brillo máximo, 0 corresponde al brillo normal y -1000 corresponde al brillo mínimo.</p>
<p>Obligatorio para todos los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM. Opcional, pero recomendado, para los WIA_CATEGORY_FINISHED_FILE que admiten vistas previas.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </dl></td>
<td ><p>Contiene la configuración de contraste de hardware actual para un dispositivo. Una aplicación establece esta propiedad en el valor de contraste del hardware. El minidriver crea y mantiene esta propiedad.</p>
<p>Los valores se deben asignar en un intervalo de -1000 a 1000, donde -1000 corresponde al contraste mínimo, 0 corresponde al contraste normal y 1000 corresponde al contraste máximo.</p>
<p>Obligatorio para todos los elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM. Opcional, pero recomendado, para los WIA_CATEGORY_FINISHED_FILE que admiten vistas previas.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </dl></td>
<td ><p>Contiene la configuración de intención actual. El minidriver crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong> acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>El controlador los usa para preestablecidar las propiedades de los elementos en función del uso previsto de la imagen por parte de una aplicación. Esto puede incluir, por ejemplo, la calidad máxima, el tamaño mínimo, y así sucesivamente.</p>
<p>El controlador elige la profundidad de bits, en puntos por pulgada, y otras configuraciones que determina son adecuadas para la intención seleccionada. La aplicación debe leer la configuración actual para determinar qué propiedades se cambiaron. Una aplicación establece esta propiedad para establecer automáticamente las propiedades de WIA para una intención de adquisición específica. Esta propiedad es necesaria para todos los analizadores.</p>
<p>Una aplicación establece esta propiedad para establecer automáticamente las propiedades de WIA para una intención de adquisición específica.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Las marcas se pueden combinar con un operador <strong>OR</strong> bit a bit, pero una imagen no puede ser de escala de grises ni de color.
</blockquote>
</div>
<div>
 
</div>
<p>Esta propiedad es necesaria para todos los analizadores.</p>
<p>La tabla siguiente contiene las marcas de tipo de imagen y sus definiciones. Estas marcas se usan para establecer el tipo de imagen que se pretende: color, escala de grises, y así sucesivamente.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Marcas de tipo de imagen previstas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Valor predeterminado. No se especifica ninguna intención.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>La aplicación pretende preparar el dispositivo para un examen de color.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>La aplicación pretende preparar el dispositivo para un examen de escala de grises.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>La aplicación pretende preparar el dispositivo para examinar el texto.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Máscara para todas las marcas de tipo de imagen.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La tabla siguiente contiene las marcas de calidad y tamaño y sus definiciones. Estas marcas se usan para establecer qué nivel de calidad está previsto.</p>

<table>
<thead>
<tr class="header">
<th>Marcas de calidad y tamaño de imagen previstos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>La aplicación pretende preparar el dispositivo para examinar una imagen que se encuentra en un examen pequeño.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>La aplicación pretende preparar el dispositivo para examinar una imagen de alta calidad.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Esta marca es una máscara para todas las marcas de tamaño y calidad.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>La aplicación pretende preparar el dispositivo para examinar una versión preliminar.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskdeskdeskx</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el número de píxeles en la dirección X desde WIA_IPS_XPOS hasta la coordenada x de la esquina superior de la imagen que se va a escritorio. Por lo tanto, describe, junto con WIA_IPS_DESKEW_Y, dónde se encuentran las dos esquinas superiores de la imagen sesgada dentro del rectángulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT y WIA_IPS_YEXTENT. El controlador del analizador implementa su propiedad si admite el escritorio.</p>
<p>Los valores válidos para WIA_IPS_DESKEW_X deben estar entre 0 y (WIA_IPS_XEXTENT - 1). Un valor de 0 significa que no se debe realizar ninguna operación de escritorio.</p>
<p>Esta propiedad es opcional para los elementos de las categorías WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM; y no está disponible para WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskdesky</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el número de píxeles en la dirección Y desde WIA_IPS_YPOS hasta la coordenada y de la esquina más izquierda de la imagen que se va a desenvolcar. Por lo tanto, describe, junto con WIA_IPS_DESKEW_X, dónde se encuentran las dos esquinas superiores de la imagen sesgada dentro del rectángulo delimitador definido por WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT y WIA_IPS_YEXTENT. El controlador del analizador implementa esta propiedad si admite el escritorio.</p>
<p>Los valores válidos para WIA_IPS_DESKEW_Y deben estar entre 0 y (WIA_IPS_YEXTENT - 1). Un valor de 0 significa que no se debe realizar ninguna operación de escritorio.</p>
<p>Esta propiedad es opcional para los elementos de las categorías WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM; y no está disponible para WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el origen y el modo de adquisición del analizador actual. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar el origen de adquisición actual del analizador o para escribir esta propiedad para establecer el origen y el modo del analizador. Además, las aplicaciones usan esta propiedad para habilitar y deshabilitar la funcionalidad del dúplex.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DUPLEX</td>
<td>Examen mediante operaciones de dúplex. Examinar ambos lados del documento mediante la configuración común configurada para el elemento de fuente (WIA_CATEGORY_FEEDER). DÚPLEX y ADVANCE_DUPLEX no se pueden establecer.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Examinar mediante la configuración individual configurada para cada elemento de fuente secundario (WIA_CATEGORY_FEEDER_FRONT y WIA_CATEGORY_FEEDER_BACK). DÚPLEX y ADVANCE_DUPLEX no se pueden establecer.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Examinar primero la parte frontal del documento. Este valor es válido cuando se establece DÚPLEX ADVANCED_DUPLEX dúplex.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Examinar primero la parte posterior del documento. Este valor es válido cuando se establece DÚPLEX ADVANCED_DUPLEX dúplex.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Examinar solo la parte frontal.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Examinar solo la parte posterior. Este valor es válido cuando se establece DÚPLEX ADVANCED_DUPLEX dúplex.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureNodeName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Habilita la especificación de un archivo adjunto de análisis de películas determinado cuando hay más de uno.</p>
<p>Esta propiedad es necesaria para los elementos WIA_CATEGORY_FILM cuando hay varios elementos de examen de películas. Si el dispositivo solo admite un elemento de película de escáner raíz, esta propiedad es opcional.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Valores permitidos: el BSTR debe tener el formato ,- ResourceID para permitir la localización, ya que esta cadena se exponería al usuario a través de la interfaz de usuario @ResourceBinary &lt; de examen de &gt; películas.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureScanMode</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Habilita la configuración del examen de películas actual.</p>
<p>Esta propiedad es necesaria para el WIA_CATEGORY_FILM elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Buscar una diapositiva de color.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Buscar un color negativo.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Buscar un negativo en blanco y negro.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><p>Reservado para uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica cuántos elementos se almacenan en el WIA_CATEGORY_FOLDER elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Activa o desactiva la luz del analizador.</p>
<p>Opcional para los WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM y se recomienda para WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Active la bombilla.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Apague la bombilla.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Establece el tiempo máximo para mantener la luz encendido cuando no se usa el analizador.</p>
<p>Opcional para los WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER y WIA_CATEGORY_FILM y se recomienda para WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_UI4</strong>, acceso: lectura/escritura, valores válidos: 0 - 0xFFF segundos</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) en la resolución actual. Puede ser el ancho del comensal de hoja o de la cómoda de análisis, según el tipo de elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) en la resolución actual. Este puede ser el alto del feeder de hoja o la cómoda de análisis, según el tipo de elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho mínimo, en milésimas de pulgada, que se examina en el eje horizontal (X) en la resolución actual.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto mínimo, en milésimas de pulgada, que se examina en el eje vertical (Y) en la resolución actual.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </dl></td>
<td ><p>Reservado para uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica horizontal. Resolución óptica horizontal más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones que puede generar el dispositivo. En su lugar, esta es la resolución de la óptica del dispositivo. El minidriver crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica vertical. Resolución óptica vertical más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones generadas por el dispositivo. En su lugar, esta es la resolución de la óptica del dispositivo. El minidriver crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </dl></td>
<td ><p>Especifica la orientación actual de los documentos que se examinarán. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación establece esta propiedad para definir la orientación original de una página o imagen que se va a adquirir. Para obtener información sobre cómo usar WIA_IPS_ORIENTATION, <strong>vea WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION hace referencia a la posición del documento que se va a examinar en la cámara del escáner o en el comensal. Es la orientación del documento en relación con la dirección del examen. WIA_IPS_ROTATION hace referencia a la rotación que se aplica a la imagen después de examinarla, justo antes de que la imagen se transfiera a la aplicación.
</blockquote>
</div>
<div>
 
</div>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las cuatro constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RETRATO</td>
<td>0 grados.</td>
</tr>
<tr class="even">
<td>PAISAJE</td>
<td>Rotación en el sentido contrario a las agujas del reloj de 90 grados, en relación con la orientación VERTICAL.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Rotación en el sentido contrario a las agujas del reloj de 180 grados, en relación con la orientación VERTICAL.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Rotación en el sentido contrario a las agujas del reloj de 270 grados, en relación con la orientación VERTICAL.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el tamaño de la página que está configurada actualmente para examinarse. Una aplicación establece esta propiedad para seleccionar las dimensiones de la página que se va a examinar. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Para ver las constantes que se pueden usar con esta propiedad, vea Constantes de tamaño de página <a href="-wia-wia2-pagesizeconstants.md"><strong>de WIA 2.0</strong></a>. Tenga en cuenta estos tamaños no fijos, en particular: </p>
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Definido por los valores de las propiedades <strong>WIA_IPS_PAGE_HEIGHT</strong> y <strong>WIA_IPS_PAGE_WIDTH</strong> propiedades.</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>El dispositivo determina automáticamente el tamaño de página.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Tamaño de página personalizado cuyas dimensiones ya conocen la aplicación y el controlador de dispositivo.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>El valor de la <strong>WIA_IPS_ORIENTATION</strong> determina la orientación de la página seleccionada actualmente. Las <strong>WIA_IPS_PAGE_WIDTH</strong> y <strong>WIA_IPS_PAGE_HEIGHT</strong> informe de las dimensiones de la página, en milésimas de pulgada. Estas propiedades deben estar de acuerdo con <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong>, que contienen las dimensiones de la página en píxeles.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Los valores válidos de tipo WIA_PROP_LIST dependen de la configuración válida de <strong>la WIA_IPS_ORIENTATION</strong> propiedad. Por ejemplo, si el dispositivo no puede examinar documentos orientados al entorno con una configuración de WIA_PAGE_A4, WIA_PAGE_A4 no es un valor válido para la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> cuando <strong>WIA_IPS_ORIENTATION</strong> está establecido en LANDSCAPE.
</blockquote>
</div>
<div>
 
</div>
<p>Si una aplicación establece <strong>WIA_IPS_PAGE_SIZE</strong> en cualquier valor distinto de los tres de la tabla anterior, el minidriver debe ajustar los valores de <strong>WIA_IPS_PAGE_WIDTH</strong> y <strong>WIA_IPS_PAGE_HEIGHT a</strong> las dimensiones de la página en milésimas de pulgada. También debe ajustar los valores de <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> a las dimensiones de la página en píxeles.</p>
<p>Si se cambia una configuración de extensión (<strong>WIA_IPS_XEXTENT</strong> <strong>o WIA_IPS_YEXTENT</strong>) a un valor que no coincide con la configuración de tamaño de página actual, el minidriver debe cambiar el valor de la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM. El minidriver también debe modificar <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> o <strong>WIA_IPS_PAGE_HEIGHT</strong> de acuerdo con la nueva configuración de extensión.</p>
<p>Si <strong>WIA_IPS_ORIENTATION</strong> se establece en LANDSCAPE, la configuración de extensión se intercambiará con respecto a sus valores habituales. Por ejemplo, si <strong></strong> una aplicación establece WIA_IPS_PAGE_SIZE en WIA_PAGE_A4, el minidriver establece <strong>WIA_IPS_PAGE_WIDTH</strong> en 11692 y <strong>WIA_IPS_PAGE_HEIGHT</strong> en 8267. (El minidriver también debe ajustar <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> en consecuencia).</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> se establece en WIA_PAGE_CUSTOM, el valor de orientación no se usa para determinar las dimensiones de extensión de la página que se va a examinar.
</blockquote>
</div>
<div>
 
</div>
<p>El minidriver es responsable de garantizar que la <strong>propiedad WIA_IPS_ORIENTATION</strong> esté de acuerdo con el área de selección actual. Si una aplicación cambia el valor de <strong>WIA_IPS_ORIENTATION a</strong> uno que no es válido para el tamaño de página seleccionado actualmente, el minidriver debe cambiar el valor de <strong>WIA_IPS_PAGE_SIZE</strong> a un tamaño de página compatible con el nuevo valor de orientación.</p>
<p>Si una aplicación establece la <strong>propiedad WIA_IPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM, el área de selección actual no se ve afectada. El minidriver wia debe obtener el diseño de imagen actual, empezando por la configuración actual de las <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> propiedades. Si la configuración de tamaño de página da como resultado un área de selección que está fuera de la cámara del analizador, el minidriver debe ajustar automáticamente los valores de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> a la configuración válida. Si las propiedades <strong>WIA_IPS_PAGE_SIZE</strong> <strong>y WIA_IPS_ORIENTATION</strong> se establecen al mismo tiempo y no son válidas cuando se aplican en combinación, el minidriver debe producir un error en la configuración de la aplicación devolviendo un error en <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvValidateItemProperties</a>.</p>
<p>Los cuatro ejemplos siguientes muestran diferentes <strong>WIA_IPS_PAGE_SIZE</strong> escenarios.</p>
<ol>
<li>El controlador notifica la configuración.</li>
<li>Una aplicación establece la <strong>WIA_IPS_PAGE_SIZE</strong> propiedad en WIA_PAGE_LETTER.</li>
<li>Una aplicación establece la <strong>WIA_IPS_ORIENTATION</strong> propiedad en LANDSCAPE.</li>
<li>Una aplicación cambia la <strong>propiedad WIA_IPS_XEXTENT</strong> a un valor más pequeño.</li>
</ol>
<p><strong>Ejemplo 1: el minidriver notifica la configuración</strong></p>
<p>En el ejemplo siguiente, el minidriver establece un área de selección personalizada antes de que una aplicación establece las propiedades de WIA. En este caso, el área de selección representa todo el plano.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Ejemplo 2: Una aplicación establece la propiedad</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>en WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Ejemplo 3: Una aplicación establece la</strong> <strong>WIA_IPS_ORIENTATION</strong>propiedad<strong>en LANDSCAPE</strong>  </p>
<p>La habitación física debe ser capaz de adquirir una página que estaba originalmente en orientación horizontal.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Ejemplo 4: Una aplicación cambia la propiedad</strong> <strong>WIA_IPS_XEXTENT</strong> a un valor <strong>más pequeño</strong></p>
<p>En el ejemplo siguiente, una aplicación cambia la <strong>WIA_IPS_XEXTENT</strong> propiedad a 1000. El minidriver debe suponer que el nuevo valor contenido en <strong>WIA_IPS_XEXTENT</strong> ya no es válido <strong></strong> para la propiedad <strong>WIA_IPS_PAGE_SIZE</strong> y, por tanto, debe cambiar WIA_IPS_PAGE_SIZE a WIA_PAGE_CUSTOM. El minidriver también debe <strong>ajustar</strong>WIA_IPS_PAGE_WIDTH .</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el alto, en milésimas de pulgada, de la página seleccionada actualmente. El minidriver crea y mantiene la <strong>WIA_IPS_PAGE_HEIGHT</strong> propiedad . Una aplicación lee esta propiedad para determinar las dimensiones físicas de la página que se está analizando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad notifica el alto de la página cuya propiedad <strong>WIA_IPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM (que es un valor de la <strong>propiedad WIA_IPS_PAGE_SIZE).</strong> <strong>WIA_IPS_PAGE_HEIGHT</strong> debe estar sincronizado con <strong>WIA_IPS_XEXTENT</strong>, que informa del alto, en píxeles, de la página que se va a examinar.</p>
<p>Esta propiedad es necesaria para WIA_CATEGORY_FEEDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el ancho de la página actual seleccionada, en milésimas de pulgada. Una aplicación lee esta propiedad para determinar las dimensiones físicas de la página que se está analizando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad notifica el ancho de la página cuya propiedad WIA_IPS_PAGE_SIZE <strong>está</strong> establecida en WIA_PAGE_CUSTOM. <strong>WIA_IPS_PAGE_WIDTH</strong> debe estar sincronizado con el valor de <strong>WIA_IPS_XEXTENT</strong>, que informa del ancho, en píxeles, de la página que se va a examinar. El minidriver crea y mantiene esta propiedad.</p>
<p>Esta propiedad es necesaria para WIA_CATEGORY_FEEDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el número actual de páginas que se adquirirán de un feeder de documentos automático. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores <a href="-wia-property-attributes.md">válidos: WIA_PROP_RANGE</a> es cero hasta el número máximo de páginas que el analizador puede examinar. El valor se ALL_PAGES (= 0) si el analizador puede examinar continuamente.</p>
<p>Una aplicación lee esta propiedad para determinar la capacidad de página del fuente de documentos. La aplicación también establece esta propiedad en el número de páginas que va a examinar.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si el modo dúplex está habilitado (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> se establece en FEEDER | DÚPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> igual al número de páginas que se examinarán.
</blockquote>
</div>
<div>
 
</div>
<p>Una hoja de papel contendrá automáticamente dos páginas si DUPLEX está habilitado, incluso si el lado posterior de la página está en blanco.</p>
<p>Si <strong>WIA_IPS_PAGES</strong> en 1, un analizador procesa un lado de la página. Se recomienda que, si un analizador no puede examinar solo un lado de una página en modo dúplex, cambie el valor <strong>de WIA_IPS_PAGES</strong> para el miembro Inc del miembro Range de la estructura WIA_PROPERTY_INFO a 2. Este valor indica a la aplicación que debe solicitar páginas en múltiplo de dos. Un valor de ALL_PAGES (= 0) <em></em> significa que se van a examinar todas las páginas que están cargadas actualmente en el feeder de documentos.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </dl></td>
<td ><p>Contiene la configuración actual para los píxeles blanco y negro. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee este valor para determinar el valor de WHITE o BLACK (en función de lo que haga la aplicación).</p>
<p>Necesario para todos los elementos almacenados o habilitados para la adquisición; Es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Si el dispositivo se puede establecer en un solo valor, cree un WIA_PROP_LIST y coloque el valor válido en él.</p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PHOTO_WHITE_0</td>
<td>WHITE es 0 y BLACK es 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>WHITE es 1 y BLACK es 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Indica el modo de vista previa de un dispositivo. Una aplicación establece esta propiedad para colocar el dispositivo en modo de vista previa.</p>
<p>Esta propiedad es necesaria para los elementos WIA_CATEGORY_FLATBED y WIA_CATEGORY_FILM, opcional para el WIA_CATEGORY_FEEDER elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>La aplicación realizará un examen final.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>La aplicación realizará un examen de vista previa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica si la imagen de vista previa existente se puede actualizar durante una vista previa de la imagen (en respuesta a un cambio en las WIA_IPA_DATATYPE o WIA_IPA_DEPTH propiedades).</p>
<p>Esta propiedad es opcional para todos los elementos habilitados para adquisición que admiten exámenes de versión preliminar; es decir, WIA_IPS_PREVIEW se admite con WIA_PREVIEW_SCAN. Esto incluye elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>Es posible actualizar la imagen existente.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>Se debe ejecutar otro examen de vista previa porque no es posible actualizar la imagen existente.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </dl></td>
<td ><p>Contiene la configuración de rotación actual, si se implementa. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación establece esta propiedad para informar al controlador de la cantidad (si en absoluto) que debe girar la imagen antes de que el controlador la devuelva a la aplicación.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION hace referencia a la posición del documento que se va a examinar en la cámara o el comensor del escáner. Es la orientación del documento en relación con la dirección del examen. WIA_IPS_ROTATION hace referencia a la rotación que se aplica a la imagen después de examinarla, justo antes de transferir la imagen a la aplicación.
</blockquote>
</div>
<div>
 
</div>
<p>El minidriver WIA es responsable de rotar los datos de imagen antes de enviarlos de vuelta a la aplicación. La aplicación es responsable de comprobar los encabezados de imagen para ver los valores recién girados.</p>
<p>Existe una confusión considerable sobre cómo resolver el efecto de la rotación en el área de selección de la imagen actual (que se define mediante las propiedades <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> <strong>y WIA_IPS_YEXTENT).</strong></p>
<p><em>El área de</em> selección hace referencia al área seleccionada en la cámara del escáner físico de la que se adquiere una imagen. <strong>WIA_IPS_ROTATION</strong> no modifica el área de selección. El controlador aplica una rotación en <strong></strong> sentido contrario a las agujas del WIA_IPS_ROTATION solo después de que el controlador haya adquirido el área de selección adecuada. <strong>WIA_IPS_ROTATION</strong> afecta a las dimensiones de la imagen de salida, por lo que estas dimensiones deben reflejarse en el encabezado de datos de la imagen resultante.</p>
<p>Opcional para todos los elementos habilitados para la adquisición; Es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Se definen las siguientes constantes de rotación.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RETRATO</td>
<td>El controlador no girará la imagen.</td>
</tr>
<tr class="even">
<td>PAISAJE</td>
<td>El controlador gira la imagen 90 grados en sentido contrario a las agujas del reloj.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>El controlador gira la imagen 180 grados en sentido contrario a las agujas del reloj.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>El controlador gira la imagen 270 grados en sentido contrario a las agujas del reloj.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica si la aplicación debe usar el filtro de segmentación del controlador para el examen de varias regiones. WIA_IPS_SEGMENTATION deben implementarse para los elementos WIA_CATEGORY_FLATBED y WIA_CATEGORY_FILM si admiten la creación de elementos secundarios con un filtro de segmentación o si el propio controlador crea elementos secundarios para marcos fijos.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>La aplicación debe usar el filtro de segmentación para el examen de varias regiones.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>El controlador crea los propios elementos secundarios para el examen en varias regiones. Este suele ser el caso si el analizador usa marcos fijos para este propósito.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Es posible que un controlador viene con un filtro de segmentación, pero todavía tiene WIA_IPS_SEGMENTATION establecido en WIA_DONT_USE_SEGMENTATION_FILTER para uno de sus elementos (por ejemplo, el elemento WIA_CATEGORY_FILM). Este podría ser el caso si el analizador usa marcos fijos para el examen de películas, pero no para el examen normal desde WIA_CATEGORY_FLATBED elementos.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o alineación y detección de borde, para los documentos que se colocan en la pantalla plana. El minidriver crea y mantiene esta propiedad. Esta propiedad indica cómo la hoja se coloca horizontalmente en la cabeza de examen de un escáner portátil o de hoja. La propiedad se usa para predecir dónde se coloca un documento a través de la cabeza del examen.</p>
<p>En el caso de los escáneres que admiten más de un responsable de examen, esta propiedad es relativa al más alto. Esta propiedad es obligatoria para escáneres de hoja, de desplazamiento y portátiles.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>La hoja se coloca a la izquierda con respecto a la cabeza de examen.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>La hoja se centra en la cabeza del examen.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>La hoja se coloca a la derecha con respecto a la cabeza de examen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Indica si un elemento necesita que se muestre al usuario un control de vista previa. El minidriver crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos habilitados para transferencia. Normalmente son solo elementos de las categorías WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM y WIA_CATEGORY_FINISHED_FILE.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Muestre un control de vista previa al usuario, ya que este dispositivo puede realizar una vista previa.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>No muestre un control de vista previa al usuario, porque este dispositivo no puede realizar una vista previa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica si la aplicación (o los filtros) pueden crear elementos secundarios en el elemento actual.</p>
<p>Opcional para todas las categorías de elementos habilitadas para transferencia: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e incluso WIA_CATEGORY_FOLDER. (Si el almacenamiento no admite la carga de nuevos elementos, esta propiedad debe ser no compatible o compatible con el <strong>valor FALSE).</strong></p>
<p>Los elementos que WIA_IPS_SEGMENTATION y WIA_USE_SEGMENTATION_FILTER también deben admitir WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION y establecerlo en <strong>TRUE.</strong></p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <strong>TRUE</strong> y <strong>FALSE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el valor de escala de grises que determina si un píxel se convertirá en blanco o negro cuando una imagen se convierta a monocromática. Los píxeles por encima del umbral se convierten en blanco. Los píxeles por debajo del umbral se convierten en blanco.</p>
<p>Esta propiedad es necesaria para los elementos de adquisición que admiten exámenes de 1 bpp y que tienen la propiedad WIA_IPA_DATATYPE establecida en WIA_DATA_THRESHOLD.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica si el controlador es capaz de transferir varios elementos secundarios en una sola llamada de transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>El único valor posible para esta propiedad es WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Si se establece esta marca, el controlador es capaz de transferir varios elementos secundarios en una sola llamada de transferencia. Si no se establece la marca, el servicio WIA recorrerá los elementos secundarios de forma recursiva y, a continuación, transferirá cada uno de esos elementos.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el número de bytes que se cargarán para el elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </dl></td>
<td ><p>Especifica el tiempo máximo de arranque, en milisegundos, que necesita el dispositivo antes de iniciar la operación de examen. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación puede leer esta propiedad para determinar el tiempo máximo de reserva para este dispositivo. A continuación, puede presentar un cuadro de diálogo esperando a que el dispositivo se ponga en marcha para que el usuario sepa que puede producirse una espera o pausa &quot; antes de que ocurra &quot; algo.</p>
<p>Esta propiedad es necesaria para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </dl></td>
<td ><p>Contiene el ancho actual, en píxeles, de la imagen seleccionada que se adquirirá. Una aplicación establece esta propiedad para marcar el ancho de un área de selección que se va a adquirir. Esta propiedad debe coincidir con la <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> propiedad . El minidriver crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; Es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </dl></td>
<td ><p>Contiene la coordenada x, en píxeles, de la esquina superior izquierda de la imagen seleccionada. Una aplicación establece esta propiedad para marcar la esquina superior izquierda del área de selección. El minidriver crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </dl></td>
<td ><p>Contiene la resolución horizontal actual, en píxeles por pulgada, para el dispositivo. Una aplicación establece esta propiedad para establecer la resolución horizontal. El minidriver crea y mantiene esta propiedad.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">tipo WIA_PROP_LIST</a> y coloque el valor válido en él. También es un caso en el que una configuración de resolución depende de otra resolución. (La resolución vertical puede depender de la resolución horizontal).</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Establece el escalado horizontal, como porcentaje, que se puede aplicar a las imágenes examinadas dentro del dispositivo del analizador o su controlador.</p>
<p>Esta propiedad es opcional para todos los elementos habilitados para la adquisición; es decir, elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</p>
<p>Los valores pueden estar entre 1 y VT_I4 (0xFFFF). Por ejemplo, 100 significa que no hay escalado, 050 significa reducir verticalmente hasta el 50 % del tamaño orignal y 200 significa escalar verticalmente hasta el 200 % del tamaño original.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </dl></td>
<td ><p>Contiene el alto actual, en píxeles, de la imagen seleccionada que se adquirirá. Una aplicación establece esta propiedad para marcar el alto de un área de selección. Esta propiedad debe estar de acuerdo con el valor de la <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> propiedad. El minidriver crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; Es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </dl></td>
<td ><p>Coordenada y actual, en píxeles, de la esquina superior izquierda de la imagen seleccionada. Una aplicación establece esta propiedad para marcar la esquina superior izquierda del área de selección. El minidriver crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </dl></td>
<td ><p>Contiene la resolución vertical actual, en píxeles por pulgada, para el dispositivo. Una aplicación establece esta propiedad para establecer la resolución vertical. El minidriver crea y mantiene esta propiedad.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">tipo WIA_PROP_LIST</a> y coloque el valor válido en él. También es un caso en el que una configuración de resolución depende de otra resolución. (La resolución horizontal puede depender de la resolución vertical).</p>
<p>Obligatorio para todos los elementos habilitados para la adquisición; es decir, elementos de las categorías: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE y WIA_CATEGORY_FILM. No se admite para WIA_CATEGORY_FOLDER elementos.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Establece el escalado vertical, como porcentaje, que se puede aplicar a las imágenes examinadas dentro del dispositivo del analizador o su controlador.</p>
<p>Esta propiedad es opcional para todos los elementos habilitados para la adquisición; es decir, elementos de tipos WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK y WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</p>
<p>Los valores pueden estar entre 1 y VT_I4 (0xFFFF). Por ejemplo, 100 significa que no hay escalado, 050 significa reducir verticalmente hasta el 50 % del tamaño orignal y 200 significa escalar verticalmente hasta el 200 % del tamaño original.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 





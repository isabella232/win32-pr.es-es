---
description: Todas las interfaces IWiaItem, IWiaItem2 e IWiaDrvItem Interface deben ser compatibles con las siguientes constantes de propiedad de dispositivo, a menos que se indique lo contrario en sus descripciones.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes comunes de propiedad de elemento de WIA (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 674f32294fafccc9a78f57125b919c230793a3e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623341"
---
# <a name="common-wia-item-property-constants"></a>Constantes comunes de propiedades de elementos WIA

Todas las interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) e [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) deben ser compatibles con las siguientes constantes de propiedad de dispositivo, a menos que se indique lo contrario en sus descripciones.

El prefijo "WIA IPA" indica una propiedad de elemento para todos los dispositivos y es la convención de nomenclatura \_ \_ usada en C/C++. Con fines de scripting, estas constantes usan el prefijo "Picture" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.



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
<td ><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td >Esta marca controla el acceso al elemento, así como si se elimina el elemento.<br/> Obligatorio para todos los elementos de WIA 2.0.<br/> Tipo: <strong>VT_I4</strong>; Solo lectura/escritura o solo lectura, en función de la capacidad del elemento para cambiar sus derechos de acceso; Valores válidos: WIA_PROP_FLAG<br/> La tabla siguiente tiene las cinco marcas que son válidas con esta propiedad.<br/> 
<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>El elemento tiene acceso de solo lectura.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>El elemento tiene acceso de solo escritura.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>El elemento tiene acceso de solo eliminación.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td ><p>Esta propiedad está reservada para su uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td ><p>Contiene el número de bits por canal de la imagen. El minidriver crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de imagen almacenados o habilitados para adquisición de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td ><p>Contiene el tamaño del búfer, en bytes, utilizado durante una transferencia de datos. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación puede leer esta propiedad para determinar el tamaño de búfer especificado por el controlador para las transferencias de datos. El servicio WIA también lee esta propiedad para asignar memoria para el minidriver durante la transferencia de datos.</p>
<p>Opcional para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
La <strong>WIA_IPA_BUFFER_SIZE</strong> contiene es la cantidad mínima de datos que una aplicación puede solicitar en un momento dado. Cuanto mayor sea el tamaño del búfer, mayores serán las solicitudes al dispositivo. Esto puede hacer que el dispositivo parezca lento y no responde, puede ralentizar el rendimiento general del sistema y puede consumir recursos excesivos. Los tamaños de búfer que son demasiado pequeños pueden ralentizar el rendimiento de la transferencia de datos al requerir muchas solicitudes más pequeñas. Elija un tamaño de búfer razonable teniendo en cuenta el tamaño típico de una solicitud de datos para el dispositivo y equilibrando el número de solicitudes con el tamaño de esas solicitudes.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td ><p>Contiene el número de bytes de una línea de examen de la imagen. El minidriver crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td ><p>Contiene el número de canales por píxel de la imagen. El minidriver crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de imagen almacenados o habilitados para adquisición de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td ><p>Esta propiedad está reservada para su uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td ><p>Contiene el tipo de compresión actual utilizado. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar el tipo de compresión de imagen o establece esta propiedad para configurar la configuración de compresión.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. El <strong>símbolo V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la <a href="-wia-iwiaitem2.md"><strong>interfaz IWiaItem2).</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Tipo de compresión</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Sin compresión. Vea <strong>Nota</strong> para obtener más información.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Modo de compresión automática. Vea <strong>Nota</strong> para obtener más información.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>Compresión RLE4</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>Compresión RLE8</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Compresión de grupo 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Compresión de grupo 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>Compresión JPEG.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>Compresión JBIG.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>Compresión JPEG 2000.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>Compresión PNG.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Cuando esta propiedad se WIA_COMPRESSION_NONE y WIA_IPA_FORMAT es WiaImgFmt_PDFA o WiaImgFmt_XPS; a WIA_COMPRESSION_NONE significa que el modo de compresión no está definido y el analizador debe decidir sobre un modo.</p>
<p>WIA_COMPRESSION_AUTO es un nuevo valor de propiedad definido para la WIA_IPA_COMPRESSION propiedad . Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos flatbed y feeder. Cuando este valor es compatible con el mini controlador WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_COMPRESSION para habilitar la detección automática del modo de compresión en el dispositivo. WIA_COMPRESSION_AUTO puede trabajar con y sin que el color automático completo sea compatible o habilitado (WIA_DATA_AUTO y WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO es más útil con formatos de archivo de transferencia que admiten varios tipos de datos y profundidades de bits, como WiaImgFmt_RAW. Para obtener más información sobre los formatos de archivo de transferencia, vea WIA_IPA_FORMAT en esta tabla.</p>
<p>Es opitonal que el mini driver de WIA suporte WIA_COMPRESSION_AUTO. Cuando se admite, el mini controlador WIA nunca debe establecerlo como el valor predeterminado para WIA_IPA_COMPRESSION; solo la aplicación WIA puede establecer este valor.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td ><p>Contiene la configuración del tipo de datos actual para el dispositivo. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar el tipo de datos de la imagen. Una aplicación escribe esta propiedad para establecer el tipo de datos actual de la imagen a punto de transferirse.</p>
<p>Esta propiedad es necesaria para todos los elementos de WIA 2.0. Debe ser de lectura y escritura para todos los elementos habilitados para la adquisición de WIA 2.0 y de solo lectura para los elementos de almacenamiento de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso para sistemas operativos Windows Vista: esta propiedad es de solo lectura para cámaras y lectura y escritura para escáneres. Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para elementos de WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y lectura y escritura para todas las demás categorías de elementos de WIA 2.0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las seis constantes que son válidas con <strong>cuando WIA_IPA_FORMAT</strong> no se establece en WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de datos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Válido para todos los elementos de origen de datos de imagen programables, incluidos flatbed y feeder. Cuando este valor es compatible con el mini driver de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DATATYPE para habilitar la detección automática de colores en el dispositivo. Cuando WIA_DATA_AUTO se establece, el mini driver de WIA debe actualizar WIA_IPA_DEPTH en el mismo elemento a WIA_DEPTH_AUTO (que debe ser un valor admitido si el dispositivo admite el color automático).<br/> Se trata de un valor opcional, pero es necesario cuando WIA_DEPTH_AUTO se admite para WIA_IPA_DEPTH.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Los datos de examen son de color rojo, verde, azul (RGB). El formato de color completo se describe mediante las siguientes propiedades de WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Igual que WIA_DATA_COLOR con la excepción de que los datos se difirieron mediante el patrón de dither seleccionado actualmente.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Igual que WIA_DATA_COLOR con la excepción de que el valor de umbral se usa al examinar los datos. Los valores de color <a href="https://msdn.microsoft.com/library/ms796233.aspx">sobre el WIA_IPS_THRESHOLD</a> se convierten al brillo completo; los colores de este valor se convierten en negro.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Los datos de examen se entrelacan mediante el patrón de dither seleccionado actualmente.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Los datos de examen representan la intensidad. La paleta es una escala de grises fija e igualmente espaciado con una profundidad especificada <a href="https://msdn.microsoft.com/library/ms795935.aspx">por WIA_IPA_DEPTH</a> propiedad.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>El umbral es de un bit por píxel de datos en blanco y negro. Los datos sobre el valor actual <a href="https://msdn.microsoft.com/library/ms796233.aspx">de WIA_IPS_THRESHOLD</a> se convierten en blanco; los datos de este valor se convierten en negro.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La <strong>WIA_IPA_DATATYPE</strong> propiedad también se usa para describir el tipo de transferencia de datos RAW que se usará cuando la aplicación WiaImgFmt_RAW. El controlador debe establecer la <strong>WIA_IPA_DATATYPE</strong> propiedad en una lista de valores permitidos de los que la aplicación puede elegir uno.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un tipo <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</p>
<p>Compruebe la <a href="https://msdn.microsoft.com/library/ms795935.aspx">propiedad WIA_IPA_DEPTH</a> para determinar la profundidad de bits. Esta propiedad normalmente contiene un valor único para las cámaras.</p>
<p>En la tabla siguiente se enumeran las constantes que son válidas <strong>con WIA_IPA_DATATYPE</strong> cuando <strong>WIA_IPA_FORMAT</strong> se establece en WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de datos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Los datos de examen representan la intensidad. La paleta es una escala de grises fija, igualmente espaciado con una profundidad especificada por <a href="https://msdn.microsoft.com/library/ms795935.aspx">la WIA_IPA_DEPTH</a> propiedad . <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Los datos de examen están en el espacio de colores BGR (azul-verde-rojo). El formato de color completo se describe con las siguientes propiedadesWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Los datos de digitalización se incluyen en el espacio de colores de color rojo-rojo (CMY). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Los datos de digitalización están en el espacio de colores de color de yellow-black ( YELLOW-black). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Los datos de examen están en el espacio de colores rojo-verde-azul (RGB). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Los datos de examen están en el espacio de colores de diferencia de diferencia de color (YUV) de luminosidad-azul. El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Los datos de examen están en el espacio de colores luminance-blue difference-red difference-black (YUVK). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td ><p>WIA_IPA_DEPTH contiene la configuración de profundidad de bits de una imagen. El minidriver crea y mantiene esta propiedad. Una aplicación lee esta propiedad para determinar la configuración de profundidad de bits de la imagen. La aplicación también puede establecer este valor en la profundidad de bits deseada.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">tipo WIA_PROP_LIST</a> y coloque el valor válido en él.</p>
<p>Esta propiedad es necesaria para todos los elementos de WIA 2.0. Debe ser de lectura y escritura para todos los elementos habilitados para la adquisición de WIA 2.0 y de solo lectura para los elementos de almacenamiento de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso para sistemas operativos Windows Vista: lectura y escritura; Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para los elementos WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y lectura y escritura para todas las demás categorías de elementos de WIA 2.0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO se define como 0 bits por píxel y es un nuevo valor de propiedad definido para el WIA_IPA_DEPTH. Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos flatbed y feeder. Cuando WIA_DEPTH_AUTO admite el mini driver de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DEPTH en este valor para habilitar la detección automática de colores en el dispositivo. Cuando WIA_DEPTH_AUTO se establece, el mini driver de WIA debe actualizar WIA_IPA_DATATYPE en el mismo elemento a WIA_DATA_AUTO (que debe ser un valor admitido, si el dispositivo admite el color automático).</p>
<p>WIA_DEPTH_AUTO es un valor opcional, pero es necesario cuando WIA_DATA_AUTO se admite para WIA_IPA_DATATYPE.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td ><p>Contiene la extensión de nombre de archivo para un formato de archivo determinado. El minidriver crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El controlador actualiza esta propiedad para reflejar el valor actual de <a href="https://msdn.microsoft.com/library/ms796440.aspx">la WIA_IPA_FORMAT</a> propiedad .</p>
<p>Por ejemplo, <strong>si WIA_IPA_FORMAT</strong> es WiaImgFmt_JPEG, WIA_IPA_FILENAME_EXTENSION <a href="-wia-property-attributes.md"></a> debe ser <strong>jpg</strong>. Si <strong>WIA_IPA_FORMAT</strong> es WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION debe ser BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
La extensión de nombre de archivo no incluye el punto.
</blockquote>
</div>
<div>
 
</div>
<p>Esta propiedad se recomienda para los controladores que admiten formatos estándar y es necesaria para los controladores que implementan formatos definidos de forma personalizada. Informa a la aplicación de la extensión de nombre de archivo correcta que se usará durante la transferencia de archivos con formato privado. Por ejemplo, si A. Datum Corporation creó un controlador WIA que transfirieron un archivo en un nuevo formato, la empresa podría especificar una extensión &quot; de adc &quot; . Esto permite a las aplicaciones transferir datos en ese formato a un archivo y crear un nombre de archivo como <em>myfile.adc</em>, lo que resulta útil para otros usuarios que comprenden la nueva extensión.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td ><p>Contiene el formato actual de la imagen que se va a transferir.</p>
<p>Una aplicación lee esta propiedad para determinar el formato de la imagen que está a punto de recibir. Una aplicación escribe esta propiedad para establecer el formato. Esta propiedad depende de la <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> propiedad. El minidriver crea y mantiene esta propiedad.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un tipo <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se enumeran las constantes que son válidas con esta propiedad. El asterisco * indica que la constante no se admite en Windows Vista. (Solo está disponible a través de la <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>interfaz IWiaItem).</strong></a> El asterisco doble ** indica que la constante no se admite en Windows Server 2003 o Windows Vista. El <strong>símbolo V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la <a href="-wia-iwiaitem2.md"><strong>interfaz IWiaItem2).</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>Formato de audio AIFF</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>Formato de audio MP3</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>Formato de audio WAV</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>Formato de audio WMA</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF**</td>
<td>Formato de vídeo de ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI**</td>
<td>Formato de vídeo AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Windows mapa de bits con un archivo de encabezado</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF*</td>
<td>Formato de archivo de imagen de cámara</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Formato de impresión DPOF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metarchivo Windows extensión</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Archivo ejecutable</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Formato de archivo intercambiable</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>Formato de imagen GIF</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>Formato HTML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows formato de archivo de icono de archivo</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Formato JBIG (Joint Bi-level Image Experts Group).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Formato comprimido JPEG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Formato comprimido JPEG 2000</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Formato comprimido JPEG 2000</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows mapa de bits sin un archivo de encabezado</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Formato PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG**</td>
<td>Formato de vídeo MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de archivo eastman-eastman</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Formato de archivo de Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG W3C</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Formato sin procesar solo para transferencias de datos</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Formato RGB sin formato</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Formato de archivo de texto enriquecido</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>Archivo de script</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Formato TIFF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>Archivo de texto</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>Codificación UNICODE de 16 bits</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows metarchivo</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>Archivo XML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Formato del paquete XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Cuando esta propiedad es WiaImgFmt_PDFA o WiaImgFmt_XPS y WIA_IPA_COMPRESSION se WIA_COMPRESSION_NONE; el último valor significa que el modo de compresión no está definido y el analizador debe decidir sobre un modo.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td ><p>Contiene el nombre completo del elemento (el nombre del elemento junto con la información de ruta de acceso). El nombre completo del elemento es el mismo que el parámetro <em>bstrFullItemName</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem.</a> Una aplicación lee esta propiedad para determinar qué elemento está usando actualmente y dónde se encuentra ese elemento en el árbol de elementos. Cada elemento debe tener un nombre único. Las aplicaciones usan normalmente el nombre completo del elemento para buscar elementos en el árbol de elementos. El servicio WIA crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td ><p>Esta propiedad está reservada para uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td ><p>Contiene el ICM de perfil que se necesita para descodificar correctamente la imagen. Una aplicación lee esta propiedad para determinar el perfil ICM que se va a usar al procesar la imagen. El servicio WIA crea y mantiene esta propiedad en función de la entrada ICMProfiles en el archivo de instalación del controlador.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td ><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Los elementos de WIA 2.0 se agrupan en categorías que definen cómo se va a tratar o usar un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2.</strong></a> Por ejemplo, si el elemento representa un feeder, la aplicación debe esperar que contenga las propiedades de fuente de documentos necesarias y funcione como un feeder de documentos. Si el elemento representa un archivo terminado, una aplicación WIA 2.0 debe tratarlo de ese modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo. (Las reglas de cada elemento se definirán en sus documentos de especificación individuales).</p>
<p>Obligatorio para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_CLSID</strong>, Acceso: Solo lectura, Valores <a href="-wia-wia2-itemcategoryguids.md"><strong>válidos: GUID de categoría de elemento</strong></a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td ><p>Contiene las marcas descriptivas para un elemento de WIA. Las marcas de elemento son las mismas que las del parámetro <em>lObjectFlags</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem.</a> El servicio WIA crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar los valores de marca descriptivos del elemento.</p>
<p>Tipo: <strong>VT_I4</strong> acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se tienen las marcas que son válidas con esta propiedad. Un asterisco * indica que la marca no se admite en Windows Vista o posterior. (Solo está disponible a través de la <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>interfaz IWiaItem).</strong></a> Un asterisco doble ** indica que la marca no se admite en Windows Server 2003 o Windows Vista o posterior. El <strong>símbolo V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la <a href="-wia-iwiaitem2.md"><strong>interfaz IWiaItem2).</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Marcar</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Este elemento admite el <strong>método IWiaItem::AnalyzeItem</strong> (descrito en la documentación de Platform SDK). Este elemento también admite la generación automática de elementos secundarios. Esta funcionalidad es útil para la detección de regiones o la descomposición de páginas.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Este elemento admite audio. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile.</strong></td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Solo para carpetas. Esta marca indica que las imágenes de esta carpeta se tomaron en una secuencia de tiempo continua.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Este elemento está marcado para su eliminación, este elemento se ha eliminado, este elemento no existe o el contenido de este elemento no es válido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Este elemento es un archivo de documento en uno de los formatos de documento que <strong>contiene WIA_IPA_FORMAT</strong> propiedad . (Estos formatos incluyen los de archivos que no son de imagen inicial, como .txt, .htm y .doc archivos).</td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>Este elemento representa un dispositivo conectado.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>Este elemento representa un dispositivo desconectado.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>El elemento admite transferencias de archivos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>El elemento es una carpeta.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>El elemento no está inicializado o se ha eliminado.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Este elemento lo ha generado una aplicación o el controlador.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Este elemento admite datos adjuntos y actualmente contiene datos adjuntos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanoram*</td>
<td>Este elemento representa una imagen horizontal de desplazamiento. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder.</strong></td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>El elemento es un archivo de imagen. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile.</strong></td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>El elemento es un origen de datos programable y sigue un conjunto de reglas de configuración predefinidas, que se basan en <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Este elemento es el elemento raíz, que es el elemento primario de todos los elementos de características que admite el dispositivo.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Esta marca indica almacenamiento adicional para los elementos de carpetas. Los controladores de WIA especifican sus elementos en términos de imágenes y carpetas. No existen propiedades de WIA que describan las características de un elemento de almacenamiento (como el espacio de almacenamiento restante, la velocidad de escritura o el tipo de medio). Se pueden agregar propiedades específicas del proveedor que exponen esta información. Estas propiedades solo son accesibles para las aplicaciones o extensiones que se escriben para reconocerlas.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Este elemento se puede usar para transferir datos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTopenCapabilityPassThrough</td>
<td>Este tipo indica que el dispositivo WIA es capaz de recibir datos de funcionalidad TWAIN de la capa de compatibilidad de TWAIN. Si se establece este tipo, cualquier funcionalidad TJDBC que no entienda la capa de compatibilidad de TJDBC se pasará al controlador de WIA. Esto solo es válido para el elemento raíz.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Este elemento admite el streaming de vídeo.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanoram*</td>
<td>Este elemento representa una imagen vertical vertical. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder.</strong></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Algunas de estas marcas son obligatorias u opcionales para los elementos de WIA 2.0, según la categoría del elemento, como se muestra en esta tabla.</p>

<table>
<thead>
<tr class="header">
<th>Categoría de elemento</th>
<th>Obligatorio</th>
<th>Opcionales</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (si se admiten varios elementos de regiones de examen, esta marca solo es opcional para el WIA_CATEGORY_FLATBED raíz).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (si WIA_CATEGORY_FEEDER_FRONT y WIA_CATEGORY_FEEDER_BACK están presentes, esta marca solo es opcional para el WIA_CATEGORY_FEEDER raíz).</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (raíz)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>None</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (secundarios)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>None</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td ><p>Contiene el nombre del elemento. Una aplicación lee esta propiedad para determinar qué elemento está usando actualmente. Cada elemento tiene un nombre único. El servicio WIA crea y mantiene esta propiedad.</p>
<p>Obligatorio para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td ><p>Contiene el tamaño actual, en bytes, de los datos asociados al elemento. El minidriver crea y mantiene esta propiedad.</p>
<p>Contains es el tamaño total de los datos que se transfieren. Si este valor es cero, significa que el minidriver no tiene información sobre el tamaño exacto de los datos. (Esto es común para los datos comprimidos). Una aplicación lee este valor para determinar el tamaño de la adquisición antes de que se lleve a cabo. El servicio WIA lee esta propiedad para ayudar a asignar memoria para las transferencias de datos. Para más información, consulte Transferencia de datos a una aplicación <a href="https://msdn.microsoft.com/library/ms792198.aspx">WIA</a> si la propiedad está establecida en cero y TYMED está configurado para una transferencia de archivos, el servicio WIA no asigna memoria para el minidriver WIA.</p>
<p>Se requiere para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td ><p>Contiene la hora a la que se capturó originalmente la imagen. El minidriver crea y mantiene esta propiedad. Esta propiedad debe informarse como un vector de ocho <strong>valores WORD</strong> en forma de una estructura SYSTEMTIME (descrita en la documentación del SDK de plataforma).</p>
<p>Opcional para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td ><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Especifica cuántos elementos se almacenan en el WIA_CATEGORY_FOLDER elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td ><p>Especifica el tamaño mínimo de búfer que se usa en las transferencias de datos. Si la transferencia de datos se realiza a través de un mecanismo de devolución de llamada, el valor de propiedad puede ser tan pequeño como 64 KB. Sin embargo, si la transferencia se va a archivo, el valor de propiedad es el número de bytes necesarios para transferir una página de datos a la vez. El minidriver crea y mantiene esta propiedad WIA.</p>
<p>Opcional para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td ><p>Contiene el número de líneas contenidas en la imagen (el alto vertical de la imagen en píxeles). El minidriver crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td ><p>Contiene el número de píxeles de cada línea de la imagen (el ancho de la imagen en píxeles). El minidriver crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td ><p>Esta propiedad no se admite en Windows Vista y versiones posteriores.</p>
<p>Contiene opciones de empaquetado de datos de imagen. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar las opciones de empaquetado de imágenes o establece las opciones de empaquetado de imágenes actuales.</p>
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
<td>WIA_PACKED_PIXEL</td>
<td>Los datos de imagen están en formato packed-pixel.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Los datos de imagen están en formato plano.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td ><p>Contiene el formato preferido para las imágenes que transfiere este minidriver. El minidriver crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td ><p>Especifica un CLSID que representa un conjunto de valores de propiedad de dispositivo. Si un controlador de dispositivo implementa esta característica, las aplicaciones usan esta propiedad para determinar si el dispositivo admite un conjunto de valores.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las 12 constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Mapa de bits de MicrosoftWindows con un archivo de encabezado</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metarchivo Windows extensión</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Formato de archivo intercambiable</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>Formato de imagen GIF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows de archivo de icono de archivo</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Formato comprimido JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de archivo EastmanIente</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG W3C</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows mapa de bits sin un archivo de encabezado</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Formato TIFF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows metarchivo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td ><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Contiene el número de bits de cada canal. Esta propiedad debe ser notificada como un vector de tantos valores BYTE como canales, donde el primer BYTE corresponde al número de bits del primer canal, el segundo byte al número de bits del segundo canal, y así sucesivamente. Debe haber tantas entradas como canales según la WIA_IPA_CHANNELS_PER_PIXEL. El controlador establece esa propiedad cuando la aplicación cambia a WiaImgFmt_RAW. Para los subtipos conocidos, hay tantas entradas como se muestran en la tabla en WIA_IPA_RAW_SUBTYPE.</p>
<p>Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td ><p>Esta propiedad está reservada para su uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td ><p>Especifica si se deben suprimir las páginas de propiedades generales de los elementos del dispositivo.</p>
<p>Esta propiedad está disponible en Windows XP y versiones posteriores.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. El asterisco * indica que la constante no es válida con Windows Vista y versiones posteriores. (Solo está disponible a través de la <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>interfaz IWiaItem).</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL*</td>
<td>Suprime la página de propiedades del elemento general para una cámara.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Suprime la página de propiedades del elemento general de un analizador.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td ><p>Esta propiedad contiene la configuración del método de transferencia. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar el método del minidriver de transferencia de datos.</p>
<p>Se requiere para todos los elementos de WIA 2.0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. El asterisco * indica constantes que no son válidas con Windows Vista y versiones posteriores. (Solo están disponibles a través de <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>la interfaz IWiaItem).</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Tipo de transferencia</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK*</td>
<td>Transferir una imagen a la memoria, en bandas.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK*</td>
<td>Transferir varias imágenes a la memoria, en bandas.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Transferir una imagen a un archivo.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Transferir una imagen a un archivo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td ><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Especifica el número de bytes que se cargarán para un elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 





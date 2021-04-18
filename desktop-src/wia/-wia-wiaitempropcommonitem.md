---
description: Las siguientes constantes de propiedad de dispositivo deben ser compatibles con todas las interfaces de interfaz IWiaItem, IWiaItem2 y IWiaDrvItem, a menos que se indique lo contrario en sus descripciones.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes de propiedad de elementos WIA comunes (Wiadef. h)
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
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705682"
---
# <a name="common-wia-item-property-constants"></a>Constantes comunes de propiedades de elementos WIA

Las siguientes constantes de propiedad de dispositivo deben ser compatibles con todas las interfaces de [interfaz](https://msdn.microsoft.com/library/ms793976.aspx) [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) y IWiaDrvItem, a menos que se indique lo contrario en sus descripciones.

El prefijo "WIA \_ IPA \_ " indica una propiedad de elemento para todos los dispositivos y es la Convención de nomenclatura que se usa en C/C++. Con fines de scripting, estas constantes usan el prefijo "Picture" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">Esta marca controla el acceso al elemento y si se elimina el elemento.<br/> Se requiere para todos los elementos de WIA 2,0.<br/> Tipo: <strong>VT_I4</strong>; Lectura/escritura o solo lectura, dependiendo de la capacidad del elemento de cambiar sus derechos de acceso; Valores válidos: WIA_PROP_FLAG<br/> En la tabla siguiente se muestran las cinco marcas que son válidas con esta propiedad.<br/> 
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
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el número de bits por canal para la imagen. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de imagen almacenados o habilitados para la adquisición de WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el tamaño del búfer, en bytes, que se utiliza durante una transferencia de datos. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación puede leer esta propiedad para determinar el tamaño de búfer especificado por el controlador para las transferencias de datos. El servicio WIA también lee esta propiedad para asignar memoria para el minicontrolador durante la transferencia de datos.</p>
<p>Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
La propiedad <strong>WIA_IPA_BUFFER_SIZE</strong> contiene la cantidad mínima de datos que una aplicación puede solicitar en un momento dado. Cuanto mayor sea el tamaño del búfer, mayores serán las solicitudes al dispositivo. Esto puede hacer que el dispositivo parezca lento y no responda, puede reducir el rendimiento general del sistema y puede consumir demasiados recursos. Los tamaños de búfer que son demasiado pequeños pueden reducir el rendimiento de la transferencia de datos al requerir muchas solicitudes más pequeñas. Elija un tamaño de búfer razonable teniendo en cuenta el tamaño típico de una solicitud de datos en el dispositivo y equilibre el número de solicitudes con respecto al tamaño de esas solicitudes.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el número de bytes en una línea de exploración de la imagen. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el número de canales por píxel de la imagen. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de imagen almacenados o habilitados para la adquisición de WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el tipo de compresión actual utilizado. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar el tipo de compresión de imagen o establece esta propiedad para establecer la configuración de compresión.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad. El símbolo <strong>V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</p>

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
<td>Sin compresión. Vea la <strong>Nota</strong> para obtener más información.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Modo de compresión automática. Vea la <strong>Nota</strong> para obtener más información.</td>
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
<p>Cuando se WIA_COMPRESSION_NONE esta propiedad y WIA_IPA_FORMAT es WiaImgFmt_PDFA o WiaImgFmt_XPS; a continuación, WIA_COMPRESSION_NONE significa que el modo de compresión es indefinido y el escáner debe decidir en un modo.</p>
<p>WIA_COMPRESSION_AUTO es un nuevo valor de propiedad definido para la propiedad WIA_IPA_COMPRESSION. Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador. Cuando este valor es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_COMPRESSION para habilitar la detección automática del modo de compresión en el dispositivo. WIA_COMPRESSION_AUTO puede trabajar con y sin que se admita o se habilite el color automático completo (WIA_DATA_AUTO y WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO es muy útil con formatos de archivo de transferencia que admiten varios tipos de datos y profundidades de bits, como WiaImgFmt_RAW. Para obtener más información acerca de los formatos de archivo de transferencia, consulte WIA_IPA_FORMAT en esta tabla.</p>
<p>Es opitonal que el mini-driver de WIA compatibilidad con WIA_COMPRESSION_AUTO. Cuando se admite, el mini controlador WIA nunca debe establecerlo como valor predeterminado para WIA_IPA_COMPRESSION; solo la aplicación WIA puede establecer este valor.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la configuración de tipo de datos actual para el dispositivo. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar el tipo de datos de la imagen. Una aplicación escribe esta propiedad para establecer el tipo de datos actual de la imagen que se va a transferir.</p>
<p>Esta propiedad es necesaria para todos los elementos de WIA 2,0. Debe ser de lectura y escritura para todos los elementos habilitados para adquisición de WIA 2,0 y solo lectura para los elementos de almacenamiento WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso para los sistemas operativos anteriores a Windows Vista: esta propiedad es de solo lectura para cámaras y lectura/escritura para escáneres; Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para los elementos de WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y de lectura y escritura para todas las demás categorías de elementos de WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se incluyen las seis constantes que son válidas con cuando <strong>WIA_IPA_FORMAT</strong> no se establece en WiaImgFmt_RAW.</p>

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
<td>Válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador. Cuando este valor es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DATATYPE para habilitar la detección automática de colores en el dispositivo. Cuando se establece WIA_DATA_AUTO, el controlador mini de WIA debe actualizar WIA_IPA_DEPTH en el mismo elemento para WIA_DEPTH_AUTO (que debe ser un valor compatible Si el dispositivo admite el color automático).<br/> Este es un valor opcional, pero es necesario cuando WIA_DEPTH_AUTO es compatible con WIA_IPA_DEPTH.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Los datos de digitalización son de color rojo, verde y azul (RGB). El formato de color completo se describe mediante las siguientes propiedades de WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Igual que WIA_DATA_COLOR con la diferencia de que los datos se han interpolado mediante el patrón de interpolación seleccionado actualmente.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Igual que WIA_DATA_COLOR, salvo que el valor de umbral se usa al examinar los datos. Los valores de color sobre el valor de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> se convierten al brillo completo; los colores que se encuentran debajo de este valor se convierten a negro.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Los datos de recorrido se comparan con el patrón de interpolación seleccionado actualmente.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Examinar datos representa la intensidad. La paleta es una escala de grises fija y equidistante con una profundidad especificada por <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propiedad.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>El umbral es un bit por píxel de datos en blanco y negro. Los datos sobre el valor actual de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> se convierten a blanco; los datos con este valor se convierten a negro.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La propiedad <strong>WIA_IPA_DATATYPE</strong> también se usa para describir el tipo de transferencia de datos sin procesar que se va a utilizar cuando la aplicación establece WiaImgFmt_RAW. El controlador debe establecer la propiedad <strong>WIA_IPA_DATATYPE</strong> en una lista de valores permitidos de los que la aplicación puede elegir uno.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</p>
<p>Compruebe la propiedad <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> para determinar la profundidad de bits. Esta propiedad normalmente contiene un valor único para las cámaras.</p>
<p>En la tabla siguiente se enumeran las constantes válidas con <strong>WIA_IPA_DATATYPE</strong> cuando <strong>WIA_IPA_FORMAT</strong> está establecido en WiaImgFmt_RAW.</p>

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
<td>Examinar datos representa la intensidad. La paleta es una escala de grises fija y equidistante con una profundidad especificada por la propiedad <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> . <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Los datos de recorrido están en el ColorSpace de BGR (Blue-Green-red). El formato de color completo se describe mediante followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Los datos de recorrido están en el ColorSpace cian-fucsia-amarillo (CMY). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Los datos de recorrido están en el ColorSpace cian-magenta-amarillo-negro (CMYK). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Los datos de recorrido están en el ColorSpace rojo-verde-azul (RGB). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Los datos de análisis están en el ColorSpace de luminancia: diferencia de azul: diferencia roja (YUV). El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Los datos de análisis están en la luminancia: diferencia de azul, diferencia de color rojo y negro (YUVK) ColorSpace. El formato de color completo se describe con las mismas propiedades de WIA que en WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> debe establecerse en 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH contiene el valor de profundidad de bits de una imagen. El minicontrolador crea y mantiene esta propiedad. Una aplicación Lee esta propiedad para determinar el valor de profundidad de bits de la imagen. Es posible que la aplicación también pueda establecer este valor en la profundidad de bits deseada.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo y coloque el valor válido en él.</p>
<p>Esta propiedad es necesaria para todos los elementos de WIA 2,0. Debe ser de lectura y escritura para todos los elementos habilitados para adquisición de WIA 2,0 y solo lectura para los elementos de almacenamiento WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso para los sistemas operativos anteriores a Windows Vista: lectura y escritura; Acceso para Windows Vista y versiones posteriores: esta propiedad es de solo lectura para los elementos de WIA_CATEGORY_FOLDER y WIA_CATEGORY_FINISHED_FILE, y de lectura y escritura para todas las demás categorías de elementos de WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO se define como 0 bits por píxel y es un nuevo valor de propiedad definido para la WIA_IPA_DEPTH. Este valor es válido para todos los elementos de origen de datos de imagen programables, incluidos el plano y el alimentador. Cuando WIA_DEPTH_AUTO es compatible con el controlador mini de WIA, el cliente de la aplicación WIA puede establecer WIA_IPA_DEPTH en este valor para habilitar la detección automática de colores en el dispositivo. Cuando se establece WIA_DEPTH_AUTO, el mini controlador WIA debe actualizar WIA_IPA_DATATYPE en el mismo elemento para WIA_DATA_AUTO (que debe ser un valor compatible, si el dispositivo admite el color automático).</p>
<p>WIA_DEPTH_AUTO es un valor opcional, pero se requiere cuando se admite WIA_DATA_AUTO para WIA_IPA_DATATYPE.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la extensión de nombre de archivo para un formato de archivo determinado. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El controlador actualiza esta propiedad para reflejar el valor actual de la propiedad <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</p>
<p>Por ejemplo, si se WiaImgFmt_JPEG <strong>WIA_IPA_FORMAT</strong> , <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> debe ser <strong>jpg</strong>. Si <strong>WIA_IPA_FORMAT</strong> es WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION debe ser BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
La extensión de nombre de archivo no incluye el punto.
</blockquote>
</div>
<div>
 
</div>
<p>Esta propiedad se recomienda para los controladores que admiten formatos estándar y es necesario para los controladores que implementan formatos definidos de forma personalizada. Informa a la aplicación de la extensión de nombre de archivo correcta que se va a usar durante la transferencia de archivos con formato privado. Por ejemplo, si A. Datum Corporation creó un controlador WIA que transfirió un archivo en un formato nuevo, la compañía podría especificar una extensión de &quot; ADC &quot; . Esto permite a las aplicaciones transferir datos en ese formato a un archivo y crear un nombre de archivo como, por ejemplo, <em>archivo. ADC</em>, que es útil para otras personas que entienden la nueva extensión.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el formato actual de la imagen que se va a transferir.</p>
<p>Una aplicación Lee esta propiedad para determinar el formato de la imagen que va a recibir. Una aplicación escribe esta propiedad para establecer el formato. Esta propiedad depende de la propiedad <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> . El minicontrolador crea y mantiene esta propiedad.</p>
<p>Si el dispositivo se puede establecer en un solo valor, cree un tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> y coloque el valor válido en él.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se enumeran las constantes que son válidas con esta propiedad. El asterisco * indica que la constante no es compatible con Windows Vista. (Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ). El doble asterisco * * indica que la constante no se admite en Windows Server 2003 o Windows Vista. El símbolo <strong>V</strong> indica que la constante solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</p>

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
<td>WiaImgFmt_ASF * *</td>
<td>Formato de vídeo ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>Formato de vídeo AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Mapa de bits de Windows con un archivo de encabezado</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>Formato de archivo de imagen de cámara</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Formato de impresión DPOF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metarchivo extendido de Windows</td>
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
<td>Formato de archivo de icono de Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>El formato Joint-LEVEL Experts Group (JBIG).</td>
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
<td>Mapa de bits de Windows sin un archivo de encabezado</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Formato PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>Formato de vídeo MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de archivo de Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Formato de archivo de Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG de W3C</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Formato RAW solo para transferencias de datos</td>
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
<td>Codificación Unicode de 16 bits</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Metarchivo de Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>Archivo XML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Formato de paquete XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Cuando esta propiedad es WiaImgFmt_PDFA o WiaImgFmt_XPS y WIA_IPA_COMPRESSION es WIA_COMPRESSION_NONE; después, el último valor significa que el modo de compresión es indefinido y el escáner debe decidir en un modo.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el nombre completo del elemento (el nombre del elemento junto con la información de la ruta de acceso). El nombre completo del elemento es el mismo que el parámetro <em>bstrFullItemName</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . Una aplicación Lee esta propiedad para determinar qué elemento está usando actualmente y dónde se encuentra ese elemento en el árbol de elementos. Cada elemento debe tener un nombre único. Normalmente, las aplicaciones usan el nombre completo del elemento para buscar elementos en el árbol de elementos. El servicio WIA crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad se reserva para uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el nombre del perfil ICM necesario para descodificar correctamente la imagen. Una aplicación Lee esta propiedad para determinar el perfil ICM que se va a utilizar al procesar la imagen. El servicio WIA crea y mantiene esta propiedad basada en la entrada ICMProfiles en el archivo de instalación del controlador.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Los elementos de WIA 2,0 se agrupan en categorías que definen cómo se trata o se usa un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> . Por ejemplo, si el elemento representa un alimentador, la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos. Si el elemento representa un archivo terminado, una aplicación WIA 2,0 debe tratarlo de este modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo. (Las reglas de cada elemento se definirán en sus documentos de especificación individuales).</p>
<p>Se requiere para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID de categoría de elemento</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>Contiene las marcas descriptivas de un elemento WIA. Las marcas de elemento son las mismas que las del parámetro <em>lObjectFlags</em> de la función de utilidad de servicio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . El servicio WIA crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar los valores de marca descriptivo del elemento.</p>
<p>Tipo: <strong>VT_I4</strong> acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se incluyen las marcas válidas con esta propiedad. Un asterisco * indica que la marca no es compatible con Windows Vista o posterior. (Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ). Un asterisco doble * * indica que la marca no se admite en Windows Server 2003 o Windows Vista o posterior. El símbolo <strong>V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores. (Solo está disponible a través de la interfaz <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> ).</p>

<table>
<thead>
<tr class="header">
<th>Marca</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Este elemento admite el método <strong>IWiaItem:: AnalyzeItem</strong> (descrito en la documentación de Platform SDK). Este elemento también admite la generación automática de elementos secundarios. Esta funcionalidad es útil para la detección de regiones o la descomposición de páginas.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Este elemento admite audio. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile</strong> .</td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Solo para carpetas. Esta marca indica que las imágenes de esta carpeta se realizaron en una secuencia de tiempo continua.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Este elemento está marcado para su eliminación, este elemento se ha eliminado, este elemento no existe o el contenido de este elemento no es válido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Este elemento es un archivo de documento en uno de los formatos de documento que contiene la propiedad <strong>WIA_IPA_FORMAT</strong> . (Estos formatos incluyen los de archivos que no son de imagen, como los archivos. txt,. htm y. doc).</td>
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
<td>El elemento admite las transferencias de archivos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>El elemento es una carpeta.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>El elemento no se ha inicializado o se ha eliminado.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Este elemento ha sido generado por una aplicación o por el controlador.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Este elemento admite datos adjuntos y actualmente contiene datos adjuntos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanorama*</td>
<td>Este elemento representa una imagen panorámica horizontal. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder</strong> .</td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>El elemento es un archivo de imagen. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFile</strong> .</td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>El elemento es un origen de datos programable y sigue un conjunto de reglas de configuración predefinidas, que se basan en <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Este elemento es el elemento raíz, que es el elemento primario de todos los elementos de característica que admite el dispositivo.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Esta marca indica almacenamiento adicional para elementos de carpeta. Los controladores WIA especifican sus elementos en términos de imágenes y carpetas. No existen propiedades de WIA que describen las características de un elemento de almacenamiento (por ejemplo, el espacio de almacenamiento restante, la velocidad de escritura o el tipo de medio). Se pueden agregar propiedades específicas del proveedor que exponen esta información. Estas propiedades solo son accesibles a las aplicaciones o extensiones que se escriben para reconocerlas.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Este elemento se puede usar para transferir datos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>Este tipo indica que el dispositivo WIA puede recibir datos de capacidad TWAIN del nivel de compatibilidad TWAIN. Si se establece este tipo, cualquier funcionalidad de TWAIN que no comprenda la capa de compatibilidad de TWAIN se pasará al controlador theWIA. Esto solo es válido para el elemento raíz.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Este elemento admite el streaming de vídeo.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanorama*</td>
<td>Este elemento representa una imagen panorámica vertical. Esta marca solo es válida para los elementos que también tienen establecida la marca <strong>WiaItemTypeFolder</strong> .</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Algunos de estos marcadores son obligatorios u opcionales para los elementos de WIA 2,0, de acuerdo con la categoría del elemento, como se muestra en esta tabla.</p>

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
<td>WiaItemTypeFolder (si se admiten varios elementos de regiones de análisis, esta marca solo es opcional para el elemento raíz WIA_CATEGORY_FLATBED).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (si los elementos WIA_CATEGORY_FEEDER_FRONT y WIA_CATEGORY_FEEDER_BACK están presentes, esta marca solo es opcional para el elemento raíz WIA_CATEGORY_FEEDER).</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (raíz)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>None</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (elementos secundarios)</td>
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
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el nombre del elemento. Una aplicación Lee esta propiedad para determinar qué elemento está usando actualmente. Cada elemento tiene un nombre único. El servicio WIA crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el tamaño actual, en bytes, de los datos asociados al elemento. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Contains es el tamaño total de los datos que se transfieren. Si este valor es cero, significa que el minicontrolador no tiene información sobre el tamaño exacto de los datos. (Esto es habitual para los datos comprimidos). Una aplicación Lee este valor para determinar el tamaño de la adquisición antes de que tenga lugar. El servicio WIA Lee esta propiedad para ayudar en la asignación de memoria para las transferencias de datos. Para obtener más información, consulte <a href="https://msdn.microsoft.com/library/ms792198.aspx">transferir datos a una aplicación WIA</a> si la propiedad se establece en cero y TYMED está configurado para una transferencia de archivos, el servicio WIA no asigna ninguna memoria para el minicontrolador WIA.</p>
<p>Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la hora en que se capturó originalmente la imagen. El minicontrolador crea y mantiene esta propiedad. Esta propiedad se debe notificar como vector de ocho valores de <strong>palabra</strong> en forma de estructura SYSTEMTIME (descrita en la documentación de Platform SDK).</p>
<p>Opcional para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> acceso: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Especifica el número de elementos que se almacenan en el elemento de WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el tamaño de búfer mínimo que se utiliza en las transferencias de datos. Si la transferencia de datos se realiza a través de un mecanismo de devolución de llamada, el valor de la propiedad puede ser tan pequeño como 64 KB. Sin embargo, si la transferencia es a archivo, el valor de la propiedad es el número de bytes que se necesitan para transferir una página de datos a la vez. El minicontrolador crea y mantiene esta propiedad de WIA.</p>
<p>Opcional para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el número de líneas contenidas en la imagen (el alto vertical de la imagen en píxeles). El minicontrolador crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el número de píxeles en cada línea de la imagen (el ancho de la imagen en píxeles). El minicontrolador crea y mantiene esta propiedad.</p>
<p>Opcional para todos los elementos de WIA 2,0.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad no se admite en Windows Vista y versiones posteriores.</p>
<p>Contiene opciones de empaquetado de datos de imagen. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar las opciones de empaquetado de imágenes o establece las opciones de empaquetado de imágenes actuales.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Si el dispositivo se puede establecer en un solo valor, cree un WIA_PROP_LIST tipo y coloque el valor válido en él.</p>
<p>En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</p>

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
<td>Los datos de la imagen están en formato de píxel empaquetado.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Los datos de la imagen están en formato plano.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el formato preferido para las imágenes que este minicontrolador transfiere. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>Especifica un CLSID que representa un conjunto de valores de propiedad del dispositivo. Si un controlador de dispositivo implementa esta característica, las aplicaciones usan esta propiedad para determinar si el dispositivo admite un conjunto de valores.</p>
<p>Tipo: <strong>CLSID</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se incluyen las 12 constantes que son válidas con esta propiedad.</p>

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
<td>Metarchivo extendido de Windows</td>
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
<td>Formato de archivo de icono de Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Formato comprimido JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato de archivo de Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG de W3C</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Mapa de bits de Windows sin un archivo de encabezado</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Formato TIFF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Metarchivo de Windows</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Contiene el número de bits de cada canal. Esta propiedad se debe presentar como un vector de tantos valores de BYTE como canales, donde el primer BYTE corresponde al número de bits del primer canal, el segundo byte al número de bits del segundo canal, etc. Debe haber tantas entradas como canales haya en función de WIA_IPA_CHANNELS_PER_PIXEL. El controlador establece esa propiedad cuando la aplicación cambia a WiaImgFmt_RAW. En el caso de los subtipos conocidos, hay tantas entradas como se muestran en la tabla en WIA_IPA_RAW_SUBTYPE.</p>
<p>Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad está reservada para un uso futuro y no se implementa en este momento.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>Especifica si se van a suprimir las páginas de propiedades generales de los elementos del dispositivo.</p>
<p>Esta propiedad está disponible en Windows XP y versiones posteriores.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad. El asterisco * indica que la constante no es válida con Windows Vista y versiones posteriores. (Solo está disponible a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ).</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>Suprime la página de propiedades general Item de una cámara.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Suprime la página de propiedades general Item de un escáner.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>Esta propiedad contiene la configuración del método de transferencia. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar el método del minicontrolador de transferencia de datos.</p>
<p>Se requiere para todos los elementos de WIA 2,0 habilitados para transferencia.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad. El asterisco * indica constantes que no son válidas con Windows Vista y versiones posteriores. (Solo están disponibles a través de la interfaz <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> ).</p>

<table>
<thead>
<tr class="header">
<th>Tipo de transferencia</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>Transferir una imagen a la memoria, en bandas.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
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
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Solo se admite en Windows Vista y versiones posteriores.</p>
<p>Especifica el número de bytes que se van a cargar para un elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 





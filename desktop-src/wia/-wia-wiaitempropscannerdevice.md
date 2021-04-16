---
description: Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propiedad del dispositivo Scanner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705680"
---
# <a name="scanner-device-property-constants"></a>Constantes de propiedades de dispositivo de escáner

Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows. Para obtener más información, consulte [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md). Las siguientes constantes de propiedades de dispositivo, con sus cadenas asociadas, son específicas de los escáneres de imágenes digitales.

El prefijo "WIA \_ DPS \_ " indica una propiedad de dispositivo para los dispositivos de escáner y es la Convención de nomenclatura que se usa en C/C++. Con el fin de crear scripts, estas constantes usan el prefijo "ScannerDevice" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Esta propiedad solo se admite en Windows Vista y versiones posteriores.
</blockquote>
<br/> Contiene un identificador único de instancia de función para un dispositivo de escáner de servicios Web. Este identificador representa el servicio Web en el dispositivo de escáner con el que se está comunicando el mini controlador WIA. No se deben realizar suposiciones sobre el formato de este identificador. El controlador mini de WIA crea y mantiene esta propiedad. <br/> Las aplicaciones WIA pueden usar el valor de WIA_DPS_DEVICE_ID para buscar, mediante la API de detección de funciones, el objeto de instancia de función que representa el dispositivo de analizador de servicios web usado en la sesión de WIA 2,0 actual.<br/> Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">Reservado, no usar.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">Reservado, no usar.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td style="text-align: left;">Contiene las capacidades del escáner. El minicontrolador crea y mantiene esta propiedad. <br/> Una aplicación Lee esta propiedad para determinar si el escáner tiene un alimentador plano, un alimentador de documentos o un dúplex instalado. Esta propiedad también se usa para definir aún más las características instaladas.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> En la tabla siguiente se describen las constantes que solo son válidas con Windows 7.<br/> 
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>El escáner tiene instalado un controlador de documentos automático.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas solo con Windows 7 y Windows Vista.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>El dispositivo admite la configuración avanzada de examen dúplex. Use WIA_IPS_DUPLEX_SETTINGS para cambiar entre el uso de configuraciones de dúplex básica y avanzada.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>El escáner puede detectar cuándo está listo para digitalizar el adaptador de película o transparencia.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>El analizador puede detectar cuándo hay documentos en el almacenamiento interno.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>El escáner está equipado con un adaptador de exploración de película o transparencia.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>El escáner está equipado con un dispositivo de almacenamiento de imágenes interno.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas con Windows XP o posterior.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>El escáner puede detectar un documento en el alimentador.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>El escáner puede detectar un documento en la placa de escáner.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>El escáner solo puede detectar un documento en el alimentador mediante el análisis.</td>
</tr>
<tr class="even">
<td>DUPLICA</td>
<td>El escáner tiene un dúplex.</td>
</tr>
<tr class="odd">
<td>FEED</td>
<td>El escáner tiene instalado un controlador de documentos automático.</td>
</tr>
<tr class="even">
<td>PISO</td>
<td>El escáner tiene una placa plana.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas solo con Windows XP. Estos valores están en desuso para Windows 7 y Windows Vista, y no deben usarse.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>El analizador puede detectar una solicitud de examen dúplex del usuario.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>El escáner puede indicar cuándo está instalado el dúplex.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>El escáner puede indicar cuándo está instalado el alimentador de documentos automático.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite en Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el origen y el modo de adquisición del detector actual. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar el origen de adquisición actual del escáner o para escribir esta propiedad para establecer el origen y el modo del escáner. Además, las aplicaciones usan esta propiedad para habilitar y deshabilitar la funcionalidad de dúplex.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>En la tabla siguiente se incluyen las diez constantes válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ALIMENTADOR</td>
<td>Digitalice con el alimentador de documentos.</td>
</tr>
<tr class="even">
<td>PLATAFORMA</td>
<td>Digitalice con el escáner plano.</td>
</tr>
<tr class="odd">
<td>D</td>
<td>Digitalice mediante operaciones de dúplex.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Habilita la alimentación automática del documento siguiente después de un examen.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Busque primero el principio del documento. Este valor es válido cuando se establece dúplex.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Digitalice primero la parte posterior del documento. Este valor es válido cuando se establece dúplex.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Examinar solo la parte frontal. Este valor es válido cuando se establece dúplex.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Examinar solo la copia. Este valor es válido cuando se establece dúplex.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Examinar la página siguiente del documento.</td>
</tr>
<tr class="even">
<td>Alimentación prefuente</td>
<td>Habilita el modo de fuente previa. Coloca el siguiente documento antes de la búsqueda.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el estado actual del escáner plano, el alimentador de documentos o el dúplex instalado del escáner. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación Lee esta propiedad para determinar si el dispositivo de escáner está listo para usarse. Esta es una manera ideal de comprobar si el papel está en el alimentador antes de adquirir una imagen.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se incluyen las constantes que son válidas con esta propiedad. Un asterisco * indica que la marca no es compatible con Windows Vista o posterior. El símbolo <strong>V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores. </p>
<table>
<thead>
<tr class="header">
<th>Marcas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>El plano está listo para su uso.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>El escáner tiene un documento en la placa de escáner.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>El dúplex está habilitado y listo para usarse.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>La cubierta plana está activa.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>La ruta de papel está actualizada y impide el funcionamiento correcto.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Se atasca un documento en el alimentador de documentos.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>El adaptador de transparencia está instalado y listo para su uso.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>El dispositivo de almacenamiento interno está listo.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>El almacenamiento está lleno, no se pueden realizar operaciones de carga.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Se produjo una condición de fuente múltiple (normalmente con una PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Hay un error que requiere la intervención del usuario en el dispositivo.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>El escáner no está listo debido a un problema de luz.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td style="text-align: left;"><p>Contiene todos los caracteres válidos que una aplicación puede utilizar para crear cadenas de aprobador válidas. Un aprobador es una impresora instalada en un escáner que imprime un mensaje de texto en cada página examinada. El minicontrolador debe validar el valor de la propiedad <strong>WIA_DPS_ENDORSER_STRING</strong> con el juego de caracteres válido en esta propiedad. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td style="text-align: left;"><p>Contiene una cadena que se va a aprobar (en otras palabras, impresa) en cada página que el minicontrolador explora. Una aplicación establece esta propiedad utilizando el juego de caracteres válido que se muestra en la propiedad <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> . El minicontrolador debe aprobar los documentos solo si se establece una cadena en esta propiedad. Una cadena vacía significa que la funcionalidad del aprobador está deshabilitada.</p>
<p>Dado que es responsabilidad del controlador interpretar la cadena del aprobador, el controlador puede usar caracteres especiales en <strong>WIA_DPS_ENDORSER_STRING</strong>. Sin embargo, solo las aplicaciones entienden estos caracteres.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Un controlador que admita la propiedad <strong>WIA_DPS_ENDORSER_STRING</strong> debe admitir la siguiente lista de tokens. </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>La fecha en el formato AAAA/MM/DD.</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>El día del formulario DD.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>Mes del año en el formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>Número de páginas transferidas.</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>La hora del día con el formato HH: MM: SS.</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>El año del formulario YYYY.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo se admite en Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la dirección SOAP de un dispositivo de analizador de servicios Web. El controlador mini de WIA 2,0 crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o la alineación horizontal, de los documentos colocados en el plano. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</p>

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
<td>El papel está justificado a la izquierda.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>El papel está centrado.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>El papel está justificado a la derecha.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho máximo, en milésimas de pulgada, que se analiza en el eje horizontal (X) de la placa de un escáner plano en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que mueven las hojas a la placa de un escáner plano para su digitalización. Esta propiedad es obligatoria para los escáneres que tienen una placa. En su lugar, otros tipos de escáner implementarán la propiedad <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) de un escáner de alimentación de mano o de papel en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que examinan sin mover hojas a la plancha de un escáner plano. Esta propiedad es obligatoria para los escáneres de alimentación de hojas, de avance y de alimentación.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td style="text-align: left;"><p>Contiene el tiempo máximo para examinar una sola página con la configuración de propiedades actual, en milisegundos. Una aplicación Lee esta propiedad para estimar el tiempo que se tardará en digitalizar una página. Esto resulta útil a la hora de determinar las condiciones de un dispositivo que ha dejado de responder. El minicontrolador crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los escáneres.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene las dimensiones horizontales físicas de la página más pequeña que el alimentador de documentos del escáner puede escanear, en milésimas de pulgada. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene las dimensiones físicas verticales de la página más pequeña que el alimentador de documentos del escáner puede escanear, en milésimas de pulgada. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica horizontal. Resolución óptica horizontal más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones que puede generar el dispositivo. En su lugar, se trata de la resolución de los medios ópticos del dispositivo. El minicontrolador crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los escáneres.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica vertical. Resolución óptica vertical más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones que genera el dispositivo. En su lugar, se trata de la resolución de los medios ópticos del dispositivo. El minicontrolador crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los escáneres.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la configuración de orientación actual. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Una aplicación establece la propiedad <strong>WIA_DPS_ORIENTATION</strong> para definir la orientación original de una página o imagen que se va a adquirir. Para obtener información sobre cómo usar WIA_DPS_ORIENTATION, vea <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las cuatro constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>La DEFINT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HORIZ</td>
<td>rotación de 90 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</td>
</tr>
<tr class="even">
<td>VERTICAL</td>
<td>0 grados.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>rotación de 180 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>rotación de 270 grados en el sentido contrario a las agujas del reloj, en relación con la orientación vertical.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vea también</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td style="text-align: left;"><p>Color que se usa para rellenar cuando no hay suficientes datos de imagen para rellenar un búfer solicitado. Esta propiedad se implementa para los escáneres que rellenan el búfer. Esta propiedad es opcional para todos los escáneres. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El formato de la información de color es <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el alto, en milésimas de pulgada, de la página seleccionada actualmente. El minicontrolador crea y mantiene la propiedad <strong>WIA_DPS_PAGE_HEIGHT</strong> . Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del alto de la página cuya propiedad <strong>WIA_DPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM (que es un valor de la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> ). <strong>WIA_DPS_PAGE_HEIGHT</strong> debe estar sincronizada con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que indica el alto, en píxeles, de la página que se va a examinar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el tamaño de la página seleccionada actualmente para su examen. Para seleccionar las dimensiones de la página que se va a examinar, una aplicación establece esta propiedad. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (orientación vertical)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definido por los valores de las propiedades <strong>WIA_DPS_PAGE_HEIGHT</strong> y <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientación vertical)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>El valor de la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina la orientación de la página seleccionada actualmente. Las propiedades <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT</strong> notifican las dimensiones de la página, en milésimas de pulgada. Tenga en cuenta que estas propiedades deben estar en acuerdo con <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong>, que contienen las dimensiones de la página en píxeles. Los valores válidos de tipo WIA_PROP_LIST deben depender de valores válidos de la propiedad <strong>WIA_IPS_ORIENTATION</strong> . Si el dispositivo no puede examinar documentos orientados horizontalmente con un valor de WIA_PAGE_A4, WIA_PAGE_A4 no debe aparecer en la lista de valores válidos para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> cuando <strong>WIA_IPS_ORIENTATION</strong> está establecida en LANSCAPE.</p>
<p>Si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en cualquier valor distinto de WIA_PAGE_CUSTOM, el minicontrolador debe ajustar los valores de <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT</strong> a las dimensiones de la página en milésimas de pulgada. También debe ajustar los valores de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> y <strong>WIA_IPS_YEXTENT</strong> a las dimensiones de la página en píxeles.</p>
<p>Si una configuración de extensión (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> o <strong>WIA_IPS_YEXTENT</strong>) se cambia a un valor que no coincide con la configuración de tamaño de página actual, el minicontrolador debe cambiar el valor de la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM. El minicontrolador también debe modificar <strong>WIA_DPS_PAGE_WIDTH</strong> o <strong>WIA_DPS_PAGE_HEIGHT</strong> de acuerdo con la nueva configuración de extensión.</p>
<p>Si <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> se establece en LANSCAPE, se volteará la configuración de la extensión &quot; . &quot; Por ejemplo, si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_A4, el minicontrolador debe establecer <strong>WIA_DPS_PAGE_WIDTH</strong> en 11692 y <strong>WIA_DPS_PAGE_HEIGHT</strong> en 8267. (El minicontrolador también debe establecer <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> en consecuencia). Tenga en cuenta que si <strong>WIA_DPS_PAGE_SIZE</strong> está establecido en WIA_PAGE_CUSTOM, el valor de orientación no se utiliza para determinar las dimensiones de extensión de la página que se va a examinar.</p>
<p>El minicontrolador es responsable de garantizar que la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> está en acuerdo con el área de selección actual. Si una aplicación cambia el valor de <strong>WIA_IPS_ORIENTATION</strong> a uno que no es válido para el tamaño de página seleccionado actualmente, el minicontrolador debe cambiar el valor de <strong>WIA_DPS_PAGE_SIZE</strong> a un tamaño de página compatible con el nuevo valor de orientación.</p>
<p>Si una aplicación establece la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM, el área de selección actual no se ve afectada. El minicontrolador WIA debe obtener el diseño de la imagen actual, a partir de la configuración actual de las propiedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> y <strong>WIA_IPS_YPOS</strong> . Si la configuración de tamaño de página da como resultado un área de selección que está fuera de la cama del escáner, el minicontrolador debe ajustar automáticamente los valores de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> a valores válidos. Si las propiedades <strong>WIA_DPS_PAGE_SIZE</strong> y <strong>WIA_IPS_ORIENTATION</strong> se establecen al mismo tiempo y no son válidas cuando se aplican en combinación, el minicontrolador debe generar un error en la configuración de la aplicación devolviendo un error en <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>. .</p>
<p>En los cuatro ejemplos siguientes se muestran distintos escenarios de <strong>WIA_DPS_PAGE_SIZE</strong> .</p>
<ol>
<li>El controlador informa de la configuración.</li>
<li>Una aplicación establece la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_LETTER.</li>
<li>Una aplicación establece la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> en LANSCAPE.</li>
<li>Una aplicación cambia la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> a un valor menor.</li>
</ol>
<p><strong>Ejemplo 1: el minicontrolador informa de la configuración</strong></p>
<p>En el ejemplo siguiente, el minicontrolador establece un área de selección personalizada antes de que una aplicación establezca las propiedades de WIA. En este caso, el área de selección representa todo el plano.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><strong>Ejemplo 2: una aplicación establece la</strong> <strong></strong><strong>propiedad WIA_DPS_PAGE_SIZE en WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><strong>Ejemplo 3: una aplicación establece la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propiedad WIA_IPS_ORIENTATION en LANSCAPE</strong>  </p>
<p>La cama física debe ser capaz de adquirir una página que estaba originalmente en orientación horizontal.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><strong>Ejemplo 4: una aplicación cambia la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propiedad WIA_IPS_XEXTENT a un valor más pequeño</strong>  </p>
<p>En el ejemplo siguiente, una aplicación cambia la propiedad <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> a 1000. El minicontrolador debe asumir que el nuevo valor incluido en <strong>WIA_IPS_XEXTENT</strong> ya no es válido para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> y, por tanto, debe cambiar <strong>WIA_DPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM. El minicontrolador también debe ajustar <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el ancho de la página actual seleccionada, en milésimas de pulgada. Una aplicación Lee esta propiedad para determinar las dimensiones físicas de la página que se está examinando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad informa del ancho de la página cuya propiedad <strong>WIA_DPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> debe estar sincronizado con el valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que notifica el ancho, en píxeles, de la página que se va a examinar. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el número actual de páginas que se van a adquirir de un alimentador de documentos automático. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (cero a través del número máximo de páginas que puede contener el alimentador de documentos)</p>
<p>Una aplicación Lee esta propiedad para determinar la capacidad de página del alimentador de documentos. La aplicación también establece esta propiedad en el número de páginas que va a examinar.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si el modo dúplex está habilitado (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> está establecido en alimentador | DÚPLEX), <strong>WIA_DPS_PAGES</strong> sigue siendo igual al número de páginas que se van a examinar.
</blockquote>
</div>
<div>
 
</div>
<p>Una hoja de papel contendrá automáticamente dos páginas si está habilitada la opción dúplex, incluso si la parte posterior de la página está en blanco.</p>
<p>Al establecer <strong>WIA_DPS_PAGES</strong> en 1, un escáner procesa uno de los lados de la página. Se recomienda que, si un escáner no puede examinar solo un lado de una página en modo dúplex, el <strong>WIA_DPS_PAGES</strong> valor válido para el miembro Inc de la estructura WIA_PROPERTY_INFO debe cambiarse a 2. Este valor indica a la aplicación que debe solicitar páginas en múltiplos de dos. Un valor de cero significa que <em>todas</em> las páginas que están cargadas actualmente en el alimentador de documentos se van a examinar.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el color de la plancha en la parte posterior de la hoja que se va a examinar. Esta propiedad es opcional para los escáneres que tienen una placa. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El formato de la información de color es <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica el modo de vista previa de un dispositivo. Una aplicación establece esta propiedad para colocar el dispositivo en modo de vista previa.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las dos constantes válidas con esta propiedad. </p>
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
<td>La aplicación realizará un análisis final.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>La aplicación realizará un examen de vista previa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td style="text-align: left;"><p>Contiene un valor que indica si el analizador almacenará en caché las páginas en un búfer del escáner antes de enviarlas a la aplicación.</p>
<p>Un valor de cero deshabilita el examen hacia tarde y no se recorren las páginas. Al realizar transferencias de datos normales en el elemento de examen previo almacenado en búfer, se recuperan las páginas almacenadas en búfer. No se pueden cambiar las propiedades de WIA durante una operación de exploración. Esta propiedad es opcional.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de cero al número máximo de páginas que puede contener el alimentador de documentos.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows 7 y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Indica el origen de entrada (plano, alimentador de documentos automático o adaptador de digitalización de fil) del que se va a realizar el análisis, o la ubicación de almacenamiento desde la que se van a transferir los datos.</p>
<p>Un evento de examen notifica a la aplicación que el usuario ha iniciado un examen, pero el evento no proporciona el nombre del elemento WIA que representa el origen de entrada. El controlador de eventos de la aplicación puede consultar la propiedad WIA_DPS_SCAN_AVAILABLE_ITEM del elemento raíz para obtener el nombre del elemento de origen de entrada.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de cero al número máximo de páginas que puede contener el alimentador de documentos.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el identificador de servicio de un dispositivo de escáner de servicios Web. El controlador mini de WIA 2,0 crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, la alineación y la detección de bordes, para los documentos que se colocan en el plano. El minicontrolador crea y mantiene esta propiedad. Esta propiedad indica cómo se coloca horizontalmente la hoja en el encabezado de digitalización de un escáner de mano o de alimentación de hojas. La propiedad se usa para predecir dónde se coloca un documento en el encabezado del examen.</p>
<p>En el caso de los escáneres que admiten más de un encabezado de examen, esta propiedad es relativa al encabezado de examen superior. Esta propiedad es obligatoria para los escáneres de alimentación de hojas, de desplazamiento y de mano.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</p>

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
<td>La hoja se coloca a la izquierda con respecto al encabezado de digitalización.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>La hoja está centrada en el encabezado de la digitalización.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>La hoja se coloca a la derecha con respecto al encabezado de digitalización.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica si un elemento necesita un control de vista previa para el usuario. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se muestran las dos constantes válidas con esta propiedad. </p>
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
<td>Mostrar un control de vista previa al usuario, ya que este dispositivo puede realizar una vista previa.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>No muestre un control de vista previa al usuario, ya que este dispositivo no puede realizar una vista previa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Lo usa el servicio WIA para informar al controlador de la cuenta de usuario sobre el nombre de la cuenta de usuario (incluido el nombre de dominio de red cuando proceda) de la sesión en la que se está ejecutando la aplicación WIA actual.</p>
<p>Se trata de una propiedad de elemento raíz, administrada por el servicio WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o la alineación vertical y la detección de bordes, para los documentos colocados en el plano. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>El papel está justificado en la parte superior.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>El papel está centrado.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>El papel está justificado en la parte inferior.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vea también</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) de la placa de un escáner plano en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos, que mueven las hojas a la placa de un escáner plano para su digitalización. Esta propiedad es obligatoria para los escáneres que tienen una placa. En su lugar, otros tipos de escáner implementarán la propiedad <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) de un escáner de alimentación de mano o de papel en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que examinan sin mover hojas a la plancha de un escáner plano. Esta propiedad es obligatoria para los escáneres alimentados por hojas. Los escáneres de avance y de alimentación manual no deben implementar esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 

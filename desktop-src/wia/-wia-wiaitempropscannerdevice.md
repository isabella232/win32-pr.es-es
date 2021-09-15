---
description: Windows Los dispositivos de hardware de adquisición de imágenes (WIA) tienen valores de propiedad que se almacenan en Windows registro.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propiedad del dispositivo del analizador (Wiadef.h)
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
ms.openlocfilehash: d9e7afee9b5b639c21e52dc797e7ad42a6ee0dd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467343"
---
# <a name="scanner-device-property-constants"></a>Constantes de propiedad del dispositivo del analizador

Windows Los dispositivos de hardware de adquisición de imágenes (WIA) tienen valores de propiedad que se almacenan en Windows registro. Para obtener más información, [**vea Constantes comunes de propiedades de dispositivo.**](-wia-wiaitempropcommondevice.md) Las siguientes constantes de propiedad de dispositivo, con sus cadenas asociadas, son específicas de los escáneres de imágenes digitales.

El prefijo "WIA DPS" indica una propiedad de dispositivo para dispositivos scanner y es la convención de nomenclatura \_ \_ usada en C/C++. Con fines de scripting, estas constantes usan el prefijo "ScannerDevice" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.



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
<td ><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
Esta propiedad solo se admite en Windows Vista y versiones posteriores.
</blockquote>
<br/> Contiene un identificador de instancia de función único para un dispositivo de analizador de servicios web. Este identificador representa el servicio web en el dispositivo del analizador con el que se comunica el mini controlador WIA. No se debe realizar ninguna suposición sobre la forma de este identificador. El mini controlador WIA crea y mantiene esta propiedad. <br/> Las aplicaciones WIA pueden usar el valor de WIA_DPS_DEVICE_ID para buscar, mediante la API de detección de funciones, el objeto de instancia de función que representa el dispositivo de analizador de servicios web usado en la sesión actual de WIA 2.0.<br/> Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td >Reservado, no use.<br/> Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td >Reservado, no use.<br/> Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td >Contiene las funcionalidades del analizador. El minidriver crea y mantiene esta propiedad. <br/> Una aplicación lee esta propiedad para determinar si el analizador tiene instalado un dúplex, un fuente de documentos o una fuente de distribución de documentos planas. Esta propiedad también se usa para definir aún más las características instaladas.<br/> Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> En la tabla siguiente se describen las constantes que son válidas solo Windows 7.<br/> 
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
<td>El analizador tiene instalado un controlador de documentos automático.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas con Windows 7 y Windows Vista.</p>
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
<td>El dispositivo admite la configuración avanzada de examen dúplex. Use WIA_IPS_DUPLEX_SETTINGS para cambiar entre el uso de configuraciones dúplex básicas y avanzadas.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>El analizador puede detectar cuándo el adaptador de transparencia o película está listo para examinarse.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>El analizador puede detectar cuándo hay documentos en el almacenamiento interno.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>El escáner está equipado con un adaptador de digitalización de transparencia o película.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>El analizador está equipado con un dispositivo de almacenamiento de imágenes interno.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas Windows XP o posterior.</p>
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
<td>El analizador puede detectar un documento en el feeder.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>El analizador puede detectar un documento en la placa plana.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>El analizador solo puede detectar un documento en el feeder mediante el examen.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>El analizador tiene un dúplex.</td>
</tr>
<tr class="odd">
<td>ALIMENTAR</td>
<td>El analizador tiene instalado un controlador de documentos automático.</td>
</tr>
<tr class="even">
<td>PLANA</td>
<td>El analizador tiene una placa plana.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>En la tabla siguiente se describen las constantes que son válidas Windows XP. Estos valores han quedado en desuso Windows 7 y Windows Vista y no deben usarse.</p>
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
<td>El analizador puede saber cuándo está instalado el dúplex.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>El analizador puede saber cuándo está instalado el alimentador automático de documentos.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite en Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el origen y el modo de adquisición del analizador actual. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar el origen de adquisición actual del analizador o para escribir esta propiedad para establecer el origen y el modo del analizador. Además, las aplicaciones usan esta propiedad para habilitar y deshabilitar la funcionalidad del dúplex.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>La tabla siguiente tiene las diez constantes que son válidas con esta propiedad. </p>
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
<td>Examinar mediante el feeder de documentos.</td>
</tr>
<tr class="even">
<td>PLANA</td>
<td>Examinar con la pantalla plana.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Examen mediante operaciones de dúplex.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Habilita la alimentación automática del siguiente documento después de un examen.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Examinar primero la parte frontal del documento. Este valor es válido cuando se establece DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Examinar primero la parte posterior del documento. Este valor es válido cuando se establece DUPLEX.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Examinar solo la parte delantera. Este valor es válido cuando se establece DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Examinar solo la parte posterior. Este valor es válido cuando se establece DUPLEX.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Examinar la página siguiente del documento.</td>
</tr>
<tr class="even">
<td>PREFEED</td>
<td>Habilite el modo de fuente previa. Coloque previamente el siguiente documento durante el examen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td ><p>Contiene el estado actual del sistema de distribución de documentos, fuente de documentos o dúplex instalados del analizador. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación lee esta propiedad para determinar si el dispositivo del analizador está listo para usarse. Esta es una manera ideal de comprobar si el papel está en la fuente antes de adquirir una imagen.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se tienen las constantes que son válidas con esta propiedad. Un asterisco * indica que la marca no se admite en Windows Vista o versiones posteriores. El <strong>símbolo V</strong> indica que la marca solo se admite en Windows Vista y versiones posteriores. </p>
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
<td>El escáner tiene un documento en la placa plana.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>El dúplex está habilitado y listo para usarse.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>La cubierta de la cómoda plana está arriba.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>La ruta de acceso del papel está cubierta y impide el funcionamiento correcto.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Un documento se alimenta en el feeder del documento.</td>
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
<td>El escáner no está listo debido a un problema de bombilla.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td ><p>Contiene todos los caracteres válidos que una aplicación puede usar para crear cadenas de aprobador válidas. Un aprobador es una impresora instalada en un escáner que imprime un mensaje de texto en cada página examinada. El minidriver debe validar la configuración de la <strong>propiedad WIA_DPS_ENDORSER_STRING</strong> con el juego de caracteres válido de esta propiedad. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td ><p>Contiene una cadena que se va a aprobar (es decir, imprimir) en cada página que el minidriver examina. Una aplicación establece esta propiedad mediante el juego de caracteres válido que se notifica en <strong>la WIA_DPS_ENDORSER_CHARACTERS</strong> propiedad . El minidriver solo debe aprobar documentos si se establece una cadena en esta propiedad. Una cadena vacía significa que la funcionalidad del aprobador está deshabilitada.</p>
<p>Dado que es responsabilidad del controlador interpretar la cadena de aprobador, el controlador puede usar caracteres especiales en <strong>WIA_DPS_ENDORSER_STRING</strong>. Sin embargo, solo las aplicaciones comprenderían estos caracteres.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Un controlador que admita la <strong>propiedad WIA_DPS_ENDORSER_STRING</strong> debe admitir la siguiente lista de tokens. </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE$</td>
<td>Fecha con el formato YYYY/MM/DD.</td>
</tr>
<tr class="even">
<td>$DAY$</td>
<td>El día con el formato DD.</td>
</tr>
<tr class="odd">
<td>$MONTH$</td>
<td>Mes del año con el formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE_COUNT$</td>
<td>Número de páginas transferidas.</td>
</tr>
<tr class="odd">
<td>$TIME$</td>
<td>Hora del día con el formato HH:MM:SS.</td>
</tr>
<tr class="even">
<td>$YEAR$</td>
<td>Año con el formato YYYY.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td ><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo se admite en Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la dirección SOAP de un dispositivo de analizador de servicios web. El mini driver de WIA 2.0 crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o alineación horizontal, para los documentos colocados en el plano plano. El minidriver crea y mantiene esta propiedad.</p>
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
<td>El papel se deja justificado.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>El papel está centrado.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>El documento se justifica a la derecha.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) desde la placa de un escáner de pantalla plana en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que mueven las hojas a la placa de un escáner plano para su examen. Esta propiedad es obligatoria para los escáneres que tienen una placa. En su lugar, otros tipos de analizador <strong>implementarán WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> propiedad .</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el ancho máximo, en milésimas de pulgada, que se examina en el eje horizontal (X) desde un escáner de fuente de hoja o portátil en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que analizan sin mover hojas a la placa de un escáner de pantalla plana. Esta propiedad es obligatoria para los escáneres de hoja, de desplazamiento y de mano.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td ><p>Contiene el tiempo máximo para examinar una sola página con la configuración de propiedades actual, en milisegundos. Una aplicación lee esta propiedad para calcular el tiempo que se va a tardar en examinar una página. Esto resulta útil al determinar las condiciones de un dispositivo que ha dejado de responder. El minidriver crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los analizadores.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene las dimensiones horizontales físicas de la página más pequeña que el feeder de documentos del analizador puede examinar, en milésimas de pulgada. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene las dimensiones verticales físicas de la página más pequeña que el feeder de documentos del analizador puede examinar, en milésimas de pulgada. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vea también</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica horizontal. Resolución óptica horizontal más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones que puede generar el dispositivo. En su lugar, esta es la resolución de la óptica del dispositivo. El minidriver crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los analizadores.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Resolución óptica vertical. Resolución óptica vertical más alta admitida en PPP. Esta propiedad es un valor único. Esta no es una lista de todas las resoluciones generadas por el dispositivo. En su lugar, esta es la resolución de la óptica del dispositivo. El minidriver crea y mantiene esta propiedad. Esta propiedad es necesaria para todos los analizadores.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td ><p>Contiene la configuración de orientación actual. El minidriver crea y mantiene esta propiedad.</p>
<p>Una aplicación establece la <strong>WIA_DPS_ORIENTATION</strong> propiedad para definir la orientación original de una página o imagen que se va a adquirir. Para obtener información sobre cómo usar WIA_DPS_ORIENTATION, <strong>consulte WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las cuatro constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Defination</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PAISAJE</td>
<td>Rotación en sentido contrario a las agujas del reloj de 90 grados, en relación con la orientación VERTICAL.</td>
</tr>
<tr class="even">
<td>RETRATO</td>
<td>0 grados.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Rotación en sentido contrario a las agujas del reloj de 180 grados, en relación con la orientación VERTICAL.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Rotación en sentido contrario a las agujas del reloj de 270 grados, con respecto a la orientación VERTICAL.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vea también</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td ><p>Color que se usa para rellenar cuando no hay suficientes datos de imagen para rellenar un búfer solicitado. Esta propiedad se implementa para los analizadores que alojen el búfer. Esta propiedad es opcional para todos los analizadores. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El formato de la información de color <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">es RGBQUAD.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el alto, en milésimas de pulgada, de la página seleccionada actualmente. El minidriver crea y mantiene la <strong>WIA_DPS_PAGE_HEIGHT</strong> propiedad . Una aplicación lee esta propiedad para determinar las dimensiones físicas de la página que se está analizando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad notifica el alto de la página cuya propiedad <strong>WIA_DPS_PAGE_SIZE</strong> está establecida en WIA_PAGE_CUSTOM (que es un valor de la <strong>propiedad WIA_DPS_PAGE_SIZE).</strong> <strong>WIA_DPS_PAGE_HEIGHT</strong> debe estar sincronizado con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que informa del alto, en píxeles, de la página que se va a examinar.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el tamaño de la página que está seleccionada actualmente para examinarse. Para seleccionar las dimensiones de la página que se va a examinar, una aplicación establece esta propiedad. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad. </p>
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
<td>8267 X 11692 (orientación VERTICAL)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definido por los valores de las propiedades <strong>WIA_DPS_PAGE_HEIGHT</strong> y <strong>WIA_DPS_PAGE_WIDTH</strong> propiedades</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientación VERTICAL)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>El valor de la <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina la orientación de la página seleccionada actualmente. Las <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT</strong> informen de las dimensiones de la página, en milésimas de pulgada. Tenga en cuenta que estas propiedades deben estar de acuerdo con <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong>, que contienen las dimensiones de la página en píxeles. Los valores válidos de tipo WIA_PROP_LIST deben depender de la configuración válida de la <strong>WIA_IPS_ORIENTATION</strong> propiedad. Si el dispositivo no puede examinar documentos orientados horizontalmente con una configuración de WIA_PAGE_A4, WIA_PAGE_A4 no debe aparecer en la lista de valores válidos para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> cuando <strong>WIA_IPS_ORIENTATION</strong> esté establecido en LANSCAPE.</p>
<p>Si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en cualquier valor distinto de WIA_PAGE_CUSTOM, el minidriver debe ajustar los valores de <strong>WIA_DPS_PAGE_WIDTH</strong> y <strong>WIA_DPS_PAGE_HEIGHT a</strong> las dimensiones de la página en milésimas de pulgada. También debe ajustar los valores de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> y <strong>WIA_IPS_YEXTENT</strong> a las dimensiones de la página en píxeles.</p>
<p>Si se cambia una configuración de extensión (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> <strong>o WIA_IPS_YEXTENT</strong>) a un valor que no coincide con la configuración de tamaño de página actual, el minidriver debe cambiar el valor de la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> a WIA_PAGE_CUSTOM. El minidriver también debe modificar <strong>WIA_DPS_PAGE_WIDTH</strong> o <strong>WIA_DPS_PAGE_HEIGHT</strong> de acuerdo con la nueva configuración de extensión.</p>
<p>Si <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> se establece en LANSCAPE, se volteará la configuración &quot; de extensión. &quot; Por ejemplo, si una aplicación establece <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_A4, el minidriver debe establecer <strong>WIA_DPS_PAGE_WIDTH</strong> en 11692 y <strong>WIA_DPS_PAGE_HEIGHT</strong> en 8267. (El minidriver también debe establecer <strong>WIA_IPS_XEXTENT</strong> y <strong>WIA_IPS_YEXTENT</strong> en consecuencia). Tenga en <strong>cuenta que WIA_DPS_PAGE_SIZE</strong> se establece en WIA_PAGE_CUSTOM, el valor de orientación no se usa para determinar las dimensiones de extensión de la página que se va a examinar.</p>
<p>El minidriver es responsable de garantizar que la <a href="-wia-wiaitempropscanneritem.md"><strong>propiedad WIA_IPS_ORIENTATION</strong></a> esté de acuerdo con el área de selección actual. Si una aplicación cambia el valor de <strong>WIA_IPS_ORIENTATION a</strong> uno que no es válido para el tamaño de página seleccionado actualmente, el minidriver debe cambiar el valor de <strong>WIA_DPS_PAGE_SIZE a</strong> un tamaño de página compatible con el nuevo valor de orientación.</p>
<p>Si una aplicación establece la <strong>propiedad WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM, el área de selección actual no se ve afectada. El minidriver wia debe obtener el diseño de imagen actual, empezando por la configuración actual de las propiedades <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> y <strong>WIA_IPS_YPOS</strong> propiedades. Si la configuración de tamaño de página da como resultado un área de selección que está fuera de la habitación del analizador, el minidriver debe ajustar automáticamente los valores de las propiedades <strong>WIA_IPS_XPOS</strong> y <strong>WIA_IPS_YPOS</strong> a la configuración válida. Si las propiedades <strong>WIA_DPS_PAGE_SIZE</strong> y <strong>WIA_IPS_ORIENTATION</strong> se establecen al mismo tiempo y no son válidas cuando se aplican en combinación, el minidriver debe producir un error en la configuración de la aplicación devolviendo un error en <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvValidateItemProperties</a>. .</p>
<p>Los cuatro ejemplos siguientes muestran diferentes <strong>WIA_DPS_PAGE_SIZE</strong> escenarios.</p>
<ol>
<li>El controlador informa de la configuración.</li>
<li>Una aplicación establece la <strong>propiedad WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_LETTER.</li>
<li>Una aplicación establece la <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> propiedad en LANSCAPE.</li>
<li>Una aplicación cambia la <a href="-wia-wiaitempropscanneritem.md"><strong>propiedad WIA_IPS_XEXTENT</strong></a> a un valor más pequeño.</li>
</ol>
<p><strong>Ejemplo 1: el minidriver informa de la configuración</strong></p>
<p>En el ejemplo siguiente, el minidriver establece un área de selección personalizada antes de que una aplicación establece las propiedades de WIA. En este caso, el área de selección representa todo el plano.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Ejemplo 2: una aplicación establece la propiedad</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>en WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Ejemplo 3: Una aplicación establece la propiedad</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>en LANSCAPE</strong></p>
<p>La habitación física debe ser capaz de adquirir una página que estaba originalmente en orientación horizontal.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Ejemplo 4: Una aplicación cambia la propiedad</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>a un valor<strong>más pequeño</strong>  </p>
<p>En el ejemplo siguiente, una aplicación cambia la <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> propiedad a 1000. El minidriver debe suponer que el nuevo valor contenido en <strong>WIA_IPS_XEXTENT</strong> ya no es válido <strong></strong> para la propiedad <strong>WIA_DPS_PAGE_SIZE</strong> y, por tanto, debe cambiar WIA_DPS_PAGE_SIZE a WIA_PAGE_CUSTOM. El minidriver también debe <strong>ajustar</strong>WIA_DPS_PAGE_WIDTH .</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td ><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el ancho de la página actual seleccionada, en milésimas de pulgada. Una aplicación lee esta propiedad para determinar las dimensiones físicas de la página que se está analizando. Si la configuración de extensión es diferente de los tamaños de página conocidos, esta propiedad notifica el ancho de la página cuya propiedad WIA_DPS_PAGE_SIZE <strong>está</strong> establecida en WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> debe estar sincronizado con el valor de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, que informa del ancho, en píxeles, de la página que se va a examinar. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el número actual de páginas que se adquirirán de un feeder de documentos automático. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>; Acceso: lectura/escritura; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (de cero a hasta el número máximo de páginas que puede contener el fuente de documentos)</p>
<p>Una aplicación lee esta propiedad para determinar la capacidad de página del fuente de documentos. La aplicación también establece esta propiedad en el número de páginas que va a examinar.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si el modo dúplex está habilitado (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> se establece en FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> sigue siendo igual al número de páginas que se va a examinar.
</blockquote>
</div>
<div>
 
</div>
<p>Una hoja de papel contendrá automáticamente dos páginas si DUPLEX está habilitado, incluso si el lado posterior de la página está en blanco.</p>
<p>Si <strong>WIA_DPS_PAGES</strong> en 1, un analizador procesa uno de los lados de la página. Se recomienda que si un analizador no puede examinar solo un lado de una página en modo <strong>dúplex,</strong> el valor válido de WIA_DPS_PAGES para el miembro Inc de la estructura WIA_PROPERTY_INFO se debe cambiar a 2. Este valor indica a la aplicación que debe solicitar páginas en múltiplo de dos. Un valor de cero significa <em>que se</em> examinarán todas las páginas que se cargan actualmente en el feeder de documentos.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td ><p>Especifica el color de la placa en la parte posterior de la hoja que se va a examinar. Esta propiedad es opcional para los escáneres que tienen una placa. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>El formato de la información de color <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">es RGBQUAD.</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica el modo de vista previa de un dispositivo. Una aplicación establece esta propiedad para colocar el dispositivo en modo de vista previa.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad. </p>
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
<tr class="odd">
<td ><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td ><p>Contiene un valor que indica si el analizador almacenará en caché las páginas de un búfer del analizador antes de enviarlos a la aplicación.</p>
<p>Un valor de cero deshabilita el examen por adelantado y no se examinará ninguna página con antelación. Al realizar transferencias de datos normales en el elemento de análisis por adelantado almacenado en búfer, se recuperan las páginas en búfer. Las propiedades de WIA no se pueden cambiar durante una operación de examen por adelantado. Esta propiedad es opcional.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md"></a> WIA_PROP_RANGE de cero al número máximo de páginas que puede contener el fuente de documentos.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows 7 y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Indica el origen de entrada (plano, el adaptador de fuente de documentos automático o el adaptador de análisis de fil) desde el que se debe examinar o la ubicación de almacenamiento desde la que se transfieren los datos.</p>
<p>Un evento de examen notifica a la aplicación que el usuario ha iniciado un examen, pero el evento no proporciona el nombre del elemento WIA que representa el origen de entrada. El controlador de eventos de la aplicación puede consultar la propiedad WIA_DPS_SCAN_AVAILABLE_ITEM del elemento raíz para obtener el nombre del elemento de origen de entrada.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md"></a> WIA_PROP_RANGE de cero al número máximo de páginas que puede contener el fuente de documentos.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el identificador de servicio de un dispositivo de analizador de servicios web. El mini driver de WIA 2.0 crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o alineación y detección de borde, para los documentos que se colocan en la pantalla plana. El minidriver crea y mantiene esta propiedad. Esta propiedad indica cómo la hoja se coloca horizontalmente en la cabeza de examen de un escáner portátil o de hoja. La propiedad se usa para predecir dónde se coloca un documento en la parte principal del examen.</p>
<p>En el caso de los escáneres que admiten más de un responsable de examen, esta propiedad es relativa al más alto. Esta propiedad es obligatoria para los escáneres de hojas, de desplazamiento y portátiles.</p>
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
<td>La hoja se centra en la parte principal del examen.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>La hoja se coloca a la derecha con respecto a la cabeza de examen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no es compatible con Windows Vista. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica si un elemento necesita que se muestre al usuario un control de vista previa. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad. </p>
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
<td>No muestre un control de vista previa al usuario, porque este dispositivo no puede realizar una vista previa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad solo es compatible con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Usado por el servicio WIA para informar al mini driver sobre el nombre de la cuenta de usuario (incluido el nombre de dominio de red cuando corresponda) de la sesión en la que se ejecuta la aplicación WIA actual.</p>
<p>Se trata de una propiedad de elemento raíz, administrada por el servicio WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene el registro, o la alineación vertical y la detección de borde, para los documentos colocados en la pantalla plana. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad. </p>
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
<td>El papel está en la parte superior.</td>
</tr>
<tr class="even">
<td>CENTRADO</td>
<td>El papel está centrado.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>El papel se justifica en la parte inferior.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Consulte también</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) desde la placa de un escáner plano en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos, que mueven las hojas a la placa de un escáner de pantalla plana para el examen. Esta propiedad es obligatoria para los escáneres que tienen una placa. En su lugar, otros tipos de analizador <strong>implementarán WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> propiedad .</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Esta propiedad no se admite con Windows Vista y versiones posteriores. Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Especifica el alto máximo, en milésimas de pulgada, que se examina en el eje vertical (Y) desde un escáner de alimentación de hoja o de mano en la resolución actual. Esta propiedad también se aplica a los alimentadores de documentos automáticos que analizan sin mover hojas a la placa de un escáner de pantalla plana. Esta propiedad es obligatoria para los escáneres de hoja. Los escáneres de desplazamiento y de mano no deben implementar esta propiedad.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 

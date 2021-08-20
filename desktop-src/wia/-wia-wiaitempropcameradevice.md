---
description: Windows Los dispositivos de hardware de adquisición de imágenes (WIA) tienen valores de propiedad que se almacenan en Windows registro. Para obtener más información, vea Constantes de propiedad de dispositivo común.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Constantes de propiedad de dispositivo de cámara (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c67c65b311994fdb3a973494c4aa45b1d80c97e4c064b3c195c43a16cbfdeb69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034886"
---
# <a name="camera-device-property-constants"></a>Constantes de propiedad de dispositivo de cámara

Windows Los dispositivos de hardware de adquisición de imágenes (WIA) tienen valores de propiedad que se almacenan en Windows registro. Para obtener más información, [**vea Constantes comunes de propiedades de dispositivo.**](-wia-wiaitempropcommondevice.md)

Las siguientes constantes de propiedad de dispositivo, con sus cadenas asociadas, son específicas de las cámaras digitales. El prefijo "WIA DPC" indica una propiedad de dispositivo para cámaras y es la convención \_ de nomenclatura usada en \_ C/C++. Con fines de scripting, estas constantes usan el prefijo "CameraDevice" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.

> [!Note]  
> WIA no admite cámaras en Windows Vista ni versiones posteriores. Para esas versiones de Windows, use la API de dispositivo portátil (WPD) de Windows descrita en el Kit de desarrollo de controladores (DDK) de Windows para adquirir imágenes de las cámaras.

 



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
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td style="text-align: left;">Número de imágenes que ha tomado la cámara. El minidriver crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td style="text-align: left;">Número de imágenes que se pueden tomar, dada la configuración de propiedad actual. Si esta configuración cambia y los cambios afectan al tamaño de las imágenes que genera el dispositivo de cámara, el minidriver WIA debe actualizar el número de imágenes restantes. El minidriver crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td style="text-align: left;">Indica el modo de exposición actual de la cámara. Una aplicación cambia esta propiedad para controlar el modo de exposición del dispositivo de cámara.<br/> Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> La tabla siguiente tiene las siete constantes que son válidas con esta propiedad.<br/> 
<table>
<thead>
<tr class="header">
<th>Modo de exposición</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>El usuario establece la velocidad de obturación y la apertura.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>La cámara establece automáticamente la velocidad de obturación y la apertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>El usuario establece la apertura y la cámara establece automáticamente la velocidad de obturación.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>El usuario establece la velocidad de obturación y la cámara establece automáticamente la apertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>La cámara establece automáticamente la velocidad de obturación y la apertura, optimizadas para la materia.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>La cámara establece automáticamente la velocidad de obturación y la apertura, optimizadas para escenas que contienen movimiento rápido.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>La cámara establece automáticamente la velocidad de obturación y la apertura, optimizadas para la fotografía vertical.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td style="text-align: left;"><p>Permite el ajuste del punto de conjunto del control de exposición automática de la cámara digital. Por ejemplo, una configuración de cero no cambia el nivel de exposición automática del conjunto de fábrica. Las unidades están en paradas que se escalan por un &quot; &quot; factor de 1000, para permitir valores de detenciones fraccionales. Un valor de 2000 corresponde a dos detendrá más exposición (cuatro veces más energía en el sensor), lo que produce imágenes más brillantes. Un valor de -1000 corresponde a una detención menos exposición (la mitad de la energía del sensor) que produce imágenes más oscuras. Los valores de configuración están en unidades del Sistema aditivo de exposición fotográfica (APEX). Esta propiedad puede expresarse como una lista o un intervalo de valores. Esta propiedad se usa normalmente solo cuando el dispositivo tiene la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> establecida en EXPOSUREMODE_MANUAL.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde a la velocidad de obturación, en segundos que se escalan en 10 000. Normalmente, el dispositivo usa esta propiedad solo cuando la <strong>propiedad WIA_DPC_EXPOSURE_MODE</strong> está establecida en EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde a la apertura de la lente, en unidades del número f-stop escalado en 100. El valor de esta propiedad suele ser válido solo cuando la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> se establece en EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la configuración actual del modo flash para el dispositivo de cámara. El controlador de dispositivo enumera los valores admitidos de esta propiedad. Una aplicación escribe esta propiedad para establecer el modo flash del dispositivo de cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las seis constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo flash</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>El dispositivo de cámara determina la configuración de flash adecuada.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>El dispositivo de cámara está configurado para parpadear independientemente de las condiciones de iluminación actuales.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>El dispositivo de cámara está configurado <em>para no</em> parpadear para ninguna imagen tomada.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>El dispositivo de cámara determina la configuración de flash adecuada mediante la reducción de los ojos rojos, independientemente de las condiciones de iluminación actuales.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>El dispositivo de cámara está configurado para usar la reducción de ojos rojos y el flash, independientemente de las condiciones de iluminación actuales.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>El dispositivo de cámara está configurado para sincronizarse con unidades flash externas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la configuración actual del modo de enfoque para el dispositivo de cámara. El controlador de dispositivo enumera los valores admitidos de esta propiedad. Una aplicación escribe esta propiedad para establecer el modo de enfoque para el dispositivo de cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo de enfoque</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>El dispositivo de cámara está configurado para permitir que el usuario se centre manualmente.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>El dispositivo de cámara está configurado para centrarse automáticamente.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>El dispositivo de cámara está configurado para centrarse automáticamente mediante la configuración de macros de corto alcance.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la fuente de alimentación actual para el dispositivo de la cámara. Una aplicación lee esta propiedad para determinar qué fuente de alimentación usa la cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo de energía</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>El dispositivo de cámara funciona en un adaptador de alimentación.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>El dispositivo de cámara funciona con batería.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td style="text-align: left;"><p>Porcentaje de energía de la batería que queda para operar el dispositivo de la cámara. Este valor debe ser un entero comprendido entre 0 y 100. Una aplicación lee esta propiedad para determinar la duración restante de la batería del dispositivo de la cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td style="text-align: left;"><p>Ancho, en píxeles, de una imagen en miniatura que se usará para las imágenes recién capturadas. Una aplicación lee este valor para obtener un tamaño estimado para mostrar miniaturas en su interfaz de usuario.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o Solo lectura (WIA_PROP_NONE), Valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td style="text-align: left;"><p>Ancho, en píxeles, de una imagen en miniatura que se usará para las imágenes recién capturadas. Una aplicación lee este valor para obtener un tamaño estimado para mostrar miniaturas en su interfaz de usuario.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o Solo lectura (WIA_PROP_NONE), Valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td style="text-align: left;"><p>Ancho en píxeles que se usará para las imágenes recién capturadas. La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la <strong>WIA_DPC_PICT_HEIGHT</strong> propiedad. Si el ancho y el alto individuales se pueden establecer linealmente y ortogonales entre sí, se pueden expresar como un intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td style="text-align: left;"><p>Alto en píxeles que se usará para las imágenes recién capturadas. La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la <strong>WIA_DPC_PICT_WIDTH</strong> propiedad. Si el ancho y el alto individuales se pueden establecer linealmente y ortogonales entre sí, se pueden expresar como un intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td style="text-align: left;"><p>Diseñado para ser aproximadamente lineal con respecto a la calidad de imagen percibida en una amplia gama de contenido de la escena, y contiene un intervalo o una lista de enteros. Los enteros más pequeños se usan para representar una calidad inferior (es decir, la compresión máxima), mientras que los enteros más grandes se usan para representar una mayor calidad (es decir, compresión mínima). Cualquier configuración disponible en un dispositivo solo es relativa a ese dispositivo y, por tanto, es específica del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no use.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td style="text-align: left;"><p>Tiempo, en milisegundos, entre las capturas de imágenes en una operación de captura de intervalo de tiempo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td style="text-align: left;"><p>El número de imágenes que el dispositivo intenta capturar durante una captura de intervalo de tiempo.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td style="text-align: left;"><p>Tiempo, en milisegundos, entre capturas de imágenes durante una operación de ráfaga.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td style="text-align: left;"><p>Número de imágenes que el dispositivo intenta capturar durante una operación de ráfaga.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo especial de adquisición de imágenes de la cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo de efecto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Capture una imagen en el modo estándar para la cámara.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Capturar una imagen de escala de grises.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Captura de una imagen sepia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td style="text-align: left;"><p>Proporción de zoom efectiva de la imagen adquirida de la cámara digital, escalada en un factor de 10. Un valor de 10 corresponde a la ausencia de zoom digital (1X), que es el tamaño estándar de la escena capturado por la cámara. Un valor de 20 corresponde a un zoom 2X, donde la cámara captura un cuarto del tamaño de la escena estándar.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td style="text-align: left;"><p>Nijez percibido de una imagen capturada. Esta propiedad puede usar una lista de valores o un intervalo de valores. El valor mínimo representa la menor cantidad de ni sharpness, mientras que el valor máximo representa la niguidad máxima. Normalmente, un valor en medio del intervalo representa la niguidad normal o predeterminada.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td style="text-align: left;"><p>Contraste percibido de una imagen capturada. Esta propiedad puede contener una lista de valores o un intervalo de valores. El valor mínimo admitido representa la menor cantidad de contraste, mientras que el valor máximo representa el mayor contraste. Normalmente, un valor en medio del intervalo representa un contraste normal o predeterminado.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td style="text-align: left;"><p>Establece el modo de captura de imágenes.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las tres constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo de captura</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Modo normal para la cámara.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Capture más de una imagen en sucesión rápida, tal como se define en los valores de las propiedades <strong>WIA_DPC_BURST_NUMBER</strong> y <strong>WIA_DPC_BURST_INTERVAL</strong> rápidas.</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Capture más de una imagen en sucesión, tal como se define en WIA_DPC_TIMELAPSE_NUMBER <strong>y</strong> <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> propiedades.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td style="text-align: left;"><p>Valor que representa la cantidad de retraso de tiempo, en milisegundos, que se debe insertar entre el desencadenador de captura y el inicio real de la captura de datos. Esta propiedad no está pensada para usarse para describir el tiempo entre fotogramas para una sola iniciación, varias capturas como ráfagas o intervalos de tiempo, que tienen propiedades de intervalo independientes WIA_DPC_BURST_INTERVAL y <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. <strong></strong> En esos casos, sigue funcionando como un retraso inicial antes de capturar la primera imagen de la serie, independientemente del tiempo entre fotogramas. Si no hay ningún retraso de captura previa, esta propiedad debe establecerse en cero.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td style="text-align: left;"><p>Permite la emulación de la configuración de velocidad de película en una cámara digital. La configuración corresponde a las designaciones ISO (ASA/LOD). Normalmente, un dispositivo admite valores enumerados discretos, pero es posible un control continuo sobre un intervalo de valores. Un valor de 0xFFFF corresponde a la configuración ISO automática.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo que usa la cámara para ajustar automáticamente la configuración de exposición.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Modo de medición de exposición</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Establezca la exposición en función de un promedio de toda la escena.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Establezca la exposición en función de un promedio ponderado en el centro.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Establezca la exposición en función de un patrón multispota.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Establezca la exposición en función de un punto central.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo que usa la cámara para ajustar automáticamente el foco.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabla siguiente tiene las dos constantes que son válidas con esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Modo de medición de foco</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Ajuste el foco en función de un punto central.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Ajuste el foco en función de un patrón multispota.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td style="text-align: left;"><p>Distancia, en milímetros, entre el plano de captura de imágenes de la cámara digital y el punto de enfoque. Un valor de 0xFFFF corresponde a un valor mayor que 655 metros.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td style="text-align: left;"><p>Longitud focal equivalente a 35 mm. Los valores de esta propiedad corresponden a la longitud focal en milímetros multiplicado por 100. La longitud focal determina el zoom óptico.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td style="text-align: left;"><p>Cadena Unicode terminada en NULL que representa la ganancia roja, verde y azul aplicada a los datos de imagen, respectivamente. Por ejemplo, 4:25:50 representa una ganancia roja de 4, una ganancia verde de 25 y una ganancia &quot; &quot; azul de 50.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td style="text-align: left;"><p>Especifica cómo pondera la cámara digital los canales de color.</p>
<p>Tipo: <strong>VT_I4</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A continuación se muestra una lista de valores posibles para esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Saldo blanco</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>El saldo de blanco se establece directamente mediante <strong>la WIA_DPC_RGB_GAIN</strong> propiedad .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>La cámara usa un mecanismo automático para establecer el equilibrio de blanco.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>La cámara determina la configuración del equilibrio de blanco cuando un usuario presiona el botón de captura mientras apunta la cámara a una superficie blanca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>La cámara establece el equilibrio de blanco en un valor adecuado para su uso en condiciones de verano.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>La cámara establece el equilibrio de blanco en un valor adecuado para su uso con una fuente de luz blanca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>La cámara establece el equilibrio de blanco en un valor adecuado para su uso con una fuente de luz más ligera.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>La cámara establece el equilibrio de blanco en un valor adecuado para su uso con un flash electrónico.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td style="text-align: left;"><p>Describe una dirección URL. La dirección URL descrita por esta proroperty es aquella en la que se pueden cargar imágenes u objetos, una vez adquiridos desde el dispositivo, según uno de los escenarios siguientes.</p>
<ul>
<li>Una aplicación WIA lee esta propiedad y permite al usuario cargar automáticamente imágenes en la dirección URL.</li>
<li>Una aplicación establece la dirección URL y otros dispositivos (quioscos, etc.) usan esta propiedad.</li>
</ul>
<p>Microsoft Windows no carga imágenes por sí mismo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td style="text-align: left;"><p>Nombre del propietario (que es el usuario actual) del dispositivo. El dispositivo usa esta propiedad para rellenar el campo Artist en cada imagen EXIF que captura.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td style="text-align: left;"><p>Notificación de copyright. El dispositivo usa esta propiedad para rellenar el campo Copyright en cada imagen EXIF que captura.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: Lectura/escritura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 





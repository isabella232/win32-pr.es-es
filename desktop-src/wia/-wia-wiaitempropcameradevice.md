---
description: Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows. Para obtener más información, consulte Common Device Property constants.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Constantes de propiedad de dispositivo de cámara (Wiadef. h)
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
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497536"
---
# <a name="camera-device-property-constants"></a>Constantes de propiedades de dispositivo de cámara

Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows. Para obtener más información, consulte [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).

Las siguientes constantes de propiedades de dispositivo, con sus cadenas asociadas, son específicas de las cámaras digitales. El prefijo "WIA \_ DPC \_ " indica una propiedad de dispositivo para las cámaras y es la Convención de nomenclatura utilizada en C/C++. Con el fin de crear scripts, estas constantes usan el prefijo "CameraDevice" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.

> [!Note]  
> WIA no admite cámaras en Windows Vista o posterior. En el caso de las versiones de Windows, use la API de dispositivo portátil de Windows (WPD) que se describe en el kit de desarrollo de controladores de Windows (DDK) para adquirir imágenes de cámaras.

 



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
<td style="text-align: left;">El número de imágenes que ha tomado la cámara. El minicontrolador crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td style="text-align: left;">El número de imágenes que se pueden tomar, dados los valores de propiedades actuales. Si esta configuración cambia y los cambios afectan al tamaño de las imágenes que genera el dispositivo de cámara, el minicontrolador WIA debe actualizar el número de imágenes restantes. El minicontrolador crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td style="text-align: left;">Indica el modo de exposición actual de la cámara. Una aplicación cambia esta propiedad para controlar el modo de exposición del dispositivo de cámara.<br/> Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> En la tabla siguiente se incluyen las siete constantes que son válidas con esta propiedad.<br/> 
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
<td>El usuario establece la velocidad y la abertura del obturador.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>La cámara establece automáticamente la velocidad y la abertura del obturador.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>El usuario establece la abertura y la cámara establece automáticamente la velocidad del obturador.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>El usuario establece la velocidad del obturador y la cámara establece automáticamente la abertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para seguir siendo importantes.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para escenas que contienen movimiento rápido.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para la fotografía vertical.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td style="text-align: left;"><p>Permite ajustar el punto de establecimiento del control de exposición automática de la cámara digital. Por ejemplo, un valor de cero no cambia el nivel de exposición automática del conjunto de fábrica. Las unidades están en &quot; paradas &quot; que se escalan por un factor de 1000, para permitir valores de detención fraccionarios. Un valor de 2000 corresponde a dos detenciones más de exposición (cuatro veces más energía en el sensor), produciendo imágenes más brillantes. Un valor de-1000 corresponde a una parada menos expuesta (la mitad de la energía en el sensor) que produce imágenes más oscuras. Los valores de configuración están en el sistema aditivo de las unidades de exposición fotográfica (vértice). Esta propiedad se puede expresar como una lista o como un intervalo de valores. Esta propiedad se usa normalmente solo cuando el dispositivo tiene la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> establecida en EXPOSUREMODE_MANUAL.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde a la velocidad del obturador, en segundos, que se escala por 10.000. Normalmente, el dispositivo usa esta propiedad solo cuando la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> está establecida en EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td style="text-align: left;"><p>Corresponde a la abertura de la lente, en unidades del número de detención de f escalado por 100. Normalmente, la configuración de esta propiedad solo es válida cuando la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> está establecida en EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la configuración de modo Flash actual para el dispositivo de cámara. El controlador de dispositivo enumera los valores admitidos de esta propiedad. Una aplicación escribe esta propiedad para establecer el modo flash para el dispositivo de cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se incluyen las seis constantes que son válidas con esta propiedad.</p>

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
<td>El dispositivo de cámara determina la configuración de Flash adecuada.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>El dispositivo de cámara está configurado para parpadear independientemente de las condiciones de iluminación actuales.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>El dispositivo de cámara está configurado para <em>no</em> parpadear en ninguna imagen tomada.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>El dispositivo de cámara determina la configuración de Flash adecuada mediante la reducción de ojos rojos, independientemente de las condiciones de iluminación actuales.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>El dispositivo de cámara está configurado para usar la reducción de ojos rojos y Flash sin tener en consideración las condiciones de iluminación actuales.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>El dispositivo de cámara está configurado para sincronizarse con unidades Flash externas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la configuración del modo de enfoque actual para el dispositivo de cámara. El controlador de dispositivo enumera los valores admitidos de esta propiedad. Una aplicación escribe esta propiedad para establecer el modo de enfoque para el dispositivo de cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</p>

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
<td>El dispositivo de cámara está configurado para permitir que el usuario se Centre manualmente.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>El dispositivo de cámara está configurado para centrarse automáticamente.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>El dispositivo de cámara está configurado para centrarse automáticamente en el uso de la configuración de macros de rango corto.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td style="text-align: left;"><p>Define la fuente de alimentación actual para el dispositivo de cámara. Una aplicación Lee esta propiedad para determinar el origen de energía que está usando la cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</p>

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
<td>El dispositivo de cámara está funcionando en un adaptador de alimentación.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>El dispositivo de cámara está funcionando con la energía de la batería.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td style="text-align: left;"><p>El porcentaje de energía de la batería que queda para operar el dispositivo de cámara. Este valor debe ser un entero comprendido entre 0 y 100. Una aplicación Lee esta propiedad para determinar la duración restante de la batería del dispositivo de cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td style="text-align: left;"><p>Ancho, en píxeles, de una imagen en miniatura que se va a usar para las imágenes recién capturadas. Una aplicación Lee este valor para obtener un tamaño estimado para Mostrar miniaturas en su interfaz de usuario.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura y escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o solo lectura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td style="text-align: left;"><p>Ancho, en píxeles, de una imagen en miniatura que se va a usar para las imágenes recién capturadas. Una aplicación Lee este valor para obtener un tamaño estimado para Mostrar miniaturas en su interfaz de usuario.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura y escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o solo lectura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td style="text-align: left;"><p>Ancho en píxeles que se va a usar para las imágenes recién capturadas. La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la propiedad <strong>WIA_DPC_PICT_HEIGHT</strong> . Si el ancho y el alto individuales se pueden establecer de forma lineal y ortogonal entre sí, se pueden expresar como un intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td style="text-align: left;"><p>Alto en píxeles que se va a usar para las imágenes recién capturadas. La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la propiedad <strong>WIA_DPC_PICT_WIDTH</strong> . Si el ancho y el alto individuales se pueden establecer de forma lineal y ortogonal entre sí, se pueden expresar como un intervalo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td style="text-align: left;"><p>Diseñado para ser aproximadamente lineal con respecto a la calidad de imagen percibida en una amplia gama de contenido de la escena, y contiene un intervalo o una lista de enteros. Los enteros más pequeños se utilizan para representar una calidad inferior (es decir, la compresión máxima), mientras que los enteros más grandes se usan para representar una mayor calidad (es decir, compresión mínima). Cualquier configuración disponible en un dispositivo solo es relativa a ese dispositivo y, por lo tanto, es específico del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reservado, no usar.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td style="text-align: left;"><p>El tiempo, en milisegundos, entre las capturas de imagen en una operación de captura de lapso de tiempo.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td style="text-align: left;"><p>El número de imágenes que el dispositivo intenta capturar durante una captura de lapso de tiempo.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td style="text-align: left;"><p>El tiempo, en milisegundos, entre las capturas de la imagen durante una operación de ráfaga.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td style="text-align: left;"><p>El número de imágenes que el dispositivo intenta capturar durante una operación de ráfaga.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo de adquisición de imagen especial de la cámara.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</p>

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
<td>Capture una imagen en el modo estándar de la cámara.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Capturar una imagen de escala de grises.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Capturar una imagen sepia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td style="text-align: left;"><p>La relación de zoom efectiva de la imagen adquirida de la cámara digital, escalada por un factor de 10. Un valor de 10 corresponde a la ausencia del zoom digital (1X), que es el tamaño de la escena estándar capturado por la cámara. Un valor de 20 corresponde a un zoom de 2X, donde la cámara captura un cuarto del tamaño de la escena estándar.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td style="text-align: left;"><p>Nitidez percibido de una imagen capturada. Esta propiedad puede utilizar una lista de valores o un intervalo de valores. El valor mínimo representa la cantidad mínima de nitidez, mientras que el valor máximo representa la nitidez máxima. Normalmente, un valor en el centro del intervalo representa la nitidez normal o predeterminada.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td style="text-align: left;"><p>El contraste percibido de una imagen capturada. Esta propiedad puede contener una lista de valores o un intervalo de valores. El valor mínimo admitido representa la menor cantidad de contraste, mientras que el valor máximo representa el mayor contraste. Normalmente, un valor en el centro del intervalo representa el contraste normal o predeterminado.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td style="text-align: left;"><p>Establece el modo de captura de imagen.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</p>

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
<td>Modo normal de la cámara.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Capturar más de una imagen en una sucesión rápida según lo definido por los valores de las propiedades <strong>WIA_DPC_BURST_NUMBER</strong> y <strong>WIA_DPC_BURST_INTERVAL</strong> .</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Capturar más de una imagen en sucesión tal y como se define en las propiedades <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> y <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td style="text-align: left;"><p>Valor que representa la cantidad de tiempo de retardo, en milisegundos, que se debe insertar entre el desencadenador de captura y el inicio real de la captura de datos. Esta propiedad no está pensada para usarse con el fin de describir el tiempo entre fotogramas para la iniciación única, varias capturas, como la ráfaga o el lapso de tiempo, que tienen propiedades de intervalo independientes <strong>WIA_DPC_BURST_INTERVAL</strong> y <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. En esos casos, todavía actúa como un retraso inicial antes de que se Capture la primera imagen de la serie, independientemente del tiempo entre fotogramas. En el caso de que no haya retraso en la captura, esta propiedad debe establecerse en cero.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td style="text-align: left;"><p>Permite la emulación de la configuración de velocidad de película en una cámara digital. La configuración corresponde a las designaciones ISO (ASA/DIN). Normalmente, un dispositivo admite valores enumerados discretos, pero es posible el control continuo sobre un intervalo de valores. Un valor de 0xFFFF corresponde a la configuración automática de ISO.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo que la cámara utiliza para ajustar automáticamente la configuración de exposición.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

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
<td>Establezca la exposición en función de la media de toda la escena.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Establezca la exposición en función de una media ponderada en el centro.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Establezca la exposición en función de un patrón de multizona.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Establezca la exposición en función de una zona central.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Especifica el modo que la cámara utiliza para ajustar automáticamente el foco.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</p>

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
<td>Ajuste el foco en función de una zona central.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Ajuste el foco en función de un patrón de selección multizona.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td style="text-align: left;"><p>Distancia, en milímetros, entre el plano de captura de imágenes de la cámara digital y el punto de foco. Un valor de 0xFFFF corresponde a una configuración superior a 655 metros.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td style="text-align: left;"><p>La longitud focal equivalente de 35mm. Los valores de esta propiedad se corresponden con la longitud focal en milímetros multiplicada por 100. La longitud focal determina el zoom óptico.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td style="text-align: left;"><p>Una cadena Unicode terminada en null que representa la ganancia de color rojo, verde y azul aplicada a los datos de imagen, respectivamente. Por ejemplo, &quot; 4:25:50 &quot; representa una ganancia roja de 4, una ganancia verde de 25 y una ganancia azul de 50.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td style="text-align: left;"><p>Especifica cómo la cámara digital pondera los canales de color.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>A continuación se muestra una lista de los valores posibles para esta propiedad.</p>

<table>
<thead>
<tr class="header">
<th>Balance de blanco</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>El balance de blanco se establece directamente mediante la propiedad <strong>WIA_DPC_RGB_GAIN</strong> .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>La cámara utiliza un mecanismo automático para establecer el equilibrio de blanco.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>La cámara determina el valor de balance de blanco cuando un usuario presiona el botón capturar mientras apunta a la cámara en una superficie blanca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>La cámara establece el balance de blanco con un valor adecuado para su uso en condiciones de horario de verano.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>La cámara establece el balance de blanco con un valor adecuado para su uso con una fuente de luz fluorescente.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>La cámara establece el balance de blanco con un valor adecuado para su uso con una fuente de luz de Tungsten.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>La cámara establece el balance de blanco con un valor adecuado para su uso con un flash electrónico.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td style="text-align: left;"><p>Describe una dirección URL. La dirección URL descrita por este proroperty es aquella en la que se pueden cargar imágenes u objetos, una vez que se han adquirido desde el dispositivo, de acuerdo con uno de los siguientes escenarios.</p>
<ul>
<li>Una aplicación WIA Lee esta propiedad y permite al usuario cargar imágenes automáticamente en la dirección URL.</li>
<li>Una aplicación establece la dirección URL y otros dispositivos (quioscos, etc.) usan esta propiedad.</li>
</ul>
<p>Microsoft Windows no carga imágenes por sí misma.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td style="text-align: left;"><p>Nombre del propietario (que es el usuario actual) del dispositivo. El dispositivo usa esta propiedad para rellenar el campo artista en cada imagen EXIF que captura.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td style="text-align: left;"><p>La notificación de copyright. El dispositivo usa esta propiedad para rellenar el campo copyright en cada imagen EXIF que captura.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 





---
description: Define valores que especifican las propiedades del paquete.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279165"
---
# <a name="packetpropertyguids-constants"></a>Constantes de PacketPropertyGuids

Define valores que especifican las propiedades del paquete. Tablet PCAPI usa identificadores únicos globales (GUID) para identificar las propiedades de los paquetes, que en COM son cadenas constantes.

En C++, puede tener acceso a estas constantes en el archivo de encabezado Msinkaut. h, que se encuentra en <systemdrive> el \\ Directorio: archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include Si instaló el SDK en la ubicación predeterminada. En C++, estas constantes son WCHARs, no BSTR. Conviértalos en BSTR antes de usarlo. Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).

En la tabla siguiente se enumeran los campos de identificador único global (GUID) de la propiedad de paquete disponible. Utilice estos GUID para especificar las propiedades que contiene el paquete al crear el contexto de la tableta. Para determinar el intervalo y la resolución de una propiedad, llame al método [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) . Las constantes de la tabla siguiente a partir de "STR \_ " son representaciones de cadena de las constantes binarias correspondientes que se muestran en la misma celda de tabla.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt> </dl></td>
<td style="text-align: left;">Coordenada x del espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Coordenada y del espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </dl></td>
<td style="text-align: left;">Coordenada y del espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt> </dl></td>
<td style="text-align: left;">La coordenada z o la distancia de la punta del lápiz desde la superficie de la tableta. El tipo de enumeración <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina la unidad de medida para esta propiedad.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </dl></td>
<td style="text-align: left;">Contiene uno o varios de los siguientes valores de marca:<br/>
<ul>
<li>El cursor toca la superficie de dibujo (valor = 1).</li>
<li>El cursor se invierte. Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (valor = 2).</li>
<li>No se usa (valor = 4).</li>
<li>Se presiona el botón de barril (valor = 8).</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">La hora a la que se generó el paquete.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </dl></td>
<td style="text-align: left;">La hora a la que se generó el paquete.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">La propiedad de paquete para identificar el paquete.<br/> Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Presión de la punta del lápiz perpendicular a la superficie de la tableta.<br/> Cuanto mayor sea la presión de la punta del lápiz, mayor será la tinta dibujada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Presión de la punta del lápiz a lo largo del plano de la superficie de la tableta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </dl></td>
<td style="text-align: left;">Presión sobre un botón sensible a la presión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Ángulo entre el plano y, z y el lápiz y el plano del eje y.<br/> Se aplica a un cursor de lápiz.<br/> El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la perpendicular.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Ángulo entre el plano x, z y el lápiz y el plano del eje x.<br/> Se aplica a un cursor de lápiz.<br/> El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o fuera del usuario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotación en el sentido de las agujas del reloj del cursor sobre el eje z a través de un intervalo circular completo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Ángulo entre el eje del lápiz y la superficie de la tableta.<br/> El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz es perpendicular a la superficie.<br/> Los valores son negativos cuando se invierte el lápiz.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotación en el sentido de las agujas del reloj del cursor sobre su propio eje.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">La propiedad de paquete que indica si la punta está por encima o por debajo de una línea horizontal que es perpendicular a la superficie de escritura.<br/>
<blockquote>
[!Note]<br />
Esto requiere un digitalizador 3D.
</blockquote>
<br/> El valor es positivo si la punta está por encima de la línea y es negativo si está por debajo de la línea. Por ejemplo, si mantiene el lápiz delante de usted y escribe en una pared imaginaria, el paso es positivo si la punta está por encima de una línea que se extiende desde usted a la pared.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Rotación en el sentido de las agujas del reloj del lápiz alrededor de su propio eje. <br/>
<blockquote>
[!Note]<br />
Esto requiere un digitalizador 3D.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Ángulo del lápiz situado a la izquierda o a la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.<br/>
<blockquote>
[!Note]<br />
Esto requiere un digitalizador 3D.
</blockquote>
<br/> Si mantiene el lápiz delante y lo escribe en un muro imaginario, el valor de guiñada cero indica que el lápiz es perpendicular a la pared. El valor es negativo si la punta está a la izquierda de la perpendicular y positiva si la punta está a la derecha de la perpendicular.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </dl></td>
<td style="text-align: left;">Ángulo del lápiz situado a la izquierda o a la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.<br/>
<blockquote>
[!Note]<br />
Esto requiere un digitalizador 3D.
</blockquote>
<br/> Si mantiene el lápiz delante y lo escribe en un muro imaginario, el valor de guiñada cero indica que el lápiz es perpendicular a la pared. El valor es negativo si la punta está a la izquierda de la perpendicular y positiva si la punta está a la derecha de la perpendicular.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </dl></td>
<td style="text-align: left;">Ancho del área de contacto en un digitalizador táctil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Alto del área de contacto en un digitalizador táctil.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </dl></td>
<td style="text-align: left;">El nivel de confianza en el que había contacto con el dedo en un digitalizador táctil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador de contacto del dispositivo para un paquete.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

> [!Note]  
> Todos los valores de paquetes procedentes del hardware de Tablet PC son enteros de tamaño de 32 bits.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Método GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Interfaz IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





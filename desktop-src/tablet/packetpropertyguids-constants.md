---
description: Define valores que especifican las propiedades del paquete.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: PacketPropertyGuids (Constantes) (Msdevut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b88a59d63bc8b45ea04e133f0d002fa86e35e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481081"
---
# <a name="packetpropertyguids-constants"></a>Constantes packetPropertyGuids

Define valores que especifican las propiedades del paquete. Tablet PCAPI usa identificadores únicos globales (GUID) para identificar las propiedades de paquete, que en COM son cadenas constantes.

En C++, puede acceder a estas constantes en el archivo de encabezado Msomisión.h, que se encuentra en el directorio : Archivos de programa SDK de <systemdrive> \\ Microsoft Windows \\ \\ \\ v6.0 \\ Include si instaló el SDK en la ubicación predeterminada. En C++, estas constantes son WCHARs, no BSTR. Conviéndolos en BSTR antes de usarlos. Para obtener más información sobre el tipo de datos BSTR, vea [Using the COM Library](using-the-com-library.md).

En la tabla siguiente se enumeran los campos de identificador único global (GUID) de la propiedad de paquete disponible. Use estos GUID para especificar qué propiedades contiene el paquete al crear el contexto de la tableta. Para determinar el intervalo y la resolución de una propiedad, llame al [**método GetPropertyMetrics.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) Las constantes de la tabla siguiente a partir de "STR" son representaciones de cadena de las constantes binarias correspondientes que se muestran \_ en la misma celda de tabla.




| Constante | Descripción | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | Coordenada X en el espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordenada Y en el espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordenada Y en el espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | Coordenada z o distancia de la punta del lápiz desde la superficie de la tableta. El <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>tipo de enumeración TabletPropertyMetricUnit</strong></a> determina la unidad de medida de esta propiedad.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Contiene uno o varios de los siguientes valores de marca:<br /><ul><li>El cursor está tocándose la superficie de dibujo (Valor = 1).</li><li>El cursor se invierte. Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (Valor = 2).</li><li>No se usa (valor = 4).</li><li>Se presiona el botón de botones (Valor = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Hora en que se generó el paquete.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Hora en que se generó el paquete.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | Propiedad de paquete para identificar el paquete.<br /> Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | Presión de la punta del lápiz a la superficie de la tableta.<br /> Mayor es la presión sobre la punta del lápiz, más lápiz se dibuja.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | Presión de la punta del lápiz a lo largo del plano de la superficie de la tableta.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | Presión en un botón sensible a la presión.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | Ángulo entre el plano y, z y el lápiz y el plano del eje Y.<br /> Se aplica a un cursor de lápiz.<br /> El valor es 0 cuando el lápiz está situado en la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la ventana.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | Ángulo entre el plano x, z y el lápiz y el plano del eje X.<br /> Se aplica a un cursor de lápiz.<br /> El valor es 0 cuando el lápiz está cerca de la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o lejos del usuario.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | Rotación en el sentido de las agujas del reloj del cursor sobre el eje Z a través de un intervalo circular completo.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | Ángulo entre el eje del lápiz y la superficie de la tableta.<br /> El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz está en paralelo a la superficie.<br /> Los valores son negativos cuando se invierte el lápiz.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | Rotación en el sentido de las agujas del reloj del cursor sobre su propio eje.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | Propiedad de paquete que indica si la propina está por encima o por debajo de una línea horizontal que está en la superficie de escritura.<br /><blockquote>[!Note]<br />Esto requiere un digitalizador 3D.</blockquote><br /> El valor es positivo si la propina está por encima de la línea y negativa si está por debajo de la línea. Por ejemplo, si mantiene el lápiz delante de usted y escribe en una pared imaginaria, el tono es positivo si la propina está por encima de una línea que se extiende desde usted hasta la pared.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | Rotación en el sentido de las agujas del reloj del lápiz alrededor de su propio eje. <br /><blockquote>[!Note]<br />Esto requiere un digitalizador 3D.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Ángulo del lápiz hacia la izquierda o hacia la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.<br /><blockquote>[!Note]<br />Esto requiere un digitalizador 3D.</blockquote><br /> Si mantiene el lápiz delante de usted y escribe en una pared imaginaria, cero yaw indica que el lápiz está en la pared. El valor es negativo si la propina está a la izquierda de y positiva si la propina está a la derecha de la esquina derecha.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Ángulo del lápiz hacia la izquierda o hacia la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.<br /><blockquote>[!Note]<br />Esto requiere un digitalizador 3D.</blockquote><br /> Si mantiene el lápiz delante de usted y escribe en una pared imaginaria, cero yaw indica que el lápiz está en la pared. El valor es negativo si la propina está a la izquierda de y positiva si la propina está a la derecha de la esquina derecha.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | Ancho del área de contacto en un digitalizador táctil.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | Alto del área de contacto en un digitalizador táctil.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | Nivel de confianza de que había contacto con los dedos en un digitalizador táctil.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | Identificador de contacto del dispositivo para un paquete.<br /> | 




## <a name="remarks"></a>Comentarios

> [!Note]  
> Todos los valores de paquetes procedentes del hardware de tableta son enteros de tamaño de 32 bits.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Método IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**GetPropertyMetrics (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**IInkTablet (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





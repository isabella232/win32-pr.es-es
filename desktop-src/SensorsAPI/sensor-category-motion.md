---
description: La \_ categoría de movimiento categoría de sensor \_ contiene sensores que proporcionan información relacionada con el movimiento físico.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666356"
---
# <a name="sensor_category_motion"></a>\_movimiento de categoría de sensor \_

La \_ categoría de movimiento categoría de sensor \_ contiene sensores que proporcionan información relacionada con el movimiento físico. Los acelerómetros miden la aceleración del sensor, incluida la aceleración Gravitational. Los detectores de movimiento, como la detección de movimiento humano en un sistema de seguridad, tienen sentido mover objetos. Cambios de Gyrometers Sense en la velocidad angular. Velocidad de medida de velocímetros.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Descripción                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Sensor \_ de TIPO \_ Accelerometer \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Acelerómetros de un eje.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Sensor \_ de Escriba \_ Accelerometer \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Acelerómetros de dos ejes.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Sensor \_ de TIPO \_ Accelerometer \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Acelerómetros de tres ejes.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Sensor \_ de Escriba \_ girómetro \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Gyrometers de un eje.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Sensor \_ de Escriba \_ girómetro \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Gyrometers de dos ejes.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Sensor \_ de Escriba \_ girómetro \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Gyrometers de tres ejes.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Sensor \_ de \_ \_ Detector de movimiento de tipo**</dt> <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Detectores de movimiento, como los que se usan en los sistemas de seguridad.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Sensor \_ de Escriba \_ velocímetro**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Sensores de velocidad de movimiento.<br/>                                   |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ GUID de \_ movimiento \_ :

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                                                                                               | Descripción                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Sensor \_ de Aceleración de tipos de datos \_ \_ \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje X, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Sensor \_ de Aceleración de tipos de datos \_ \_ \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje Y, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Sensor \_ de Aceleración de tipos de datos \_ \_ \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje Z, en *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ de \_Aceleración angular de tipo de datos \_ \_ \_ X \_ degrees \_ por \_ segundo \_ cuadrado**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Gyrometric: aceleración del eje x, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ de \_Aceleración angular de tipo de datos \_ \_ \_ Y \_ grados \_ por \_ segundo \_ cuadrado**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Aceleración del eje y de Gyrometric, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ de \_Aceleración angular de tipo de datos en \_ \_ \_ Z \_ degrees \_ por \_ segundo \_**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Gyrometric: aceleración del eje z, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Sensor \_ de \_Velocidad angular de tipo de datos \_ \_ \_ X \_ grados \_ por \_ segundo**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric velocidad del eje x, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Sensor \_ de \_ \_ Velocidad Y grados angulares de tipo de datos \_ \_ \_ \_ por \_ segundo**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Velocidad del eje y de Gyrometric, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Sensor \_ de \_Velocidad angular de tipo de datos: \_ \_ \_ \_ grados Z \_ por \_ segundo**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric velocidad del eje z, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Sensor \_ de \_Estado de \_ movimiento \_ de tipo de datos**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **VT \_ bool**<br/> **True** si se detecta movimiento; en caso contrario, **false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Sensor \_ de \_Medidores de velocidad de tipos de datos \_ \_ \_ por \_ segundo**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Velocidad en metros por segundo.<br/>                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 





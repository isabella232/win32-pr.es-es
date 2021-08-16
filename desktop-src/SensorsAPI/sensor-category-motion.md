---
description: La categoría SENSOR \_ CATEGORY \_ MOTION contiene sensores que proporcionan información relacionada con el movimiento físico.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d57c8406ad1344d696f63e574484943ea68a6654f63c3d7d38e904aaa44e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889493"
---
# <a name="sensor_category_motion"></a>MOVIMIENTO \_ DE CATEGORÍA DE \_ SENSOR

La categoría SENSOR \_ CATEGORY \_ MOTION contiene sensores que proporcionan información relacionada con el movimiento físico. Los acelerómetros miden la aceleración del sensor, incluida la aceleración retornal. Los detectores de movimiento, como la detección de movimiento humano en un sistema de seguridad, detectan objetos móviles. Los girómetros detectan los cambios en la velocidad angular. Los velocómetros miden la velocidad.

**Tipos de sensor definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Descripción                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**SENSOR \_ TYPE \_ ACCELEROMETER \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Acelerómetros de un eje.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**SENSOR \_ TYPE \_ ACCELEROMETER \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Acelerómetros de dos ejes.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**SENSOR \_ TIPO \_ ACCELEROMETER \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Acelerómetros de tres ejes.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**SENSOR \_ TYPE \_ GYROMETER \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Girómetros de un eje.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**SENSOR \_ TYPE \_ GYROMETER \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Girómetros de dos ejes.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**SENSOR \_ TYPE \_ GYROMETER \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Girómetros de tres ejes.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**SENSOR \_ DETECTOR \_ DE \_ MOVIMIENTO**</dt> DE <dt>TIPO {5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Detectores de movimiento, como los que se usan en los sistemas de seguridad.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**SENSOR \_ TIPO \_ SPEEDOMETER**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Sensores de velocidad de movimiento.<br/>                                   |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el GUID DE MOVIMIENTO \_ DEL TIPO DE DATOS \_ \_ \_ SENSOR:

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                                                                                               | Descripción                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**SENSOR \_ ACELERACIÓN \_ DE TIPOS DE DATOS X \_ \_ \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje X, *en g'* s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**SENSOR \_ ACELERACIÓN \_ DE TIPOS DE DATOS Y \_ \_ \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje Y, *en g'* s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**SENSOR \_ ACELERACIÓN \_ DE TIPOS DE DATOS Z \_ \_ \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Aceleración del eje Z, *en g'* s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE ANGULAR ACCELERATION X \_ \_ \_ \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Aceleración del eje X girmétrico, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE ANGULAR ACCELERATION Y \_ \_ \_ \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Aceleración del eje Y girmétrico, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE ANGULAR ACCELERATION Z \_ \_ \_ \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Aceleración del eje Z girmétrico, en grados por segundo al cuadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**SENSOR \_ TIPO \_ DE DATOS VELOCIDAD ANGULAR X GRADOS POR \_ \_ \_ \_ \_ \_ SEGUNDO**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Velocidad del eje X girmétrico, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**SENSOR \_ TIPO \_ DE DATOS VELOCIDAD ANGULAR Y GRADOS POR \_ \_ \_ \_ \_ \_ SEGUNDO**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Velocidad del eje y girmétrico, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**SENSOR \_ TIPO \_ DE DATOS ANGULAR VELOCITY Z \_ \_ \_ \_ DEGREES PER \_ \_ SECOND**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Velocidad del eje Z girmétrico, en grados por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ DE MOVIMIENTO DEL TIPO \_ \_ DE**</dt> <dt>DATOS (PID = 9)</dt> </dl>                                                                                                                      | **VT \_ BOOL**<br/> **TRUE si** se detecta movimiento; de lo contrario, **FALSE**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**SENSOR \_ MEDIDORES DE VELOCIDAD DE TIPO DE DATOS \_ \_ POR \_ \_ \_ SEGUNDO**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Velocidad en metros por segundo.<br/>                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 





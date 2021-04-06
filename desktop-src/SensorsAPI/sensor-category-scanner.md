---
description: La \_ categoría de analizador categoría de sensor \_ contiene sensores que proporcionan información obtenida mediante el análisis.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001034"
---
# <a name="sensor_category_scanner"></a>\_escáner de categoría de sensor \_

La \_ categoría de analizador categoría de sensor \_ contiene sensores que proporcionan información obtenida mediante el análisis.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descripción                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**Sensor \_ de ESCRIBIR \_ \_ escáner de código de barras**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Sensores que usan el examen óptico para leer códigos de barras.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**Sensor \_ de ESCRIBIR \_ \_ escáner RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Sensores de detección de ID. de radio.<br/>                 |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ GUID del \_ analizador \_ :

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                     | Descripción                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**Sensor \_ de Tipo de datos de \_ \_ \_ etiqueta RFID \_ 40 \_ bits**</dt> <dt>(PID = 2)</dt> </dl> | **VT \_ UI8**<br/> valor de etiqueta de identificador de frecuencia de radio de 40 bits.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 





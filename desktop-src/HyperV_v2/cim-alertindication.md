---
description: Una superclase concreta para las notificaciones de alerta de CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686518"
---
# <a name="cim_alertindication-class"></a>\_Clase AlertIndication de CIM

Una superclase concreta para las notificaciones de alerta de CIM. **CIM \_ AlertIndication** es un tipo especializado de clase de **\_ indicación CIM** que contiene información sobre la gravedad, la causa, las acciones recomendadas y otros datos para un evento del mundo real. Este evento y sus datos pueden modelarse o no en la jerarquía de clases CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ AlertIndication** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ AlertIndication** tiene estas propiedades.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**","**\_ AlertIndication CIM**.**OtherAlertingElementFormat**")
</dt> </dl>

Formato de la propiedad **AlertingManagedElement** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Una aplicación cliente CIM no reconoce el formato o lo interpreta de forma significativa.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

El formato se define mediante el valor de la propiedad OtherAlertingElementFormat.

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)


</dt> <dd>

El formato es CIMObjectPath, especificando una instancia en el esquema CIM.

</dd> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")
</dt> </dl>

La información de identificación de la entidad (es decir, la instancia) para la que se genera esta indicación. La propiedad contiene la ruta de acceso de una instancia, codificada como un parámetro de cadena, si la instancia se modela en el esquema CIM. Si no es una instancia de CIM, la propiedad contiene alguna cadena de identificación que nombra la entidad para la que se genera la alerta. Se da formato a la ruta de acceso o a la cadena de identificación según la propiedad AlertingElementFormat.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Tipo de evento ")
</dt> </dl>

La clasificación principal de la indicación.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

\- Distinta. La propiedad OtherAlertType de la indicación transmite su clasificación. El uso de "Other" en una enumeración es una convención estándar de CIM. Significa que la indicación actual no se ajusta a las categorías descritas por esta enumeración.

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Alerta de comunicaciones** (2)


</dt> <dd>

Una indicación de este tipo está asociada principalmente a los procedimientos y/o procesos necesarios para transmitir información de un punto a otro.

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de calidad de servicio** (3)


</dt> <dd>

Una indicación de este tipo está asociada principalmente a una degradación o errores en el rendimiento o la función de una entidad.

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Error de procesamiento** (4)


</dt> <dd>

Una indicación de este tipo está asociada principalmente a un error de software o de procesamiento.

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Alerta de dispositivo** (5)


</dt> <dd>

Una indicación de este tipo está asociada principalmente a un error de equipo o de hardware.

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Alerta de entorno** (6)


</dt> <dd>

Alerta de entorno. Una indicación de este tipo está asociada principalmente a una condición relacionada con un contenedor en el que reside el hardware, u otras consideraciones del entorno.

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Cambio de modelo** (7)


</dt> <dd>

La indicación trata los cambios en el modelo de información. Por ejemplo, puede insertar una indicación del ciclo de vida para transmitir el cambio de modelo específico que se va a notificar.

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Alerta de seguridad** (8)


</dt> <dd>

. Se ha asociado una indicación de este tipo.

</dd> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Texto adicional ")
</dt> </dl>

Breve descripción de la indicación.

</dd> <dt>

**Id. de evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Un valor específico de instrumentación o proveedor que describe el evento del mundo real subyacente representado por la indicación. La entidad de creación tiene en cuenta las indicaciones con el mismo valor **EventID** distinto de null para representar el mismo evento. La comparación de dos valores **EventID** solo se define para las indicaciones de alerta con valores idénticos no NULL de las propiedades **SystemCreateClassName**, **SystemName** y **providerName** .

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Fecha y hora que indica cuándo se detectó por primera vez el evento subyacente. Si se especifican estos valores y la entidad que crea no es capaz de proporcionar esta información, esta propiedad debe establecerse en **null**. Este valor se basa en la noción de la fecha y hora locales del objeto **CIM \_ ManageSystemElement** que generó la indicación.

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**","**CIM \_ AlertIndication**.**MessageArguments**")
</dt> </dl>

Mensaje con formato para la indicación de alerta. Se da formato a este mensaje mediante la combinación de uno o varios de los elementos dinámicos especificados en la propiedad **MessageArguments** y con los elementos estáticos que se identifican de forma única mediante la propiedad **MessageID** .

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Mensaje**","**CIM \_ AlertIndication**.**MessageID**")
</dt> </dl>

Una matriz que contiene el contenido dinámico del mensaje para la indicación de alerta.

</dd> <dt>

**Identificador**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Mensaje**","**CIM \_ AlertIndication**.**MessageArguments**")
</dt> </dl>

IDENTIFICADOR único del formato de mensaje, con el ámbito de la organización especificado en **OwningEntity**.

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")
</dt> </dl>

Define el formato de la propiedad **AlertingManagedElement** cuando la propiedad **AlertingElementFormat** se establece en "1" (otro); de lo contrario, este valor debe establecerse en **null**.

</dd> <dt>

**OtherAlertType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")
</dt> </dl>

Una cadena que describe el valor **AlertType** cuando la propiedad **AlertType** se establece en "1" (otro cambio de estado).

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR único de la organización a la que pertenece la definición del formato de la propiedad del **mensaje** . **OwningEntity** debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad de negocio o del cuerpo de los estándares que haya definido el formato de mensaje.

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Gravedad percibida ")
</dt> </dl>

La gravedad de la indicación de alerta desde el punto de vista del elemento que provocó la alerta.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Sigue el uso común.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

Indica que el valor de la gravedad se puede encontrar en la propiedad OtherSeverity.

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)


</dt> <dd>

Sigue el uso común.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)


</dt> <dd>

Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)


</dt> <dd>

Indica que la acción es necesaria, pero la situación no es seria en este momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

Indica que la acción es necesaria ahora.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)


</dt> <dd>

Indica que se ha producido un error, pero es demasiado tarde para tomar medidas correctivas.

</dd> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recommendation. itu \| X733. Causa probable: "," recommendation. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**","**\_ AlertIndication CIM**.**EventID**","**CIM \_ AlertIndication**.**EventTime**")
</dt> </dl>

La causa probable de la situación que produjo la indicación de la alerta.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

**Error de tarjeta/adaptador** (2)


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

**Error del subsistema de aplicación** (3)


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

**Ancho de banda reducido** (4)


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

**Error de establecimiento de conexión** (5)


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

**Error de protocolo de comunicaciones** (6)


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

**Error del subsistema de comunicaciones** (7)


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

**Error de configuración/personalización** (8)


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

**Congestión** (9)


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

**Datos dañados** (10)


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

Se **superó el límite de ciclos de CPU** (11)


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

**Error de conjunto** de


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

**Señal degradada** (13)


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

**Error de la interfaz DTE-DCE** (14)


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

Abertura de la **puerta del gabinete** (15)


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

**Funcionamiento incorrecto del equipo** (16)


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

**Vibración excesiva** (17)


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

**Error de formato de archivo** (18)


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

**Desencadenamiento detectado** (19)


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

**Inundación detectada** (20)


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

**Error de tramas** (21)


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

**Problema de HVAC** (22)


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

**Humedad inaceptable** (23)


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

**Error de dispositivo de e/s** (24)


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

**Error de dispositivo de entrada** (25)


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

**Error de LAN** (26)


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

**Pérdida no tóxica detectada** (27)


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

**Error de transmisión del nodo local** (28)


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

**Pérdida de fotograma** (29)


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

**Pérdida de señal** (30)


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

**Suministro de material agotado** (31)


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

**Problema del multiplexor** (32)


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

**Memoria insuficiente** (33)


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

**Error de dispositivo de salida** (34)


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

**Rendimiento degradado** (35)


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

**Problema de energía** (36)


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

**Presión inaceptable** (37)


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

**Problema del procesador (error interno de la máquina)** (38)


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

**Error de bombeo** (39)


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

**Tamaño de cola superado** (40)


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

**Error de recepción** (41)


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

**Error del receptor** (42)


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

**Error de transmisión de nodo remoto** (43)


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

**Recursos a la capacidad o en proximidad** (44)


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

**Tiempo de respuesta excesivo** (45)


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

**Tasa de retransmisión excesiva** (46)


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

**Error de software** (47)


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

**Programa de software finalizado** de manera anómala (48)


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

**Error del programa de software (resultados incorrectos)** (49)


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

**Problema de capacidad de almacenamiento** (50)


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

**Temperatura inaceptable** (51)


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

**Umbral superado** (52)


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

**Problema de sincronización** (53)


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

**Pérdida tóxica detectada** (54)


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

**Error de transmisión** (55)


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

**Error de transmisor** (56)


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

**Recurso subyacente no disponible** (57)


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

**Discrepancia de versiones** (58)


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

**Alerta anterior desactivada** (59)


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

**Error de intentos de inicio de sesión** (60)


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

**Virus de software detectado** (61)


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

**Seguridad de hardware infringida** (62)


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

**Denegación de servicio detectada** (63)


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

**No coincide la credencial de seguridad** (64)


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

**Acceso no autorizado** (65)


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

**Alarma recibida** (66)


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

**Pérdida de puntero** (67)


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

Error de **coincidencia de carga** (68)


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

**Error de transmisión** (69)


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

**Tasa de errores excesiva** (70)


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

**Problema de seguimiento** (71)


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

**Elemento no disponible** (72)


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

**Falta el elemento** (73)


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

**Pérdida de varios fotogramas** (74)


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

**Error de canal de difusión** (75)


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

Se **recibió un mensaje no válido** (76)


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

**Error de enrutamiento** (77)


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

**Error de backplane** (78)


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

**Duplicación de identificadores** (79)


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

**Error de ruta de protección** (80)


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

**Pérdida o desigualdad de sincronización** (81)


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

**Problema de terminal** (82)


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

**Error de reloj en tiempo real** (83)


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

**Error de antena** (84)


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

**Error de carga** de la batería (85)


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

**Error de disco** (86)


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

**Error de salto de frecuencia** (87)


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

**Pérdida de redundancia** (88)


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

**Error** de la fuente de alimentación (89)


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

**Problema de calidad** de la señal (90)


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

**Descarga** de la batería (91)


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

**Error de batería** (92)


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

**Problema de alimentación comercial** (93)


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

**Error de ventilador** (94)


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

**Error del motor** (95)


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

**Error del sensor** (96)


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

**Error de fusible** (97)


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

**Error del generador** (98)


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

**Batería baja** (99)


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

**Combustible bajo** (100)


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

**Bajo agua** (101)


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

**Gas explosivo** (102)


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

**Viento alto** (103)


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

**Acumulación de hielo** (104)


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

**Humo** (105)


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

**No coincide la memoria** (106)


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

**Ciclos de CPU agotados** (107)


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

**Problema del entorno de software** (108)


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

**Error de descarga de software** (109)


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

**Elemento reinicializado** (110)


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

**Tiempo de espera** (111)


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

**Problemas de registro** (112)


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

**Pérdida detectada** (113)


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

**Error del mecanismo de protección** (114)


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

**Error de protección de recursos** (115)


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

Incoherencia de la **base de datos** (116)


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

**Error de autenticación** (117)


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

**Infracción de la confidencialidad** (118)


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

**Manipulación de cables** (119)


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

**Información retrasada** (120)


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

**Información duplicada** (121)


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

**Falta información** (122)


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

**Modificación** de la información (123)


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

**Información fuera de secuencia** (124)


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

**Clave expirada** (125)


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

**Error sin repudio** (126)


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

**Actividad fuera de horas** (127)


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

**Fuera de servicio** (128)


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

**Error de procedimiento** (129)


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

**Información inesperada** (130)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")
</dt> </dl>

Información adicional relacionada con la propiedad **ProbableCause** .

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre del proveedor que generó la indicación.

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Acciones de reparación propuestas ")
</dt> </dl>

Descripciones de forma libre de las acciones recomendadas que se deben realizar para resolver la causa de la notificación.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Valor de **CreationClassName** del sistema de ámbito para el proveedor que generó la indicación.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre del sistema de ámbito del proveedor que generó la indicación.

</dd> <dt>

**Tendencias**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. TrendIndication")
</dt> </dl>

Proporciona información sobre tendencias: tendencia hacia arriba, hacia abajo o sin cambios.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (1)


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

**Tendencia hacia arriba** (2)


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

**Tendencia hacia abajo** (3)


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

**Sin cambios** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_PROCESSINDICATION CIM**](cim-processindication.md)
</dt> </dl>

 


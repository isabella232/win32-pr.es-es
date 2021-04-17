---
description: Permite iniciar la especificación de la recopilación de métricas puntuales y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Método ControlSampleTimes de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687650"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>Método ControlSampleTimes de la \_ clase MetricService de CIM

Permite iniciar la especificación de la recopilación de métricas puntuales y especificar el tiempo de intervalo de muestra preferido para la recopilación periódica de datos.

Cada vez que se inicia el muestreo de métricas adicionales, se puede usar la configuración especificada por este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartSampleTime* \[ de\]
</dt> <dd>

Un momento dado en el que se va a iniciar el muestreo de las métricas.

Un valor de 99990101000000.000000 + 000 indicará que el muestreo debe iniciarse en la próxima vez que se sincronice con la hora completa. El muestreo se sincroniza con la hora completa si los segundos desde el intervalo de ejemplo de módulo medianoche en segundos es igual a 0.

</dd> <dt>

*PreferredSampleInterval* \[ de\]
</dt> <dd>

Tiempo de intervalo de muestra preferido. Para obtener métricas que se pueden correlacionar, se recomienda elegir el intervalo de ejemplo de modo que el tiempo de intervalo de ejemplo de módulo 3600 en segundos sea igual a 0.

Es responsabilidad de la implementación del servicio de métricas de CIM decidir si se respeta el tiempo de intervalo de muestra solicitado.

El cliente CIM puede comprobar si los proveedores de métricas respetan el tiempo de intervalo de muestra solicitado recuperando instancias de BaseMetricDefinition relacionadas y comprobando el contenido de la [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md).**Propiedad SampleInterval** .

</dd> <dt>

*RestartGathering* \[ de\]
</dt> <dd>

**True** para solicitar que la recopilación de todas las métricas asociadas al servicio de métrica se reinicie con esta llamada al método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

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

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 





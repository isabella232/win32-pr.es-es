---
description: Proporciona la capacidad de devolver una lista filtrada de \_ las instancias de BaseMetricValue de CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Método GetMetricValues de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667568"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Método GetMetricValues de la \_ clase MetricService de CIM

Proporciona la capacidad de devolver una lista filtrada de las instancias de [**\_ BaseMetricValue de CIM**](cim-basemetricvalue.md) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Definición* \[ de de\]
</dt> <dd>

Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se devolverán las métricas.

</dd> <dt>

*Intervalo* \[ de de\]
</dt> <dd>

Identifica cómo se seleccionan las instancias. El algoritmo para ordenar instancias de valor es específico de la definición de métricas.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Mínimo** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del proveedor** (32768... 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Recuento* \[ de\]
</dt> <dd>

Identifica el número máximo de instancias que debe devolver el método.

</dd> <dt>

*Valores* \[ de enuncia\]
</dt> <dd>

Tras la finalización correcta del método, contiene referencias a instancias [**de \_ BaseMetricValue de CIM**](cim-basemetricvalue.md), filtradas según los valores de los parámetros de entrada.

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

 

 





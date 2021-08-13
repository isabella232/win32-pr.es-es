---
description: Se usa para controlar la colección de métricas de un elemento o elementos administrados.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Método ControlMetrics de la Msvm_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 051a08f261432c817bc0e56cab323c56cd11935c1541c40357b6b151a14f4074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645864"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Método ControlMetrics de la clase \_ Msvm MetricService

Se usa para controlar la colección de métricas de un elemento o elementos administrados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Asunto* \[ En\]
</dt> <dd>

Instancia [**de \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que identifica los elementos administrados para los que se recopilarán las métricas. Si este parámetro es **Null,** se recopilarán las métricas de todos los elementos administrados asociados al parámetro *Definition.*

</dd> <dt>

*Definición* \[ En\]
</dt> <dd>

Instancia [**de \_ BaseMetricDefinition de Msvm**](msvm-basemetricdefinition.md) que especifica qué métricas se recopilarán. Si este parámetro es **Null,** se recopilarán las métricas de todas las definiciones asociadas al elemento administrado identificado por el *parámetro Subject.*

</dd> <dt>

*MetricCollectionEnabled* \[ En\]
</dt> <dd>

Especifica la operación que se realizará en la colección de métricas. Debe ser uno de los siguientes valores.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** (2)


</dt> <dd>

Habilite la recopilación de métricas.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (3)


</dt> <dd>

Deshabilite la recopilación de métricas.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecimiento** (4)


</dt> <dd>

Restablezca los valores de las métricas.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Este método producirá un error en las siguientes instancias:

-   Los *parámetros Subject* y *Definition* son **null.**
-   Los *parámetros Subject* y *Definition* no son NULL y no hay una instancia de [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md) que asocie las dos instancias.
-   El *parámetro Definition* es una referencia a una instancia de [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que no está asociada a [**Msvm \_ MetricService**](msvm-metricservice.md) a través de [**Msvm \_ ServiceAffectsElement.**](msvm-serviceaffectselement.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 


---
description: Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Método ControlMetrics de la clase Msvm_MetricService
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
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667838"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Método ControlMetrics de la \_ clase MetricService de MSVM

Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.

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

*Asunto* \[ de\]
</dt> <dd>

Instancia [**de \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que identifica los elementos administrados para los que se recopilarán las métricas. Si este parámetro es **null**, se recopilarán las métricas de todos los elementos administrados asociados al parámetro de *definición* .

</dd> <dt>

*Definición* \[ de de\]
</dt> <dd>

Una instancia de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que especifica qué métricas se van a recopilar. Si este parámetro es **null**, se recopilarán las métricas de todas las definiciones asociadas al elemento administrado identificado por el parámetro de *asunto* .

</dd> <dt>

*MetricCollectionEnabled* \[ de\]
</dt> <dd>

Especifica la operación que se va a realizar en la colección de métricas. Debe ser uno de los valores siguientes.

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

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (4)


</dt> <dd>

Restablezca los valores de las métricas.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


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

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Este método producirá un error en las instancias siguientes:

-   Los parámetros de *asunto* y *definición* son **null**.
-   Los parámetros de *asunto* y *definición* son no **null** y no hay una instancia de [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) que asocie las dos instancias.
-   El parámetro *Definition* es una referencia a una instancia de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que no está asociada con [**MSVM \_ MetricService**](msvm-metricservice.md) a [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 


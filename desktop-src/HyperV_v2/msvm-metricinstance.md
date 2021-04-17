---
description: Representa una asociación de objetos de valor de métrica con sus definiciones de métricas.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687478"
---
# <a name="msvm_metricinstance-class"></a>MSVM \_ MetricInstance (clase)

Representa una asociación de objetos de valor de métrica con sus definiciones de métricas. Esta asociación asocia una instancia de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) a su [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md).

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ MetricInstance** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ MetricInstance** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: * * * * CIM \_ ManagedElement * * * *
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Una referencia a una instancia de la clase [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que representa las definiciones de las métricas.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: * * * * CIM \_ ManagedElement * * * *
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) que representa las métricas que dependen del **antecedente**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 





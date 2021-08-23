---
description: Define la asociación entre un elemento BaseMetricDefinition de Msvm y un elemento ManagedElement de \_ CIM para definir \_ métricas para el último. ManagedElement proporciona contexto a la definición de métricas, por lo que la definición depende del elemento .
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c6da093c5f902657c51285e124593e0bf44a9be0bf32ed87a55d3349cbfba92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521605"
---
# <a name="msvm_metricdefforme-class"></a>Clase Msvm \_ MetricDefForME

Define la asociación entre [**un elemento \_ BaseMetricDefinition de Msvm**](msvm-basemetricdefinition.md) y un elemento [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir las métricas de este último. ManagedElement proporciona contexto a la definición de métricas, por lo que la definición depende del elemento .

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ MetricDefForME** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ MetricDefForME** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de la clase [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) de CIM que representa el elemento administrado que puede tener aplicadas métricas del tipo definido por **Dependent.** Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Cim BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de la clase [**\_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) de CIM que representa la definición de métrica que el **antecedente** puede haber aplicado a ella. Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**MetricCollectionEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la métrica definida por **Dependent** se recopila para **el antecedente.** Este será uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                               | Significado                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>2</dt> </dl>                                         | La métrica se está recopilando.<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>3</dt> </dl>                                     | La métrica no se está recopilando.<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Reservado**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**PartiallyEnabled**</dt> <dt>32768</dt> </dl> | La métrica se recopila para algunos dispositivos, pero no todos.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


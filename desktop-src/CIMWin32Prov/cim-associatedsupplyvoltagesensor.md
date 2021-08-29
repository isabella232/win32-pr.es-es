---
description: Asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyVoltageSensor clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 65ed830a1bb0649ac2a1e934a6de958d16706ae5a39f544c42f91369d16c3f48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218935"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a>Cim \_ AssociatedSupplyVoltageSensor (clase)

La **clase \_ Cim AssociatedSupplyVoltageSensor** asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a>Miembros

La **clase \_ AssociatedSupplyVoltageSensor de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AssociatedSupplyVoltageSensor de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VoltageSensor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Cim [**\_ VoltageSensor que**](cim-voltagesensor.md) describe el sensor de voltaje.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PowerSupply**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Cim [**\_ PowerSupply**](cim-powersupply.md) que describe la fuente de alimentación asociada al sensor de voltaje.

</dd> <dt>

**MonitoringRange**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el intervalo de voltaje de entrada de la fuente de alimentación medido por el sensor asociado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervalo 1** (2)


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervalo 2** (3)


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Intervalo 1 y 2** (4)


</dt> <dd>

Intervalo 1 y 2

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AssociatedSupplyVoltageSensor de CIM** se deriva de CIM [**\_ AssociatedSensor.**](cim-associatedsensor.md)

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> </dl>

 


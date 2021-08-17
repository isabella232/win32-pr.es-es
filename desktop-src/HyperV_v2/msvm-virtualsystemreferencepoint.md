---
description: Representa un punto de referencia para un sistema virtual.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Msvm_VirtualSystemReferencePoint clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d5faa54edc18aa025445a34574aa912a39a1322c91f4d1a7e94c740a493f2b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963515"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a>Clase VirtualSystemReferencePoint de Msvm \_

Representa un punto de referencia para un sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualSystemReferencePoint de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VirtualSystemReferencePoint de Msvm** tiene estas propiedades.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nivel de coherencia del punto de referencia.

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente con la** aplicación (1)


</dt> <dd>

El punto de referencia indica un momento dado en el que el sistema virtual estaba en estado coherente con la aplicación.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherente con bloqueos** (2)


</dt> <dd>

El punto de referencia indica un momento dado en el tiempo en el que el sistema virtual estaba en estado coherente con los bloqueos.

</dd> </dl>

</dd> <dt>

**HasAssociatedData**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Se establece **en true** si el punto de referencia tiene datos asociados. Esto solo es válido para los puntos de referencia basados en registros. Para los puntos de referencia basados en RCT, **HasAssociatedData** se establece en **false.** Para los puntos de referencia basados en registros, una vez descartado el registro **HasAssociatedData se** convierte en **false.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificación única de un objeto de punto de referencia.

</dd> <dt>

**ReferencePointType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica el tipo del punto de referencia.

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en registros** (1)


</dt> <dd>

Seguimiento de registros de réplica de Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basado en RCT** (2)


</dt> <dd>

Basado en la resistencia Change Tracking discos virtuales.

</dd> </dl>

</dd> <dt>

**ResilientChangeTrackingIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de los ID de RCT correspondientes a los discos virtuales de la máquina virtual en el momento en que se creó este punto de referencia. Este campo solo es válido para los puntos de referencia basados en RCT.

</dd> <dt>

**VirtualDiskIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de los IDs de instancia de WMI correspondientes a los discos virtuales de la máquina virtual en el momento en que se creó este punto de referencia. Estos discos virtuales tienen los ID de RCT asociados.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Nombre del sistema de [**\_ equipos CIM**](cim-computersystem.md) al que pertenece este punto de referencia

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento administrado de CIM \_**](cim-managedelement.md)
</dt> </dl>

 


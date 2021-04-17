---
description: Se usa en el método GetSummaryInformation de la \_ clase MSVM VirtualSystemManagementService para recuperar rápidamente información común relacionada con un sistema virtual o una instantánea.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652513"
---
# <a name="msvm_summaryinformationbase-class"></a>MSVM \_ SummaryInformationBase (clase)

Se usa en el método [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rápidamente información común relacionada con un sistema virtual o una instantánea.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SummaryInformationBase** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SummaryInformationBase** tiene estas propiedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que se creó el sistema virtual o la instantánea.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement. ElementName")
</dt> </dl>

Nombre descriptivo del sistema virtual o de la instantánea.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del sistema virtual o de la instantánea.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el host permite o no conexiones en modo mejorado y, si se permiten, si están disponibles para la máquina virtual.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Permitido y disponible** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**No permitido** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Permitido pero no disponible** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado de mantenimiento actual del sistema virtual. Esta propiedad no es válida para las instancias de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representan una instantánea del sistema virtual.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo que hospeda esta máquina virtual.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement. InstanceId"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID es una propiedad opcional que se puede usar para identificar de forma opaca y única una instancia de esta clase dentro del ámbito del espacio de nombres de la instancia. Varias subclases de esta clase pueden invalidar esta propiedad para que sea necesaria, o una clave. Estas subclases también pueden modificar los algoritmos preferidos para garantizar la exclusividad que se definen a continuación.

Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido":

<OrgID>:<LocalID>

Donde <OrgID> y <LocalID> se separan con dos puntos (:), donde <OrgID> debe incluir un nombre de propiedad intelectual, marca registrada o de otro tipo, que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un identificador registrado asignado a la entidad empresarial por una entidad global reconocida. (Este requisito es similar al <Schema Name> \_ <Class Name> estructura de los nombres de clase de esquema.) Además, para garantizar la exclusividad, <OrgID> no debe contener un signo de dos puntos (:). Al utilizar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre <OrgID> y <LocalID> .

<LocalID> la entidad de negocio elige y no se debe reutilizar para identificar distintos elementos subyacentes (del mundo real). Si no es NULL y no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs generado por este u otros proveedores para el espacio de nombres de esta instancia.

Si no se establece en null para las instancias definidas por DMTF, se debe usar el algoritmo "preferido" con el <OrgID> establecido en CIM.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único del sistema virtual o de la instantánea.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notas asociadas al sistema virtual o a la instantánea.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número total de procesadores virtuales asignados al sistema virtual o a la instantánea.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Estado actual del elemento.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro"). Esta propiedad debe establecerse en NULL cuando **EnabledState** es cualquier valor distinto de 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadenas que describen los distintos valores de la matriz **OperationalStatus** .

</dd> <dt>

**Actividad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de tiempo transcurrido desde el último arranque del sistema virtual. Esta propiedad no es válida para las instancias de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representan una instantánea del sistema virtual.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión del sistema virtual en un formato de "Major. minor"; por ejemplo, "2,0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadenas que muestran los nombres descriptivos de los conmutadores virtuales a los que está conectada la máquina virtual.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subtipo del sistema virtual.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: SubType: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: SubType: 2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Vista CIM**](cim-view.md)
</dt> </dl>

 


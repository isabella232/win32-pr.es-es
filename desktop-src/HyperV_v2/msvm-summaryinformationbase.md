---
description: Se usa en el método GetSummaryInformation de la clase Msvm VirtualSystemManagementService para recuperar rápidamente información común relacionada con un sistema \_ virtual o una instantánea.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase clase
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
ms.openlocfilehash: d131a2630c0c64e4b4b6bcec371eb901665c989948a1db510b47a41d9159f06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950104"
---
# <a name="msvm_summaryinformationbase-class"></a>Clase Msvm \_ SummaryInformationBase

Se usa en [**el método GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rápidamente información común relacionada con un sistema virtual o una instantánea.

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

La **clase Msvm \_ SummaryInformationBase** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ SummaryInformationBase** tiene estas propiedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se creó el sistema virtual o la instantánea.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.ElementName")
</dt> </dl>

Nombre descriptivo del sistema virtual o la instantánea.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del sistema virtual o la instantánea.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el host permite o no las conexiones en modo mejorado y, si se permiten, si están disponibles para la máquina virtual.

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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de mantenimiento actual del sistema virtual. Esta propiedad no es válida para las instancias de [**Msvm \_ SummaryInformation que**](msvm-summaryinformation.md) representan una instantánea del sistema virtual.

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

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID es una propiedad opcional que se puede usar para identificar de forma opaca e inequívoca una instancia de esta clase dentro del ámbito del espacio de nombres de creación de instancias. Varias subclases de esta clase pueden invalidar esta propiedad para que sea necesaria o una clave. Estas subclases también pueden modificar los algoritmos preferidos para garantizar la unidad que se define a continuación.

Para garantizar la unidad dentro de NameSpace, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido":

<OrgID>:<LocalID>

Donde y están separados por dos puntos (:) y donde deben incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que crea o define instanceID o que es un identificador registrado asignado a la entidad empresarial por una autoridad <OrgID> <LocalID> global <OrgID> reconocida. (Este requisito es similar al <Schema Name> \_ <Class Name> estructura de los nombres de clase de esquema). Además, para garantizar la unidad, <OrgID> no debe contener dos puntos (:). Cuando se usa este algoritmo, los primeros dos puntos que aparecen en InstanceID deben aparecer entre <OrgID> y <LocalID> .

<LocalID> la elige la entidad empresarial y no debe reutilizarse para identificar diferentes elementos subyacentes (reales). Si no es NULL y no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceID generado por este u otros proveedores para nameSpace de esta instancia.

Si no se establece en NULL para las instancias definidas por DMTF, se debe usar el algoritmo "preferido" <OrgID> con el establecido en CIM.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único del sistema virtual o la instantánea.

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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de procesadores virtuales asignados al sistema virtual o instantánea.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Estado actual del elemento.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la **propiedad EnabledState** se establece en 1 ("Other"). Esta propiedad debe establecerse en null cuando **EnabledState** es cualquier valor distinto de 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Cadenas que describen los distintos **valores de matriz OperationalStatus.**

</dd> <dt>

**Uptime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de tiempo desde que se arranque por última vez el sistema virtual. Esta propiedad no es válida para las instancias de [**Msvm \_ SummaryInformation que**](msvm-summaryinformation.md) representan una instantánea del sistema virtual.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión del sistema virtual en un formato de "major.minor"; por ejemplo, "2.0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Cadenas que enumera los nombres descriptivos de los conmutadores virtuales a los que está conectada la máquina virtual.

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

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Vista \_ CIM**](cim-view.md)
</dt> </dl>

 


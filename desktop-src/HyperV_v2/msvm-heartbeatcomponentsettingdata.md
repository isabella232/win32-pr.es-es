---
description: Representa el estado configurado del servicio de latido.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Msvm_HeartbeatComponentSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8a542713c9e7e3fd1fa5827b7ad9dbce1a1c7ce76da788b7f9838a5f155d88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789845"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a>Clase Msvm \_ HeartbeatComponentSettingData

Representa el estado configurado del servicio de latido.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ HeartbeatComponentSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ HeartbeatComponentSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en **Null.**

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la dirección de este recurso en el contexto del elemento primario. Las **propiedades** / **AddressOnParent primarias** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador. Por ejemplo, si el elemento primario es un controlador PCI, esta propiedad especificaría la ranura PCI de este dispositivo secundario. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en **Null.**

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidades de asignación usadas por las **propiedades Reservation** **y Limit.** Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "Componentes de integración".

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se asigna automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **True.**

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se desasigna automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **True.**

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de la clase [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "Heartbeat".

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El elemento al que está conectado este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en **Null.**

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la visibilidad de los consumidores sobre el recurso asignado. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en 3 (virtualizado).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Datos de configuración del servicio de latidos de Microsoft".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Heartbeat". Al cambiar esta propiedad, se cambiará **la propiedad ElementName** del derivado [**\_ logicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) asociado.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitados y deshabilitados de un elemento.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorThreshold**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad siempre se establece en 2 (habilitado).

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Expone una asignación específica al host o a los recursos subyacentes. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en **Null.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData".*

</dd> <dt>

**Intervalo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo, en milisegundos, entre los intentos de ping. Siempre se establece en 2000.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Latency**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Latencia máxima esperada, en milisegundos, entre un ping de solicitud y una respuesta antes de que una solicitud determinada se considere descartada. Esta propiedad siempre se establece en 1000.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Límite superior o cantidad máxima de recursos que se concederán para esta asignación. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en 1.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **Null.**

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y la **propiedad ResourceType** tiene el valor 1 (Other). Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "Componente de latido de Microsoft".

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **Null.**

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asigna el recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de recursos que se garantiza que estará disponible para esta asignación. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en 1.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subtipo específico de implementación para este recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **Null.**

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación. Esta propiedad se hereda de la clase [**\_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) de CIM y siempre se establece en 1 (Other).

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de recursos que se presentan al consumidor. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en 1.

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las unidades usadas por la **propiedad VirtualQuantity.** Por ejemplo, si ResourceType=Processor, el valor de la propiedad **VirtualQuantityUnits** se puede establecer en "count", lo que indica que el valor de la propiedad **VirtualQuantity** se expresa como un recuento. Si ResourceType=Memory, el valor de la propiedad **VirtualQuantityUnits** se puede establecer en "bytes 10^3", lo que indica que el valor de la propiedad \* **VirtualQuantity** se expresa en kilobytes. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "count".

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad relativa para esta asignación en relación con otras asignaciones del mismo grupo de recursos. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en 0.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm HeartbeatComponentSettingData** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[**Msvm \_ HeartbeatComponentSettingData**](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 


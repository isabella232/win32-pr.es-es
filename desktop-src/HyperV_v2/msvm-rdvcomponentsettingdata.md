---
description: Representa el estado configurado del componente de virtualización de Escritorio remoto (RDV). El estado predeterminado es habilitado.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Msvm_RdvComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910145"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a>MSVM \_ RdvComponentSettingData (clase)

Representa el estado configurado del componente de virtualización de Escritorio remoto (RDV). El estado predeterminado es habilitado.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
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
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ RdvComponentSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ RdvComponentSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la dirección de este recurso en el contexto del elemento primario. Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidad de asignación utilizada por las propiedades de **límite** y **reserva** . Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se asignará automáticamente. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se desasignará automáticamente. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo al que está conectado este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visibilidad del consumidor en el recurso asignado. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 3 (virtualizado).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)). Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. Los valores válidos son 2 (habilitado) y 3 (deshabilitado). El valor predeterminado es 2 (habilitado). Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solo se puede asignar un recurso de host a cada dispositivo del conmutador virtual, por lo que solo se puede establecer el primer elemento de esta matriz. En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de recursos de host correspondientes que puede consumir el conmutador virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro). Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y no se utiliza.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asignó este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de recursos reservados para su uso por el conmutador virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de la implementación para este recurso. Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que esta configuración de asignación representa. Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 33 (conexión Ethernet).

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número total de puertos en el conmutador virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la unidad de medida para la propiedad **VirtualQuantity** . El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un entero que define el peso de cada conmutador virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Intervalo: 0 1000

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


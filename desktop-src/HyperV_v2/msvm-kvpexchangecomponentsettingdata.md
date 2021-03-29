---
description: Representa el estado configurado del servicio de intercambio de pares clave-valor.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Msvm_KvpExchangeComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667174"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a>MSVM \_ KvpExchangeComponentSettingData (clase)

Representa el estado configurado del servicio de intercambio de pares clave-valor.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ KvpExchangeComponentSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ KvpExchangeComponentSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.

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

Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** . Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

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

Indica si el recurso se anulará la asignación automáticamente. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento al que está conectado este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La visibilidad de los consumidores del recurso asignado. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).



| Value                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>3</dt> </dl> | Virtualizado<br/> |



 

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DisableHostKVPItems**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Esta propiedad deshabilita el host de populatinghost automáticamente el nombre y la información del sistema operativo dentro del invitado.

> [!Note]  
> Esta propiedad se agregó en la versión 1703 de Windows 10.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado habilitado del elemento.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExchangeItems**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")
</dt> </dl>

Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incrustadas que representan los pares clave-valor.

</dd> <dt>

**HostOnlyItems**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")
</dt> </dl>

Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) que contiene los pares clave-valor que se almacenan en el archivo de configuración, pero no se intercambian con el sistema operativo invitado. Esto permite que las aplicaciones almacenen datos específicos de la máquina virtual que no es necesario que sean visibles para el sistema operativo invitado. Los elementos tienen el mismo formato que los elementos de la propiedad **HostExchangeItems** , excepto que la propiedad **source** de la instancia de **MSVM \_ KvpExchangeDataItem** se establece en 4. Cada archivo de configuración está limitado a 128 pares clave-valor, donde cada campo de valor puede tener un tamaño de hasta 16 KB y el campo de clave puede tener hasta 512 bytes.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Expone una asignación específica para hospedar o los recursos subyacentes. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.

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

El límite superior o la cantidad máxima de recursos que se concederán para esta asignación. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro). Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de recursos que se garantiza que estarán disponibles para esta asignación. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que esta configuración de asignación representa. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).



| Value                                                                        | Significado          |
|------------------------------------------------------------------------------|------------------|
| <dl> <dt>1</dt> </dl> | Otros<br/> |



 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de recursos que se presentan al consumidor. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la unidad de medida para esta asignación de recursos. El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ KvpExchangeComponentSettingData** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 


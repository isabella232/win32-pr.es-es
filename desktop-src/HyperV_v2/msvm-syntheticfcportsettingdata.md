---
description: Representa el estado configurado de un puerto Canal de fibra sintético.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Msvm_SyntheticFcPortSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a31d8e927373bab0d7bcbc18156e2a6551b32db6393480fb12de4236631040d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810864"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a>Clase Msvm \_ SyntheticFcPortSettingData

Representa el estado configurado de un puerto Canal de fibra sintético.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ SyntheticFcPortSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ SyntheticFcPortSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la dirección de este recurso en el contexto del elemento primario. Las **propiedades Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidad de asignación utilizada por las propiedades **Reservation** **y Limit.** Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se asignará automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se desasignará automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChapEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica que este puerto se ha configurado con un secreto compartido mediante DH-CHAP, lo que permite que el tejido de Canal de fibra autentique que esta máquina virtual puede usar legítimamente los nombres de todo el mundo asignados a este puerto.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dispositivo al que está conectado este recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visibilidad del consumidor para el recurso asignado. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)). Al cambiar esta propiedad, se cambiará el nombre del elemento derivado del dispositivo lógico asociado.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solo se puede asignar un recurso host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz. Para los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de recursos de host correspondientes que puede consumir la máquina virtual. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**ResourceType**](msvm-processorsettingdata.md) tiene el valor 1(Other). Esta propiedad se hereda de [**\_ ResourceAllocationSettingData de CIM,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)pero no se usa.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asignó este recurso. En el caso de las instancias asociadas a una máquina virtual, será "Microsoft:*datos* \\ *específicos del dispositivo GUID".* En el caso de las instancias que definen la configuración potencial de una máquina virtual, será "Microsoft:Definition GUID Type", donde Type puede ser \\  \\ "Maximum", "Minimum", "Default" o "Increment".  Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de recursos reservados para su uso por la máquina virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData de CIM,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)pero no se usa.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir distintos modelos del mismo tipo de recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)



| Valor                                                                                                                                                                                          | Significado                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <dt>**FC HBA**</dt> <dt>7</dt> </dl> | Canal de fibra<br/> |



 

</dd> <dt>

**SecondaryWWNN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre del nodo de todo el mundo del puerto HBA virtual que se usará durante la migración en vivo de la máquina virtual.

</dd> <dt>

**SecondaryWWPN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre de puerto de todo el mundo del puerto HBA virtual que se usará durante la migración en vivo de la máquina virtual.

</dd> <dt>

**VirtualPortWWNN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre del nodo de todo el mundo del puerto HBA virtual.

</dd> <dt>

**VirtualPortWWPN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el nombre de puerto de todo el mundo del puerto HBA virtual.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la cantidad de recursos presentados al consumidor. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la unidad de medida para la **propiedad VirtualQuantity.** El valor de esta propiedad debe ser un valor legal del calificador Unidades de programación tal como se define en el anexo C.1 de DSP0004 V2.5 o posterior. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de cadenas de identificadores de este recurso presentada al sistema operativo de la máquina virtual. Los índices y valores por índice se definen por recurso (es decir, para cada valor **resourceType** enumerado). Esta propiedad no se usa

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entero que define el peso relativo de cada procesador de máquina virtual. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData de CIM,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)pero no se usa.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


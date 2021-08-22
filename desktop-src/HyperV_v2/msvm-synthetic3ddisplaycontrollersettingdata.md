---
description: Representa la configuración de un controlador de pantalla 3D sintético para una máquina virtual.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Msvm_Synthetic3DDisplayControllerSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f8b9aa97aa57089cd88be3c24111a49231fdc5f922e956e98c4842eef461713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950004"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a>Clase Msvm \_ Synthetic3DDisplayControllerSettingData

Representa la configuración de un controlador de pantalla 3D sintético para una máquina virtual. Esta clase solo se usa con máquinas virtuales que usan RemoteFX.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
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
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ Synthetic3DDisplayControllerSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ Synthetic3DDisplayControllerSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Se trata de una propiedad de solo lectura, pero si la propiedad **ResourceType** es 20 (controlador de gráficos), se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

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

Unidades de asignación utilizadas por las **propiedades Reservation** **y Limit.** Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

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

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dispositivo al que está conectado este recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Se trata de una propiedad de solo lectura, pero si 1) la propiedad **ResourceType** es 17 (puerto serie) o 2) la propiedad **ResourceType** es 21 (extensión Storage) y la propiedad **ResourceSubType** es "Disco duro virtual de Microsoft", se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

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

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solo se puede asignar un recurso host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz. Para los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso host subyacente que se va a asignar. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

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

**MaximumMonitors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número máximo de monitores disponibles para el controlador de pantalla 3D. El número mínimo de monitores es 1 y el máximo depende de la resolución de pantalla máxima. En la tabla siguiente se define el número máximo de monitores permitidos para diferentes resoluciones.



| Resolución            | Monitores máximos |
|-----------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

**MaximumScreenResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la resolución de pantalla máxima para el controlador de pantalla 3D. Debe ser uno de los siguientes valores.

<dt>

<span id="1024___768"></span>

<span id="1024___768"></span>**1024 \* 768** (0)


</dt> <dd>

La resolución máxima es 1024 768.

</dd> <dt>

<span id="1280___1024"></span>

<span id="1280___1024"></span>**1280 \* 1024** (1)


</dt> <dd>

La resolución máxima es 1280 1024.

</dd> <dt>

<span id="1600___1200"></span>

<span id="1600___1200"></span>**1600 \* 1200** (2)


</dt> <dd>

La resolución máxima es 1600 1200.

</dd> <dt>

<span id="1920___1200"></span>

<span id="1920___1200"></span>**1920 \* 1200** (3)


</dt> <dd>

La resolución máxima es 1920 1200.

</dd> <dt>

<span id="2560___1600"></span>

<span id="2560___1600"></span>**2560 \* 1600** (4)


</dt> <dd>

La resolución máxima es 2650 1600.

</dd> <dt>

<span id="3840___2160"></span>

<span id="3840___2160"></span>**3840 \* 2160** (5)


</dt> <dd>

La resolución máxima es 3840 2160.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.msvm \_ synte

 

</dd> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**ResourceType**](msvm-processorsettingdata.md) tiene el valor 1(Other). Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asignó este recurso. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de recursos de CPU reservados para su uso por la máquina virtual. Se garantiza que estos recursos estarán disponibles para su consumo por parte de la máquina virtual. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir diferentes modelos del mismo tipo de recurso. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de núcleos de la máquina virtual. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la unidad de medida para la **propiedad VirtualQuantity.** El valor de esta propiedad debe ser un valor legal del calificador Unidades de programación, tal como se define en el anexo C.1 de DSP0004 V2.5 o posterior. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VRAMSizeBytes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tamaño de la memoria de vídeo de la máquina virtual.

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

<dt>



 (67108864)


</dt> <dd></dd> <dt>



 (134217728)


</dt> <dd></dd> <dt>



 (268435456)


</dt> <dd></dd> <dt>



 (536870912)


</dt> <dd></dd> <dt>



 (1073741824)


</dt> <dd></dd> </dl>

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entero que define el peso de cada procesador de máquina virtual. Una vez que se hayan cumplido todas las reservas, la capacidad restante del procesador físico de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus pesos relativos. Esta propiedad se hereda de [**\_ RESOURCEAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

0

Intervalo: 0 1000

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


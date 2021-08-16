---
description: Representa los datos de estado de la característica de descarga de puertos.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Msvm_EthernetSwitchPortOffloadData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e6e2de8571d665dc86393708b2afcf73fc4885f0b4de26624daafcdccff995b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681485"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a>Clase Msvm \_ EthernetSwitchPortOffloadData

Representa los datos de estado de la característica de descarga de puertos.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchPortOffloadData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchPortOffloadData** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Estado de la característica de descarga del puerto de conmutador Ethernet".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre de la subclase usada en la creación de esta instancia de datos de puerto. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "Msvm \_ EthernetSwitchPortOffloadData".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Representa los datos de estado de la característica de descarga de puerto".

</dd> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre de clase de creación del sistema de ámbito. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "Msvm \_ EthernetSwitchPort".

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 64 )
</dt> </dl>

Id. de dispositivo del puerto que tiene como ámbito esta instancia de datos de puerto. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Estado de la característica de descarga del puerto de conmutador Ethernet".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IovOffloadUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

La virtualización de E/S actual (IOV) descarga el uso.

</dd> <dt>

**IovQueuePairUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Número actual de pares de cola que usa el puerto.

</dd> <dt>

**IovVfDataPathActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica si la ruta de acceso de datos de VF de IOV está activa.

</dd> <dt>

**IovVfId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificador de VF de IOV actual que se asigna al puerto. Esto es válido si **IovOffloadUsage** no es cero.

</dd> <dt>

**IpsecCurrentOffloadSaCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

El número actual de ranuras de descarga de asociación de seguridad (SA) en uso en el puerto.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Cadena que identifica de forma única esta instancia de datos de puerto dentro del ámbito del conmutador y el puerto. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** (256)
</dt> </dl>

Nombre de clase de creación del sistema de ámbito. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "Msvm \_ VirtualEthernetSwitch".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre del conmutador virtual que tiene como ámbito esta instancia de datos de puerto. Esta propiedad se hereda de [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md).

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica si VMMQ está activo.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703.

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica cuántas colas se usan para VRSS/VMMQ.

> [!Note]  
> Esta propiedad se agregó en Windows 10 versión 1703 y Windows Server 2016.

 

</dd> <dt>

**VMQId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Identificador de cola de máquina virtual actual que se asigna al puerto. Esto es válido si **VMQOffloadUsage** no es cero.

</dd> <dt>

**VMQOffloadUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

La cola de máquina virtual (VMQ) actual descarga el uso.

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Indica si vRSS está activo.

> [!Note]  
> Esta propiedad se agregó en Windows 10 versión 1703.

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica si la CPU de VMQ principal se excluye de la tabla de direccionamiento indirecto de VRSS/VMMQ.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica si se produce la propagación de VRSS/VMMQ del lado host, independientemente de la configuración RSS de la NIC virtual.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica el número mínimo de colas usadas para VRSS/VMMQ.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica cómo las colas VRSS/VMMQ se dirige a distintos procesadores de host.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Indica cómo se asocian los canales de Vmbus a los procesadores de host.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


---
description: Representa la configuración actual de un conmutador Ethernet virtual.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687260"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>MSVM \_ VirtualEthernetSwitchSettingData (clase)

Representa la configuración actual de un conmutador Ethernet virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualEthernetSwitchSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualEthernetSwitchSettingData** tiene estas propiedades.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de grupos de recursos de host que se van a asociar o que están asociados actualmente con el conmutador Ethernet con el fin de asignar conexiones Ethernet entre una máquina virtual y un conmutador Ethernet. Cada valor debe ajustarse al URI de WBEM de producción \_ \_ UntypedInstancePath, tal y como se define en DSP0207. Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual. Los errores en este caso significan un error que es detectado por la plataforma del host, como una condición de estado de espera no interrumpida. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se realizará para la máquina virtual cuando se apague el host. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se realizará para la máquina virtual cuando se inicie el host. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tiempo de retardo antes de que la máquina virtual se inicie automáticamente. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host. Un número menor indica la activación anterior. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**BandwidthReservationMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Modo de reserva de ancho de banda.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valor predeterminado** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Peso** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absolute** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del conmutador Ethernet virtual".

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso de un directorio donde se almacena la información sobre la configuración de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso relativa y el nombre de un archivo donde se almacena la información sobre la configuración de la máquina virtual. Esta ruta de acceso es relativa a la propiedad **ConfigurationDataRoot** . Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "configuración activa del conmutador Ethernet virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ExtensionOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de instancias incrustadas de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representan las extensiones de conmutador enlazadas a este modificador en el orden en que se aplican.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".

</dd> <dt>

**IOVPreferred**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si la virtualización de e/s de raíz única (SR-IOV) es preferida o no, si está disponible, en el adaptador subyacente.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso de un directorio en el que se almacena la información de registro de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el número máximo de direcciones MAC únicas que puede obtener el conmutador para admitir el aprendizaje de direcciones MAC, tal como se define en el estándar IEEE 802,1. Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notas proporcionadas por el usuario que están relacionadas con la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**PacketDirectEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se debe usar PacketDirect, si está disponible. El valor predeterminado es **false**.

> [!Note]  
> Esta propiedad se agregó en Windows 10 y Windows Server 2016.

 

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso completa de un archivo donde se almacena información relacionada con la recuperación de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso de un directorio donde se almacena información sobre las instantáneas de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso de un directorio donde se almacena información relacionada con la suspensión de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual. Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.

</dd> <dt>

**TeamingEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si se debe usar la formación de equipos NIC. El valor predeterminado es **false**.

> [!Note]  
> Esta propiedad se agregó en Windows 10 y Windows Server 2016.

 

</dd> <dt>

**Virtualsystemidentifer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del objeto [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen estos datos de configuración. Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de máquina virtual que representan los datos de configuración. Esta propiedad se hereda de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de identificadores de VLAN a los que puede tener acceso este conmutador. Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


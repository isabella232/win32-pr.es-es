---
description: Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908223"
---
# <a name="msvm_bioselement-class"></a>MSVM \_ BIOSElement (clase)

Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema. El BIOS no es un dispositivo lógico, por lo tanto, el BIOS virtual no debe considerarse como un dispositivo de máquina virtual. Dado que no es un dispositivo, no tiene un grupo de recursos de equipo correspondiente. El objeto BIOS está asociado a la máquina virtual a través de la Asociación [**MSVM \_ SystemBIOS**](msvm-systembios.md) .

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ BIOSElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ BIOSElement** tiene estas propiedades.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de serie del panel base de la máquina virtual.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único del BIOS.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado habilitado del Bloq Num en el BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de serie del BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

El orden en el que se buscará en los dispositivos un sector de arranque en el inicio.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Identificador interno de esta compilación de elemento de software. Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 14.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El BIOS lo rellena automáticamente cuando se crea la máquina virtual.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El BIOS lo rellena automáticamente cuando se crea la máquina virtual.

</dd> <dt>

**Dese**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Conjunto de código utilizado por el elemento de software. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Idioma seleccionado actualmente para el BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| ISO8859-1".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del elemento. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.

Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información. La propiedad **EnabledState** también puede contener más información. Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Value                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Aceptar**</dt> <dt>5</dt> </dl>                                                                               | La máquina virtual es totalmente funcional y funciona en parámetros operativos normales y sin errores.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Error principal**</dt> <dt>20</dt> </dl>             | Se produjo un error importante en la máquina virtual. Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha puesto en pausa.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Error crítico**</dt> <dt>25</dt> </dl> | El elemento no es funcional y es posible que la recuperación no sea posible. Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o información, o que uno o varios discos que contienen los discos duros virtuales de la máquina virtual tienen poco espacio en disco.<br/> |



 

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Identificador del fabricante para este elemento de software. A menudo, se trata de una referencia de almacén (SKU) o un número de pieza. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El BIOS lo rellena automáticamente cuando se crea la máquina virtual. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (32)
</dt> </dl>

Edición de idioma de este elemento de software. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de idiomas instalables para el BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| ISO8859-1".

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección final de la memoria que ocupa este BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en 0xFFFFF.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección inicial de la memoria que ocupa este BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en 0xE0000.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe la utilidad Flash/Load de BIOS necesaria para actualizar el elemento BIOS. En esta propiedad se puede indicar la versión y otra información. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en **null**.

</dd> <dt>

**Le**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Fabricante de este BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en "Microsoft Corporation".

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (1024)
</dt> </dl>

Nombre usado para identificar este elemento de software. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "BIOS".

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** . Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene los Estados actuales del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). El valor en el índice cero (0) es uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Aceptar**</dt> <dt>2</dt> </dl>                                                                                      | La máquina virtual es funcional y funciona con normalidad.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>3</dt> </dl>                                         | La máquina virtual solo es parcialmente funcional. Esto indica que no se puede tener acceso al almacenamiento que contiene la configuración. Una máquina virtual en este estado solo se puede desactivar o eliminar. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Error predictivo**</dt> <dt>5</dt> </dl> | La máquina virtual es funcional, pero puede producir un error en el futuro. Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio disponible. La máquina virtual se pausará si no hay más espacio disponible en disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Detenido**</dt> <dt>10</dt> </dl>                                            | Este valor no se admite. Si se detiene la máquina virtual, la propiedad **EnabledState** tendrá un valor de 3 (deshabilitado).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**En el servicio**</dt> <dt>11</dt> </dl>                                | La máquina virtual está procesando una solicitud.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inactivo**</dt> <dt>15</dt> </dl>                                            | Este valor no se admite. Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).<br/>                                                                                    |



 

El valor en el índice uno (1) es opcional y contiene información de estado secundaria. Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual. Si **OperationalStatus** \[ 0 \] es 2 (OK),  \[ \] se puede interrumpir la operación indicada por OperationalStatus 1.

El valor de **OperationalStatus** \[ 1 \] es uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creando instantánea**</dt> <dt>32768</dt> </dl>                                 | Se está creando una instantánea en el proceso de creación de la máquina virtual.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Aplicando la instantánea**</dt> <dt>32769</dt> </dl>                                 | Una instantánea está en proceso de aplicarse a la máquina virtual.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminando instantánea**</dt> <dt>32770</dt> </dl>                                 | Se está eliminando una instantánea de la máquina virtual.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Esperando a iniciar**</dt> <dt>32771</dt> </dl>                                     | La máquina virtual se iniciará después de que haya transcurrido el retraso de inicio automático.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Combinación de discos**</dt> <dt>32772</dt> </dl>                                                 | Se están combinando los discos duros virtuales de las instantáneas eliminadas previamente.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportando Máquina Virtual**</dt> <dt>32773</dt> </dl> | La máquina virtual se está exportando.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrando la máquina Virtual**</dt> <dt>32774</dt> </dl> | La máquina virtual se está migrando en directo desde un equipo físico a otro.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

El fabricante y el sistema operativo de un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 (otro), que requiere que la propiedad **OtherTargetOS** tenga un valor distinto de **null** . Para el resto de los valores de **TargetOperatingSystem**, la propiedad **OtherTargetOS** debe ser **null**. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es true, se trata del BIOS principal del equipo. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en **true**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que representa la ubicación de publicación del registro de atributos del BIOS o de los registros a los que se ajusta la implementación. Esta propiedad se hereda de [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La fecha en la que se liberó el BIOS. Esta propiedad se hereda de [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Número de serie asignado del BIOS. Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement).

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Identificador del elemento de software. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "Microsoft:*GUID* \\ *specific Device-specific Data*".

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado del ciclo de vida de un elemento de software. Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 2 (ejecutable).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** . Por ejemplo, si 11 (en servicio) es el valor asignado a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] puede incluir una explicación sobre el motivo por el que la máquina virtual está procesando una solicitud. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entorno del sistema operativo del elemento. Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 0 (desconocido).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Versión del BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "8.02.00".

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ BIOSElement** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_BIOSELEMENT CIM**](cim-bioselement.md)
</dt> <dt>

[Clases de BIOS](bios-classes.md)
</dt> <dt>

[**\_BIOSELEMENT CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 


---
description: Representa el software de bajo nivel que se carga en ram para configurar e iniciar el sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement clase
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
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149305"
---
# <a name="msvm_bioselement-class"></a>Clase BIOSElement de Msvm \_

Representa el software de bajo nivel que se carga en ram para configurar e iniciar el sistema. El BIOS no es un dispositivo lógico, por lo que el BIOS virtual no debe considerarse como un dispositivo de máquina virtual. Como no es un dispositivo, no tiene un grupo de recursos correspondiente. El objeto BIOS está asociado a la máquina virtual a través de la [**asociación \_ SystemBIOS de Msvm.**](msvm-systembios.md)

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ BIOSElement de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ BIOSElement de Msvm** tiene estas propiedades.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de serie de la placa base de la máquina virtual.

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

Estado habilitado del bloqueo num en el BIOS.

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

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Orden en el que se buscará un sector de arranque en el inicio de los dispositivos.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Identificador interno de esta compilación del elemento de software. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en 14.

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

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Rellenado automáticamente por el BIOS cuando se crea la máquina virtual.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Rellenado automáticamente por el BIOS cuando se crea la máquina virtual.

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Conjunto de código utilizado por el elemento de software. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en **Null.**

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación para comunicarse con el elemento administrado subyacente. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Idioma seleccionado actualmente para el BIOS. Esta propiedad se hereda de [**\_ CIM BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| iso8859-1".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus con** detalles de estado adicionales. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del elemento. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.

Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información. La **propiedad EnabledState** también puede contener más información. Por ejemplo, cuando el espacio en disco es críticamente bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)



| Valor                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Ok**</dt> <dt>5</dt> </dl>                                                                               | La máquina virtual es totalmente funcional y funciona dentro de los parámetros operativos normales y sin errores.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Error principal**</dt> <dt>20</dt> </dl>             | La máquina virtual ha sufrido un error importante. Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha pausado.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Error crítico**</dt> <dt>25</dt> </dl> | El elemento no es funcional y es posible que la recuperación no sea posible. Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o de información, o que uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco.<br/> |



 

</dd> <dt>

**Código de identificación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Identificador del fabricante para este elemento de software. A menudo, será una unidad de mantenimiento de existencias (SKU) o un número de pieza. Esta propiedad se hereda de [**\_ CIM SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en **Null.**

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Rellenado automáticamente por el BIOS cuando se crea la máquina virtual. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (32)
</dt> </dl>

Edición de idioma de este elemento de software. Esta propiedad se hereda de [**\_ CIM SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en **Null.**

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de idiomas instalables para el BIOS. Esta propiedad se hereda de [**\_ CIM BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| iso8859-1".

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección final de la memoria que ocupa este BIOS. Esta propiedad se hereda de [**\_ CIM BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en 0xFFFFF.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **unit64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección inicial de la memoria que ocupa este BIOS. Esta propiedad se hereda de [**\_ CIM BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en 0xE0000.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe la utilidad flash/load del BIOS necesaria para actualizar el elemento BIOS. La versión y otra información se pueden indicar en esta propiedad. Esta propiedad se hereda de [**\_ CIM BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en **Null.**

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Fabricante de este BIOS. Esta propiedad se hereda de [**\_ BIOSElement de CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "Microsoft Corporation".

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (1024)
</dt> </dl>

Nombre utilizado para identificar este elemento de software. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "BIOS".

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado actual para la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la **propiedad EnabledState.** Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene los estados actuales del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) El valor del índice cero (0) es uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Ok**</dt> <dt>2</dt> </dl>                                                                                      | La máquina virtual es funcional y funciona con normalidad.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>3</dt> </dl>                                         | La máquina virtual solo es parcialmente funcional. Esto indica que no se puede acceder al almacenamiento que contiene la configuración. Una máquina virtual en este estado solo se puede desactivar o eliminar. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Error predictivo**</dt> <dt>5</dt> </dl> | La máquina virtual es funcional, pero puede producir un error en el futuro. Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio libre. La máquina virtual se pausará si no hay más espacio en disco disponible.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Detenido**</dt> <dt>10</dt> </dl>                                            | Este valor no se admite. Si se detiene la máquina virtual, la **propiedad EnabledState** tendrá un valor de 3 (deshabilitado).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**En el servicio**</dt> <dt>11</dt> </dl>                                | La máquina virtual está procesando una solicitud.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inactivo**</dt> <dt>15</dt> </dl>                                            | Este valor no se admite. Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).<br/>                                                                                    |



 

El valor del índice uno (1) es opcional y contiene información de estado secundario. Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual. Si **OperationalStatus** \[ 0 es 2 (correcto), se puede interrumpir la operación indicada por \] **OperationalStatus** \[ 1. \]

El valor de **OperationalStatus** \[ 1 \] es uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creación de la instantánea**</dt> <dt>32768</dt> </dl>                                 | Se está creando una instantánea para la máquina virtual.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Aplicación de la instantánea**</dt> <dt>32769</dt> </dl>                                 | Una instantánea está en proceso de aplicarse a la máquina virtual.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminación de la instantánea**</dt> <dt>32770</dt> </dl>                                 | Una instantánea está en proceso de eliminación de la máquina virtual.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> Waiting to Start 32771 <dt>**(Esperando a iniciar**</dt> <dt>32771)</dt> </dl>                                     | La máquina virtual se inicia una vez transcurrido el retraso de inicio automático.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Combinar discos**</dt> <dt>32772</dt> </dl>                                                 | Se combinan discos duros virtuales de instantáneas eliminadas previamente.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportación de la máquina virtual**</dt> <dt>32773</dt> </dl> | La máquina virtual se está exportando.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migración de la máquina virtual**</dt> <dt>32774</dt> </dl> | La máquina virtual se está migrando en vivo de un equipo físico a otro.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

El fabricante y el sistema operativo de un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 (Other), lo que requiere que la propiedad **OtherTargetOS** tenga un valor distinto de **NULL.** Para todos los demás valores **de TargetOperatingSystem**, la **propiedad OtherTargetOS** debe ser **Null.** Esta propiedad se hereda de [**\_ CIM SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en **Null.**

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es True, este es el BIOS principal del sistema informático. Esta propiedad se hereda de [**\_ BIOSElement de CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en **True.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe usarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que representa la ubicación de publicación del registro de atributos BIOS o los registros a los que cumple la implementación. Esta propiedad se hereda de [**CIM \_ BIOSElement.**](/windows/desktop/CIMWin32Prov/cim-bioselement)

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha en que se publicó el BIOS. Esta propiedad se hereda de [**CIM \_ BIOSElement.**](/windows/desktop/CIMWin32Prov/cim-bioselement)

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Número de serie asignado del BIOS. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Identificador del elemento de software. Esta propiedad se hereda de [**\_ CIM SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "Microsoft:*datos* \\ *específicos del dispositivo GUID".*

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado del ciclo de vida de un elemento de software. Esta propiedad se hereda de [**\_ CIM SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en 2 (ejecutable).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**\_ MANAGEDSystemElement de CIM,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("Indexed")
</dt> </dl>

Matriz que contiene cadenas que describen los valores de **matriz OperationalStatus** correspondientes. Por ejemplo, si 11 (en servicio) es el valor asignado a **OperationalStatus** \[ \] 0, **StatusDescriptions** 0 puede contener una explicación de por qué la máquina virtual está procesando \[ una \] solicitud. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El entorno del sistema operativo del elemento. Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en 0 (desconocido).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

La versión del BIOS. Esta propiedad se hereda de [**\_ BIOSElement de CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "8.02.00".

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ BIOSElement de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[Clases de BIOS](bios-classes.md)
</dt> <dt>

[**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 


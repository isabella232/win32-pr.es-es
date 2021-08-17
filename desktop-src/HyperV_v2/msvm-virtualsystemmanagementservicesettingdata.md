---
description: Representa la configuración del servicio de virtualización presente en un único sistema host.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ccb0a1a9bc4a10ec7f8a366f012446e0374dab299f8ee779f16cfeb38fb005b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147978"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>Clase Msvm \_ VirtualSystemManagementServiceSettingData

Representa la configuración del servicio de virtualización presente en un único sistema host. Las propiedades de esta clase no se pueden modificar directamente. El cliente debe llamar al [**método ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar cualquiera de estas propiedades.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ VirtualSystemManagementServiceSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ VirtualSystemManagementServiceSettingData** tiene estas propiedades.

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

Lo usan los OEM para permitir que los sistemas operativos Windows BIOS se ejecuten en la máquina virtual. Esta cadena debe tener exactamente 32 caracteres de longitud.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Servicio de administración de sistemas virtuales de Hyper-V".

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del nombre de nodo de todo el mundo (WWNN) para las direcciones de nombre ancho del mundo generadas dinámicamente que se usan para los adaptadores de bus host sintéticos.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")
</dt> </dl>

Raíz de datos externos predeterminada. De forma predeterminada,*"root* \\ ProgramData Microsoft Windows \\ \\ \\ Virtualization".

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el almacenamiento en caché de archivos en memoria se debe usar para los discos de forma predeterminada. Este valor se puede invalidar por disco en el campo **CachingMode** de la clase [**\_ StorageAllocationSettingData de Msvm.**](msvm-storageallocationsettingdata.md)

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Sin almacenamiento en caché** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Elementos padres que se pueden compartir en** caché (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso predeterminada del disco duro virtual. De forma predeterminada,*"root* \\ Users Public Documents Virtual Hard \\ \\ \\ Disks".

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ MANAGEDElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Configuración para el servicio de administración de sistema virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Servicio de administración de sistemas virtuales de Hyper-V". Al cambiar esta propiedad, se cambiará **la propiedad ElementName** del derivado [**\_ logicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) asociado.

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se permite el modo de sesión mejorada en el servidor. **True** indica permitido; en caso contrario, **False.**

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la cantidad de tiempo que el dispositivo virtual Canal de fibra sintético esperará a que aparezca un número de unidad lógica (LUN) antes de iniciar una máquina virtual.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si el programador raíz del hipervisor está habilitado o no.

> [!Note]  
> Se ha agregado Windows 10, versión 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Microsoft:*host",* donde *host* es el nombre NetBIOS del sistema de equipo host.

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección MAC máxima para direcciones MAC generadas dinámicamente.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección máxima del nombre de puerto ancho del mundo (WWPN) para las direcciones de nombre ancho del mundo generadas dinámicamente que se usan para los adaptadores de bus host sintéticos.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección MAC mínima para direcciones MAC generadas dinámicamente.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección mínima del nombre de puerto de todo el mundo para las direcciones de nombre de todo el mundo generadas dinámicamente que se usan para los adaptadores de bus host sintéticos.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si se puede asignar memoria desde nodos de acceso remoto a memoria no uniforme (NUMA) al iniciar una máquina virtual o al asignar memoria a una máquina virtual mediante memoria dinámica. Puede ser uno de los siguientes valores.



| Value                                                                                | Significado                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Verdadero**</dt> </dl>  | La memoria se puede asignar desde nodos NUMA locales y remotos.<br/>                   |
| <dl> <dt>**Falso**</dt> </dl> | La memoria solo se puede asignar desde el nodo NUMA asignado a la máquina virtual.<br/> |



 

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Información general de DMTF \| \| 001.4")
</dt> </dl>

Describe cómo se puede acceder al propietario del sistema principal (por ejemplo, el número de teléfono o la dirección de correo electrónico). De forma predeterminada, está vacía. Este nombre no puede superar los 256 caracteres de longitud.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| General Information \| 001.3")
</dt> </dl>

Nombre del propietario del sistema principal. De forma predeterminada, "Administradores". Este valor no puede superar los 64 caracteres de longitud.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm VirtualSystemManagementServiceSettingData** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Clases de administración de sistemas virtuales](virtual-system-management-classes.md)
</dt> </dl>

 


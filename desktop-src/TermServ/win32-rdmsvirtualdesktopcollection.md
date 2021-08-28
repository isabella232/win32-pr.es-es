---
title: Win32_RDMSVirtualDesktopCollection clase
description: Crea y administra una colección de escritorios virtuales.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 580b5ae194a28726a06143dce0007eeedfbb8564b49a4cbc2e7c2d0d8507dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868075"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>Clase \_ RDMSVirtualDesktopCollection de Win32

Crea y administra una colección de escritorios virtuales.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSVirtualDesktopCollection de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ RDMSVirtualDesktopCollection de Win32** tiene estos métodos.



| Método                                                                                            | Descripción                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddVirtualDesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Agrega un escritorio virtual a una colección de escritorios virtuales.<br/>                                                                              |
| [**CancelPatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Cancela un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Recupera un valor de propiedad entero de una colección de escritorios virtuales.<br/>                                                               |
| [**GetPatchProperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.<br/>             |
| [**GetStringProperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Recupera un valor de propiedad de cadena de una colección de escritorios virtuales.<br/>                                                                 |
| [**ProvisioningEnumerateJobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Enumera los trabajos de aprovisionamiento de escritorios virtuales para este servicio.<br/>                                                                       |
| [**ProvisioningJobCancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Cancela un trabajo de aprovisionamiento de escritorio virtual.<br/>                                                                                          |
| [**ProvisioningJobExecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Ejecuta un trabajo de aprovisionamiento de escritorio virtual.<br/>                                                                                             |
| [**ProvisioningJobGetReport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.<br/>                                                                |
| [**ProvisioningPrepJob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Crea un trabajo de aprovisionamiento de escritorio virtual.<br/>                                                                                          |
| [**RemoveVirtualDesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Quita un escritorio virtual de una colección de escritorios virtuales.<br/>                                                                         |
| [**SchedulePatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Programa un trabajo de aprovisionamiento de actualizaciones de software que instala actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Actualiza un valor de propiedad entero de una colección de escritorios virtuales.<br/>                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Actualiza un valor de propiedad de cadena de una colección de escritorios virtuales.<br/>                                                                     |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDMSVirtualDesktopCollection de Win32** tiene estas propiedades.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene o establece el alias de la colección.

</dd> <dt>

**CollectionDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene o establece la descripción de la colección.

</dd> <dt>

**IconoContents**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene o establece una matriz de valores que especifican iconos para la colección.

</dd> <dt>

**Isha**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica si la colección contiene máquinas virtuales de alta disponibilidad. **TRUE** si la colección contiene máquinas virtuales de alta disponibilidad; de lo contrario, **FALSE**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica si la colección está administrada. **TRUE** si se administra la colección; de lo contrario, **FALSE**.

</dd> <dt>

**IsUserAdmin**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica si un usuario es administrador de una máquina virtual. **TRUE** si el usuario es administrador en una máquina virtual; de lo contrario, **FALSE**.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece el nombre de la colección.

</dd> <dt>

**RollbackEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica si una máquina virtual se ha implantado con una instantánea de máquina virtual. **TRUE** si la máquina virtual se ha implantado con una instantánea de máquina virtual; de lo contrario, **FALSE**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene o establece un descriptor de seguridad con formato SSDL que controla el acceso a la colección.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica si la colección se muestra en Terminal Services Web Access (TS Web Access). **TRUE** para mostrar la colección en TS Web Access; de lo contrario, **FALSE**.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene o establece un valor que indica el tipo de sesiones de máquina virtual hospedadas por la colección.

Esta propiedad contiene uno de los valores siguientes:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)


</dt> <dd>

Máquinas virtuales temporales.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)


</dt> <dd>

Máquinas virtuales creadas manualmente.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)


</dt> <dd>

Máquinas virtuales generadas automáticamente.

</dd> </dl>

</dd> <dt>

**UserVHDSetting**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene o establece la configuración del VHD de datos de usuario para la colección.

</dd> <dt>

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene o establece la configuración de escritorio para las máquinas virtuales de la colección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 


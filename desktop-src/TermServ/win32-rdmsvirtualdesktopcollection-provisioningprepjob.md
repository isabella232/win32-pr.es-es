---
title: Método ProvisioningPrepJob de la clase Win32_RDMSVirtualDesktopCollection
description: Crea un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Método ProvisioningPrepJob Servicios de Escritorio remoto
- Método ProvisioningPrepJob Servicios de Escritorio remoto, Win32_RDMSVirtualDesktopCollection interfaz
- Win32_RDMSVirtualDesktopCollection Servicios de Escritorio remoto de interfaz, método ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996307"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningPrepJob de la \_ clase RDMSVirtualDesktopCollection de Win32

Crea un trabajo de aprovisionamiento de escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CollectionAlias* \[ de\]
</dt> <dd>

El alias de la colección que hospeda el escritorio virtual.

</dd> <dt>

*VMHostName* \[ de\]
</dt> <dd>

El nombre de host de la máquina virtual.

</dd> <dt>

*VMName* \[ de\]
</dt> <dd>

El nombre de la máquina virtual.

</dd> <dt>

*ExportToLocation* \[ de\]
</dt> <dd>

La ruta de acceso completa de la ubicación para exportar el trabajo de aprovisionamiento.

</dd> <dt>

*bSysPrep* \[ de\]
</dt> <dd>

Indica si el trabajo de aprovisionamiento representa una implementación de Sysprep.

</dd> <dt>

*MachineName* \[ de\]
</dt> <dd>

El nombre de equipo del equipo que hospeda la máquina virtual.

</dd> <dt>

*Nombre de usuario* \[ de\]
</dt> <dd>

El nombre de usuario del administrador de la máquina virtual.

</dd> <dt>

*Contraseña* \[ de de\]
</dt> <dd>

La contraseña del administrador de la máquina virtual.

</dd> <dt>

*JobGuid* \[ enuncia\]
</dt> <dd>

**GUID** que identifica de forma única el trabajo de aprovisionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






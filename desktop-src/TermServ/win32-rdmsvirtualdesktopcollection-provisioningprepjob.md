---
title: Método ProvisioningPrepJob de la Win32_RDMSVirtualDesktopCollection clase
description: Crea un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Método ProvisioningPrepJob Servicios de Escritorio remoto
- Método ProvisioningPrepJob Servicios de Escritorio remoto , Win32_RDMSVirtualDesktopCollection interfaz
- Win32_RDMSVirtualDesktopCollection interfaz Servicios de Escritorio remoto , método ProvisioningPrepJob
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
ms.openlocfilehash: b2dab9dcbd606dd32857f0d2dc4b2de3d8516e2b2da10e804fa36254679c1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422845"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningPrepJob de la clase \_ RDMSVirtualDesktopCollection de Win32

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

*CollectionAlias* \[ En\]
</dt> <dd>

Alias de la colección que hospeda el escritorio virtual.

</dd> <dt>

*VMHostName* \[ En\]
</dt> <dd>

Nombre de host de la máquina virtual.

</dd> <dt>

*VMName* \[ En\]
</dt> <dd>

El nombre de la máquina virtual.

</dd> <dt>

*ExportToLocation* \[ En\]
</dt> <dd>

Ruta de acceso completa a la ubicación para exportar el trabajo de aprovisionamiento.

</dd> <dt>

*bSysPrep* \[ En\]
</dt> <dd>

Indica si el trabajo de aprovisionamiento representa una implementación de Sysprep.

</dd> <dt>

*MachineName* \[ En\]
</dt> <dd>

Nombre de la máquina del equipo que hospeda la máquina virtual.

</dd> <dt>

*UserName* \[ En\]
</dt> <dd>

Nombre de usuario del administrador de la máquina virtual.

</dd> <dt>

*Contraseña* \[ En\]
</dt> <dd>

Contraseña del administrador de la máquina virtual.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

GUID **que** identifica de forma única el trabajo de aprovisionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDMSVirtualDesktopCollection de Win32 \_**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






---
title: Win32_RdvhManagement clase
description: Describe un servicio Escritorio remoto administración de host virtual (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement clase Servicios de Escritorio remoto
- Win32_RdvhManagement clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea403621aa23cb999bdf2fe692e2d4e053866492608e71346d978cb764ab005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422585"
---
# <a name="win32_rdvhmanagement-class"></a>Clase \_ RdvhManagement de Win32

Describe un servicio Escritorio remoto administración de host virtual (RDVH).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Miembros

La **clase \_ RdvhManagement de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase \_ RdvhManagement de Win32** tiene estos métodos.



| Método                                                                                  | Descripción                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada. Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia una migración en vivo de máquina virtual en escenarios de VDI<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copia la ubicación de la máquina virtual base localmente en Host de RDV servidor<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada. Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia una migración en vivo de la máquina virtual en escenarios de VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Establece permisos en la máquina virtual para el autor de la llamada<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Revierte los permisos en la máquina virtual establecidos por RdvSetupVMPermissions.<br/>                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | \\TerminalServices cimv2 \\ raíz<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 






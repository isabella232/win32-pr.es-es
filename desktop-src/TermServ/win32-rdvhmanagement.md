---
title: Win32_RdvhManagement (clase)
description: Describe un servicio de administración de Escritorio remoto virtual (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RdvhManagement de clase, se describe
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
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676769"
---
# <a name="win32_rdvhmanagement-class"></a>\_Clase Win32 RdvhManagement

Describe un servicio de administración de Escritorio remoto virtual (RDVH).

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

La clase **Win32 \_ RdvhManagement** tiene estos métodos.



| Método                                                                                  | Descripción                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada. Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia una migración en vivo de la máquina virtual en escenarios VDI.<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copia localmente la ubicación de la máquina virtual base en Host de RDV Server<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada. Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Inicia una migración en vivo de la máquina virtual en escenarios VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Establece permisos en la máquina virtual para el autor de la llamada<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Revierte los permisos de la máquina virtual establecida por RdvSetupVMPermissions<br/>                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | Raíz de \\ cimv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 






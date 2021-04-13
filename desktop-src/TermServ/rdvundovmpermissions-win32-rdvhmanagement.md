---
title: Método RdvUndoVMPermissions de la clase Win32_RdvhManagement
description: Revierte los permisos establecidos por RdvSetupVMPermissions en la máquina virtual especificada.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Método RdvUndoVMPermissions Servicios de Escritorio remoto
- Método RdvUndoVMPermissions Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492760"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Método RdvUndoVMPermissions de la \_ clase RdvhManagement de Win32

Revierte los permisos establecidos por [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) en la máquina virtual especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VmName* \[ de\]
</dt> <dd>

Nombre de la máquina virtual en la que se van a deshacer los permisos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 






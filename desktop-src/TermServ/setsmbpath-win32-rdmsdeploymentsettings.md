---
title: Método SetSMBPath de la clase Win32_RDMSDeploymentSettings
description: Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Método SetSMBPath Servicios de Escritorio remoto
- Método SetSMBPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996672"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetSMBPath de la \_ clase RDMSDeploymentSettings de Win32

Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ de\]
</dt> <dd>

La nueva ruta de acceso al recurso compartido de SMB, en formato UNC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






---
title: Método GetSMBPath de la Win32_RDMSDeploymentSettings clase
description: Recupera la ruta de acceso UNC al recurso compartido SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Método GetSMBPath Servicios de Escritorio remoto
- Método GetSMBPath Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método GetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073340"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetSMBPath de la clase RDMSDeploymentSettings de Win32 \_

Recupera la ruta de acceso UNC al recurso compartido SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Recibe una ruta de acceso con formato UNC al recurso compartido SMB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDMSDeploymentSettings de Win32 \_**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






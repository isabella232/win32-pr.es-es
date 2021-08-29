---
title: Método SetSMBPath de la Win32_RDMSDeploymentSettings clase
description: Actualiza la ruta de acceso UNC al recurso compartido SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Método SetSMBPath Servicios de Escritorio remoto
- Método SetSMBPath Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método SetSMBPath
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
ms.openlocfilehash: 3c91d64b589ed61e7cc9713636dcc0f0b090da749ca9d8e8d9ab7567e8500175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008585"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetSMBPath de la clase RDMSDeploymentSettings de Win32 \_

Actualiza la ruta de acceso UNC al recurso compartido SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ En\]
</dt> <dd>

Nueva ruta de acceso al recurso compartido SMB, en formato UNC.

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

 

 






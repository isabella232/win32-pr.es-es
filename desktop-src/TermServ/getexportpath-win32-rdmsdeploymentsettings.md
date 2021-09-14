---
title: Método GetExportPath de la Win32_RDMSDeploymentSettings clase
description: Recupera la ruta de acceso del directorio en la que se implementan las máquinas virtuales para una colección de escritorios virtuales.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Método GetExportPath Servicios de Escritorio remoto
- Método GetExportPath Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170625"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetExportPath de la clase RDMSDeploymentSettings de Win32 \_

Recupera la ruta de acceso del directorio en la que se implementan las máquinas virtuales para una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Recibe la ruta de acceso del directorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

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

 

 






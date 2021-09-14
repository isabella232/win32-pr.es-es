---
title: Método GetStringArrayDeploymentSetting de la Win32_RDMSDeploymentSettings clase
description: Recupera la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Método GetStringArrayDeploymentSetting Servicios de Escritorio remoto
- Método GetStringArrayDeploymentSetting Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método GetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073335"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetStringArrayDeploymentSetting de la clase RDMSDeploymentSettings de Win32 \_

Recupera la configuración de implementación de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Alias de la colección de escritorios virtuales.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Recibe una matriz de cadenas que contiene la configuración de implementación.

</dd> </dl>

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

 

 






---
title: Método GetStringProperty de la Win32_RDMSDeploymentSettings clase
description: Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4a7cb338cd6f6858bba0536b012effb8621eee0d68dc386eceb79cdfd694e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033695"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetStringProperty de la clase RDMSDeploymentSettings de Win32 \_

Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
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

Cadena que recibe el valor recuperado.

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

 

 






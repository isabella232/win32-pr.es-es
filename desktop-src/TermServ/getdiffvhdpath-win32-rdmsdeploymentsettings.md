---
title: Método GetDiffVHDPath de la Win32_RDMSDeploymentSettings clase
description: Recupera la ruta de acceso del directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Método GetDiffVHDPath Servicios de Escritorio remoto
- Método GetDiffVHDPath Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968516"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetDiffVHDPath de la clase RDMSDeploymentSettings de Win32 \_

Recupera la ruta de acceso del directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Recibe la nueva ruta de acceso del disco de diferenciación.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RDMSDeploymentSettings de Win32 \_**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






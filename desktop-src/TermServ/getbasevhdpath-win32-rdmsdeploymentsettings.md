---
title: Método GetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales. | Método GetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Método GetBaseVHDPath Servicios de Escritorio remoto
- Método GetBaseVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003615"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetBaseVHDPath de la \_ clase RDMSDeploymentSettings de Win32

Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ enuncia\]
</dt> <dd>

Recibe la ruta de acceso de implementación de VHD.

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

 

 






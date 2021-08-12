---
title: Método SetBaseVHDPath de la Win32_RDMSDeploymentSettings clase
description: Recupera la ruta de acceso base al directorio en el que se implementan los discos duros virtuales de la colección de escritorios virtuales. | Método SetBaseVHDPath de la Win32_RDMSDeploymentSettings clase
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Método SetBaseVHDPath Servicios de Escritorio remoto
- Método SetBaseVHDPath Servicios de Escritorio remoto , Win32_RDMSDeploymentSettings clase
- Win32_RDMSDeploymentSettings clase Servicios de Escritorio remoto , método SetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6179c87e6566a18f2c47046007a17c6073a51e0afcdce4925b50d327adf528f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605122"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetBaseVHDPath de la clase RDMSDeploymentSettings de Win32 \_

Recupera la ruta de acceso base al directorio en el que se implementan los discos duros virtuales de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ En\]
</dt> <dd>

Nueva ruta de acceso de implementación de VHD.

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

 

 






---
title: Método SetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales. | Método SetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Método SetBaseVHDPath Servicios de Escritorio remoto
- Método SetBaseVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetBaseVHDPath
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
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678679"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método SetBaseVHDPath de la \_ clase RDMSDeploymentSettings de Win32

Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryPath* \[ de\]
</dt> <dd>

La nueva ruta de implementación de VHD.

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

 

 






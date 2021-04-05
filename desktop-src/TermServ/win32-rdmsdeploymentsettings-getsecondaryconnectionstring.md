---
title: Método GetSecondaryConnectionString de la clase Win32_RDMSDeploymentSettings
description: Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Método GetSecondaryConnectionString Servicios de Escritorio remoto
- Método GetSecondaryConnectionString Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359726"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Método GetSecondaryConnectionString de la \_ clase RDMSDeploymentSettings de Win32

Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecondaryConnectionString* \[ enuncia\]
</dt> <dd>

Cadena de conexión que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 






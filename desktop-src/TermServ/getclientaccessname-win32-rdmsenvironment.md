---
title: Método GetClientAccessName de la Win32_RDMSEnvironment clase
description: Recupera el nombre del registro de recursos del Sistema de nombres de dominio (DNS) del Escritorio remoto Management Services (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Método GetClientAccessName Servicios de Escritorio remoto
- Método GetClientAccessName Servicios de Escritorio remoto , Win32_RDMSEnvironment clase
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto método , GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 206ef89765bd18a73559c98d70a614664d076099214bd20f7b97ca9c29e94bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139008"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Método GetClientAccessName de la clase \_ RDMSEnvironment de Win32

Recupera el nombre del registro de recursos del Sistema de nombres de dominio (DNS) del Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientAccessName* \[ out\]
</dt> <dd>

Recibe el nombre RR recuperado.

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

[**\_RDMSEnvironment de Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 






---
title: Método GetActiveServer de la Win32_RDMSEnvironment clase
description: Recupera el nombre de dominio completo (FQDN) del Escritorio remoto Management Services (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Método GetActiveServer Servicios de Escritorio remoto
- Método GetActiveServer Servicios de Escritorio remoto , Win32_RDMSEnvironment clase
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto , método GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730fa1230ddf08f5bd598e2041cd82ab4287d30387fa61460771fea5bcf3ec50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139018"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Método GetActiveServer de la clase \_ RDMSEnvironment de Win32

Recupera el nombre de dominio completo (FQDN) del Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerName* \[ out\]
</dt> <dd>

Recibe el FQDN recuperado.

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

[**\_RDMSEnvironment de Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 






---
title: Método SetClientAccessName de la Win32_RDMSEnvironment clase
description: Actualiza el nombre del registro de recursos (RR) del Sistema de nombres de dominio (RR) de un Escritorio remoto Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Método SetClientAccessName Servicios de Escritorio remoto
- Método SetClientAccessName Servicios de Escritorio remoto , Win32_RDMSEnvironment clase
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto , método SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604877"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Método SetClientAccessName de la clase \_ RDMSEnvironment de Win32

Actualiza el nombre del registro de recursos (RR) del Sistema de nombres de dominio (RR) de un Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientAccessName* \[ En\]
</dt> <dd>

Nuevo nombre RR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 






---
title: Método SetClientAccessName de la clase Win32_RDMSEnvironment
description: Actualiza el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) de un entorno de Escritorio remoto Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Método SetClientAccessName Servicios de Escritorio remoto
- Método SetClientAccessName Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método SetClientAccessName
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
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676966"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Método SetClientAccessName de la \_ clase RDMSEnvironment de Win32

Actualiza el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) de un entorno de Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientAccessName* \[ de\]
</dt> <dd>

Nombre del nuevo RR.

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

[**Win32 \_ RDMSEnvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 






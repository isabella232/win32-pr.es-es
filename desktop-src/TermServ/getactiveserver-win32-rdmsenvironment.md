---
title: Método GetActiveServer de la clase Win32_RDMSEnvironment
description: Recupera el nombre de dominio completo (FQDN) del entorno de servicios de administración de Escritorio remoto (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Método GetActiveServer Servicios de Escritorio remoto
- Método GetActiveServer Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método GetActiveServer
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
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491350"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Método GetActiveServer de la \_ clase RDMSEnvironment de Win32

Recupera el nombre de dominio completo (FQDN) del entorno de servicios de administración de Escritorio remoto (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDeServidor* \[ enuncia\]
</dt> <dd>

Recibe el FQDN recuperado.

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

 

 






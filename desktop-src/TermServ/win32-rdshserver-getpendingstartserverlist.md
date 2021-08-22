---
title: Método GetPendingStartServerList de la Win32_RDSHServer clase
description: Recupera una lista de servidores en espera de inicio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Método GetPendingStartServerList Servicios de Escritorio remoto
- Método GetPendingStartServerList Servicios de Escritorio remoto , Win32_RDSHServer clase
- Win32_RDSHServer clase Servicios de Escritorio remoto , método GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422655"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Método GetPendingStartServerList de la clase RDSHServer de Win32 \_

Recupera una lista de servidores en espera de inicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*maxServers* \[ En\]
</dt> <dd>

Número máximo de servidores que se devolverán en la lista.

</dd> <dt>

*ServerFQDNs* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, contiene una colección de nombres de dominio completos de los servidores que esperan a iniciarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La lista de servidores se restablece después de cada llamada, de modo que la siguiente llamada no obtenga un servidor duplicado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RdsHServer de Win32 \_**](win32-rdshserver.md)
</dt> </dl>

 

 






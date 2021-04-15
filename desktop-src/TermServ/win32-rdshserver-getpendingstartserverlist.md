---
title: Método GetPendingStartServerList de la clase Win32_RDSHServer
description: Recupera una lista de servidores en espera de inicio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Método GetPendingStartServerList Servicios de Escritorio remoto
- Método GetPendingStartServerList Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método GetPendingStartServerList
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
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422362"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Método GetPendingStartServerList de la \_ clase RDSHServer de Win32

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

*maxServers* \[ de\]
</dt> <dd>

Número máximo de servidores que se van a devolver en la lista.

</dd> <dt>

*ServerFQDNs* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, contiene una colección de nombres de dominio completos de los servidores a la espera de iniciarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La lista de servidores se restablece después de cada llamada, de modo que la siguiente llamada no obtenga un servidor duplicado.

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

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 






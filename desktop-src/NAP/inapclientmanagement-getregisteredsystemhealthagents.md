---
title: Método INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera información acerca de los Sha registrados.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Método GetRegisteredSystemHealthAgents NAP
- Método GetRegisteredSystemHealthAgents NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996694"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>INapClientManagement:: GetRegisteredSystemHealthAgents (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetRegisteredSystemHealthAgents** recupera información acerca de los Sha registrados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*recuento* \[ enuncia\]
</dt> <dd>

Un puntero a un [**SystemHealthEntityCount**](nap-datatypes.md) que describe el número de Sha registrados.

</dd> <dt>

*agentes* \[ de enuncia\]
</dt> <dd>

Puntero a una matriz de estructuras [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen los Sha registrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






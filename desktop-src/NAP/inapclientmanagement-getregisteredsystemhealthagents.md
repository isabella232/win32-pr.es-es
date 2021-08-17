---
title: Método INapClientManagement GetRegisteredSystemHealthAgents (NapManagement.h)
description: Recupera información sobre las SHA registradas.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Método NAP de GetRegisteredSystemHealthAgents
- Método NAP de GetRegisteredSystemHealthAgents, interfaz INapClientManagement
- INapClientManagement interface NAP , GetRegisteredSystemHealthAgents method
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
ms.openlocfilehash: 57d9c2792282245ad4903d77700f5413bef0d2f769a65753aed60f50ba759707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800115"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>Método INapClientManagement::GetRegisteredSystemHealthAgents

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetRegisteredSystemHealthAgents** recupera información sobre las SHA registradas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Puntero a [**SystemHealthEntityCount que**](nap-datatypes.md) describe el número de SHA registrados.

</dd> <dt>

*agentes* \[ out\]
</dt> <dd>

Puntero a una matriz de [**estructuras NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen las SHA registradas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | NapAgent no se está ejecutando.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 






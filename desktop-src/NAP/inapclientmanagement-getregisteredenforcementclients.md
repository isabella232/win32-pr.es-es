---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement.h)
description: Recupera información sobre los clientes de cumplimiento registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método NAP de GetRegisteredEnforcementClients
- Método NAP de GetRegisteredEnforcementClients, interfaz INapClientManagement
- INapClientManagement interface NAP , GetRegisteredEnforcementClients method
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7854a36ffb1d313a1598764c5375a8146471c1b2fd930b4022948f147acc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940213"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Método INapClientManagement::GetRegisteredEnforcementClients

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método GetRegisteredEnforcementClients** recupera información sobre los clientes de cumplimiento registrados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Puntero a [**EnforcementEntityCount que**](nap-datatypes.md) contiene el número de clientes de cumplimiento registrados.

</dd> <dt>

*aplicadores* \[ out\]
</dt> <dd>

Puntero a una matriz de [**estructuras NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen los clientes de cumplimiento registrados.

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

 

 






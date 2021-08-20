---
title: Método INapClientManagement UnregisterEnforcementClient (NapManagement.h)
description: Anula el registro de un cliente de cumplimiento con el sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- UnregisterEnforcementClient, método NAP
- UnregisterEnforcementClient, método NAP, interfaz INapClientManagement
- INapClientManagement interface NAP , UnregisterEnforcementClient (método)
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0298b55a5552f2a3ce7a40e048874076729f7e506475c8626de9e9e343da3b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134557"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>Método INapClientManagement::UnregisterEnforcementClient

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método UnregisterEnforcementClient** anula el registro de un cliente de cumplimiento con el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* \[ en\]
</dt> <dd>

Valor [**EnforcementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento para anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operación correcta.<br/>                                               |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | El límite de recursos del sistema no pudo realizar la operación.<br/>             |
| <dl> <dt>**NAP \_ E \_ TODAVÍA \_ ENLAZADO**</dt> </dl> | No se pudo anular el registro del cliente de cumplimiento y permanece enlazado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 






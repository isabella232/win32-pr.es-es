---
title: Método INapClientManagement RegisterEnforcementClient (NapManagement.h)
description: Registra un cliente de cumplimiento con el sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Método NAP RegisterEnforcementClient
- Método NAP registerEnforcementClient , interfaz INapClientManagement
- Nap de interfaz INapClientManagement , método RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e22deffb8f144e8f7176bd78fb18978228a26251be5591df61a322e5da17d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134567"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>Método INapClientManagement::RegisterEnforcementClient

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método RegisterEnforcementClient** registra un cliente de cumplimiento con el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*enforcer* \[ En\]
</dt> <dd>

Puntero a una [**estructura de datos NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro asociada al cliente de cumplimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT que incluye, entre otros, uno de los siguientes.



| Código devuelto                                                                                            | Descripción                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operación correcta.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/>                |
| <dl> <dt>**NAP \_ E \_ CONFLICTING \_ ID**</dt> </dl> | Ya se ha registrado un agente de cumplimiento que use el identificador especificado.<br/> |



 

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

 

 






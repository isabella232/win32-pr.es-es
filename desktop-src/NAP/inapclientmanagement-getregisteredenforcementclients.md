---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera información acerca de los clientes de cumplimiento registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método GetRegisteredEnforcementClients NAP
- Método GetRegisteredEnforcementClients NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetRegisteredEnforcementClients
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
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491711"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>INapClientManagement:: GetRegisteredEnforcementClients (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **GetRegisteredEnforcementClients** recupera información sobre los clientes de cumplimiento registrados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*recuento* \[ enuncia\]
</dt> <dd>

Un puntero a un [**EnforcementEntityCount**](nap-datatypes.md) que contiene el número de clientes de cumplimiento registrados.

</dd> <dt>

*aplicadores* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de estructuras [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen los clientes de cumplimiento registrados.

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

 

 






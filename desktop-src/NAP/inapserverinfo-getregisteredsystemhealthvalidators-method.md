---
title: Método INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement.h)
description: Recupera una lista de SHV registrados.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Método NAP GetRegisteredSystemHealthValidators
- Método NAP de GetRegisteredSystemHealthValidators, interfaz INapServerInfo
- Nap de interfaz INapServerInfo , método GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e096d706107ca812e569e46c980f56cdc7b8eba14f4742530f632570fd3d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133950"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Método INapServerInfo::GetRegisteredSystemHealthValidators

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapServerInfo::GetRegisteredSystemHealthValidators** recupera una lista de SHV registrados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Puntero a [**systemHealthEntityCount que**](nap-type-constants.md) contiene el número de SHV registrados.

</dd> <dt>

*validadores* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro de SHV.

</dd> <dt>

*validatorClsids* \[ out\]
</dt> <dd>

Puntero a una matriz de los ID de los SHV registrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 






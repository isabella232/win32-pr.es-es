---
title: Método INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Anula el registro de un SHA con el sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Método UnregisterSystemHealthAgent NAP
- Método UnregisterSystemHealthAgent NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676859"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>INapClientManagement:: UnregisterSystemHealthAgent (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **UnregisterSystemHealthAgent** anula el registro de un Sha con el sistema NAP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

[**SystemHealthEntityId**](nap-datatypes.md) que identifica el agente de mantenimiento del sistema cuyo registro se va a anular.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.



| Código devuelto                                                                                         | Descripción                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Operación correcta.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ todavía \_ enlazado**</dt> </dl> | SHA permanece enlazado y no se pudo anular el registro.<br/>    |



 

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

 

 






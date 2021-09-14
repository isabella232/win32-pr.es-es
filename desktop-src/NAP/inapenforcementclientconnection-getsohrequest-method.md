---
title: Método INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient.h)
description: Obtiene la solicitud SoH-Request actual.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Nap del método GetSoHRequest
- Método NAP de GetSoHRequest , interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362151"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a>Método INapEnforcementClientConnection::GetSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetSoHRequest** obtiene el soH-Request actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Puntero a un puntero a una [**estructura NetworkSoHRequest,**](/windows/win32/api/naptypes/ns-naptypes-networksoh) que es un blob de datos opaco para el ejecutor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Lo establece NapAgent y los aplicadores lo consultan para enviarlos en la conexión.

Un paquete SoH de longitud cero byte no es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






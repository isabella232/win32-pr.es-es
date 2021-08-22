---
title: Método INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient.h)
description: Establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Método NAP de SetSoHResponse
- Método NAP de SetSoHResponse, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , Método SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a86c1a0fc86fcef9189f9d575063cee9abdf627e1cf3c58e68d669358142f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626235"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>Método INapEnforcementClientConnection::SetSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::SetSoHResponse** establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohResponse* \[ En\]
</dt> <dd>

Puntero a una estructura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) única, que es un blob de datos opaco para el ejecutor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | El paquete SoH es válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Un paquete de tamaño cero es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






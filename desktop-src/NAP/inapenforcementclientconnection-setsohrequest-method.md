---
title: Método INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient.h)
description: Establece soH-request.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Método NAP de SetSoHRequest
- Método NAP de SetSoHRequest, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , SetSoHRequest method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2d2d3a4574b086d49cba7d9c0afda72cf62621dbed37add8550a7ae2f93cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799639"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>Método INapEnforcementClientConnection::SetSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::SetSoHRequest** establece SoH-Request.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ En\]
</dt> <dd>

Puntero a una estructura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) única, que es un blob de datos opaco para el ejecutor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | El paquete SoH es válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Lo establece NapAgent y lo consultan los aplicadores para enviarlos en la conexión.

Un paquete SoH de longitud de cero bytes no es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






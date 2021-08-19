---
title: Método INapEnforcementClientConnection GetMaxSize (NapEnforcementClient.h)
description: Obtiene el tamaño máximo del paquete SoH para este cliente.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Método NAP de GetMaxSize
- Método NAP de GetMaxSize, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , GetMaxSize (método)
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cacde01de088739f6e2dc8b8952c81394d82120e278b072189ed1572555740a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799619"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a>INapEnforcementClientConnection::GetMaxSize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetMaxSize** obtiene el tamaño máximo del paquete SoH para este cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*maxSize* \[ out\]
</dt> <dd>

Puntero a [**ProtocolMaxSize**](nap-datatypes.md) que indica el tamaño máximo, en bytes, del paquete SoH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

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

 

 






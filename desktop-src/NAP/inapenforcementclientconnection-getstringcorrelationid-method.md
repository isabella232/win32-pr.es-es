---
title: Método INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient.h)
description: Obtiene la versión de cadena del identificador que se usa para correlacionar solicitudes y respuestas.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Método NAP de GetStringCorrelationId
- Método NAP de GetStringCorrelationId, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , GetStringCorrelationId method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a7729873958d830e40a1979abb5fbcb3135ec4f08ae75af8396244ef35537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781015"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>INapEnforcementClientConnection::GetStringCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetStringCorrelationId** obtiene la versión de cadena del identificador que se usa para correlacionar solicitudes y respuestas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Puntero a una [**estructura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión de cadena de CorrelationId de [**la conexión.**](/windows/win32/api/naptypes/ns-naptypes-correlationid)

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

 

 






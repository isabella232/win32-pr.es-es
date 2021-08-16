---
title: Método INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient.h)
description: Establece el identificador que se usa para poner en correlación soH-requests y SoH-responses.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Método NAP de SetCorrelationId
- Método SetCorrelationId NAP , interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be8a7fbcbe9e2accd074768b8a0e50d6ce2dcaa2bda53e063cb76d294ff92c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368265"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>INapEnforcementClientConnection::SetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::SetCorrelationId** establece el identificador usado para correlacionar soH-requests y SoH-responses.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ En\]
</dt> <dd>

Estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica un intercambio de SoH específico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

NapAgent establece el identificador de correlación y se basa en el identificador de conexión.

Este identificador se usa para correlacionar solicitudes y respuestas, es decir, describe de forma única un intercambio de SoH y siempre contiene el identificador del conjunto de SoH más reciente en el objeto de conexión.

Cuando se recibe SoH-Response, NapAgent garantiza primero la coincidencia de los IDs. Si no es así, se devuelve un error y el ejecutor debe quitar el paquete. Vea [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) para obtener más detalles.

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

 

 






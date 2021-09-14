---
title: Método INapEnforcementClientConnection GetCorrelationId (NapEnforcementClient.h)
description: Obtiene el identificador utilizado para poner en correlación soH-requests y SoH-responses.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- Método NAP de GetCorrelationId
- Método NAP de GetCorrelationId, interfaz INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , GetCorrelationId method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362161"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>INapEnforcementClientConnection::GetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientConnection::GetCorrelationId** obtiene el identificador que se usa para correlacionar soH-requests y soH-responses.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Estructura [**CorrelationId única**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que identifica este intercambio de SoH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent establece el identificador de correlación y se basa en el identificador de conexión.

Este identificador se usa para correlacionar solicitudes y respuestas, es decir, describe de forma única un intercambio de SoH y siempre contiene el identificador del conjunto de SoH más reciente en el objeto de conexión.

Cuando se SoH-Response una aplicación, NapAgent garantiza primero la coincidencia de los IDs. Si no es así, se devuelve un error y el ejecutor debe quitar el paquete. Vea [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) para obtener más detalles.

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

 

 






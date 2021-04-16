---
title: Método INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Establece el identificador usado para correlacionar las solicitudes de SoH y las respuestas de SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Método SetCorrelationId NAP
- Método SetCorrelationId NAP, interfaz INapEnforcementClientConnection
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
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533963"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>INapEnforcementClientConnection:: SetCorrelationId (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientConnection:: SetCorrelationId** establece el identificador usado para correlacionar las solicitudes de SOH y las respuestas de SOH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CorrelationId* \[ de\]
</dt> <dd>

Una estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica un intercambio de SOH específico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El NapAgent establece el identificador de correlación y se basa en el identificador de conexión.

Este identificador se usa para correlacionar las solicitudes y las respuestas, es decir, describe de forma única un intercambio de SoH y siempre contiene el ID. del SoH más reciente establecido en el objeto de conexión.

Cuando se recibe un SoH-Response, el NapAgent primero asegura que los identificadores coincidan; Si no es así, se devuelve un error y el forzado debe quitar el paquete. Consulte [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 






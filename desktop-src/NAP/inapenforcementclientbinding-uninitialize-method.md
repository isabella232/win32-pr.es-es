---
title: INapEnforcementClientBinding método UnInitialize (NapEnforcementClient. h)
description: Concluye el servicio NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Anular la inicialización del método NAP
- Método uninitial NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método UnInitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666085"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>INapEnforcementClientBinding:: UnInitialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientBinding:: UnInitialize** termina el servicio NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

El NapAgent bloquea el procesamiento hasta que se completen todas las llamadas existentes en las interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) y [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) . Al final de esta llamada, NapAgent libera todas sus referencias en punteros COM del cliente de cumplimiento.

Antes de llamar a esta función, el exigidor debe llamar a [**INapEnforcementClientBinding:: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) en todas las conexiones activas, por lo que se puede notificar a los Sha si alguno de sus SoH-Requests fuera huérfano.

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 






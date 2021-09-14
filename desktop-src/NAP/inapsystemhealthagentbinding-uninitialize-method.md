---
title: Método INapSystemHealthAgentBinding Uninitialize (NapSystemHealthAgent.h)
description: Hace que NapAgent libere todas sus referencias a punteros COM del agente de mantenimiento del sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Uninitialize method NAP
- Uninitialize method NAP , INapSystemHealthAgentBinding interface
- Método NAP de la interfaz INapSystemHealthAgentBinding , Uninitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071656"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>INapSystemHealthAgentBinding::Uninitialize (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthAgentBinding::Uninitialize** hace que NapAgent libere todas sus referencias a los punteros COM del agente de mantenimiento del sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                   | Operación realizada correctamente.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | Sha no se ha inicializado previamente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl>     | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Observaciones

NapAgent bloquea la ejecución de esta llamada de método hasta que se completan todas las llamadas existentes en las interfaces Binding y Callback.

Sha debe llamar a [**Initialize antes**](inapsystemhealthagentbinding-initialize-method.md) de llamar a este método o a cualquier otro método de la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 






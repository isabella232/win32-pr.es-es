---
title: Método INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent.h)
description: Lo usan las SHA cuando cambia su SoH.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Nap del método NotifySoHChange
- Método NAP NotifySoHChange , interfaz INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP , NotifySoHChange (método)
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a418a78e0d21178f3dd1889816873afb1c7ec7212da48be5d75e44d40d0a61d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367843"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>Método INapSystemHealthAgentBinding::NotifySoHChange

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las SHA usan el método **INapSystemHealthAgentBinding::NotifySoHChange** cuando cambia su SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifySoHChange();
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
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | El SHA no se ha inicializado previamente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl>     | NapAgent se ha detenido. Este objeto se recuperará automáticamente y se volverá a conectar a NapAgent, una vez que se reinicie.<br/> |



 

## <a name="remarks"></a>Comentarios

Las SHA no deben llamar a esta API de forma especulativa, ya que produce un intercambio de soH en la conexión. Las llamadas a esta API solo se deben realizar cuando sea necesario.

NapAgent no contiene este subproceso para procesar el cambio de SoH. En su lugar, devuelve inmediatamente y procesa el cambio de forma asincrónica.

Sha debe llamar a [**Initialize antes**](inapsystemhealthagentbinding-initialize-method.md) de llamar a este método o a cualquier otro método de la [**interfaz INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 






---
title: Método INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent.h)
description: NapAgent llama a este método para indicar que ha cambiado el estado de aislamiento del sistema o la hora de finalización de la sondeo.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Método NAP NotifySystemIsolationStateChange
- Método NAP NotifySystemIsolationStateChange , interfaz INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , NotifySystemIsolationStateChange method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071637"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>Método INapSystemHealthAgentCallback::NotifySystemIsolationStateChange

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent llama al método **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** para indicar que el estado de aislamiento del sistema o la hora de finalización de la sondeo han cambiado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica que se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

El agente de mantenimiento puede consultar el estado nap del sistema mediante [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






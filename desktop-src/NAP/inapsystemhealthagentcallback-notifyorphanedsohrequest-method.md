---
title: Método INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent.h)
description: Se llama a si se ha consultado una solicitud SoHRequest desde sha, pero la respuesta nunca ha vuelto.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Método NAP NotifyOrphanedSoHRequest
- Método NAP NotifyOrphanedSoHRequest , interfaz INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , NotifyOrphanedSoHRequest method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071639"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>Método INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Se llama al método **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** si se ha consultado [**una solicitud SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) desde sha, pero la respuesta nunca ha vuelto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*correlationId* \[ En\]
</dt> <dd>

Puntero a la estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica el [**soHRequest huérfano.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica que se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

El sistema puede llamar a este método en los casos siguientes:

-   No se pudo enviar una [**solicitud SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en la conexión.
-   Se [**envió una solicitud SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en la conexión, pero no regresó **SoHResponse,** es decir, el ejecutor se ha quedó el tiempo de espera o no había ningún SHV correspondiente en el lado servidor.
-   La conexión se ha desconectado o un ejecutor se ha desconectado.

Esta es solo una notificación de mejor esfuerzo, por lo que las SHA no deben confiar en esta información para limpiar el estado. Hay varias situaciones en las que no se notificará a sha:

-   Si un ejecutor no funciona bien, es decir, no notifica al SHA cuando el estado de conexión está fuera de estado.
-   Si se bloquea un ejecutor.
-   En condiciones de error, es decir, NapAgent no tiene memoria.

Es posible que las SHA reciban algunas notificaciones falsos cuando se enlazan por primera vez a NapAgent, por ejemplo, si hay un intercambio de SoH en curso cuando el sha está enlazado y, a continuación, se hace el tiempo de espera.

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

 

 






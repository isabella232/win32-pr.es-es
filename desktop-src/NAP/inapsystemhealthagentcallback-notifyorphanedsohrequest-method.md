---
title: Método INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Se llama a si se ha consultado un SoHRequest desde SHA, pero la respuesta nunca llegó.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Método NotifyOrphanedSoHRequest NAP
- Método NotifyOrphanedSoHRequest NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método NotifyOrphanedSoHRequest
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422579"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Se llama al método **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** si se ha consultado un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) desde Sha, pero la respuesta nunca llegó.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CorrelationId* \[ de\]
</dt> <dd>

Un puntero a la estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)huérfano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Indica que se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.

El sistema puede llamar a este método en los casos siguientes:

-   No se pudo enviar un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en la conexión.
-   Se envió un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) de seguridad de red en la conexión, pero no se devolvió ningún **SoHResponse** , es decir, el forzado agotó el tiempo de espera o no había ningún SHV correspondiente en el lado servidor.
-   La conexión dejó de funcionar o un forzado se desconectó.

Esta es solo una notificación de mejor esfuerzo, por lo que los Sha no deben confiar en esta información para limpiar el estado. Hay varias situaciones en las que un SHA no recibirá ninguna notificación:

-   Si un forzador no se comporta, es decir, no notifica al SHA cuando el estado de conexión está inactivo.
-   Si se bloquea un forzador.
-   En condiciones de error, es decir, el NapAgent no tiene memoria suficiente.

Los Sha pueden obtener algunas notificaciones falsas cuando se enlazan por primera vez a NapAgent, por ejemplo, si un intercambio de SoH está en curso cuando se enlaza SHA y después se agota el tiempo de espera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 






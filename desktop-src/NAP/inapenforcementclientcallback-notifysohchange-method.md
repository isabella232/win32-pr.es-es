---
title: Método INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient.h)
description: NapAgent lo usa para informar al cliente de cumplimiento de los cambios de SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Método NAP NotifySoHChange
- Método NAP NotifySoHChange , interfaz INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP , NotifySoHChange (método)
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9011db09b698f886bd10ad19298a104668d038cc2bb11136b6e4ac58035e3425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940139"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>INapEnforcementClientCallback::NotifySoHChange (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

NapAgent usa el método de devolución de llamada **INapEnforcementClientCallback::NotifySoHChange** para informar al cliente de cumplimiento de los cambios de SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método de devolución de llamada debe devolver uno de los siguientes códigos de error.



| Código devuelto                                                                                                | Descripción                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Devuelve este valor si la operación se ha realiza correctamente.<br/>                                                                                                                                                              |
| <dl> <dt>**SERVIDOR \_ RPC S NO \_ \_ DISPONIBLE**</dt> </dl> | La devolución de este valor hace que el ejecutor se quite de la lista enlazada a SHA y se vacíe la entrada de caché de NapAgent correspondiente. Después, el SHA con errores puede volver a inicializarse con NapAgent.<br/> |



 

## <a name="remarks"></a>Comentarios

La finalización de la corrección del sistema es un evento de cambio de estado del sistema. Esto significa que debe llamar a **NotifySoHChange cuando** una notificación [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indique que el cliente está corregido. Cuando se fija un cliente, **el** miembro de estado de la estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) devuelto por **GetFixupInfo** tiene un valor **de fixupStateSuccess**.

Después de que NapAgent lo llame a través de esta devolución de llamada, el agente de cumplimiento debe llamar a [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar la nueva solicitud. Esta llamada se puede realizar en el mismo subproceso que **INapEnforcementClientCallback::NotifySoHChange**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 






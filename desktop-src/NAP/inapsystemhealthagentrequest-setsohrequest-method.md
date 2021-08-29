---
title: Método INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent.h)
description: Los agentes de mantenimiento usan para escribir su solicitud soH resultante de la llamada a INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Método NAP de SetSoHRequest
- Método NAP de SetSoHRequest, interfaz INapSystemHealthAgentRequest
- Interfaz NAP de INapSystemHealthAgentRequest, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6945e8fcc8e53398067cfb7f26bd6029d8920876d23d35aab676b9fb197e64e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686145"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>Método INapSystemHealthAgentRequest::SetSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los agentes de mantenimiento usan el método **INapSystemHealthAgentRequest::SetSoHRequest** para escribir su solicitud de SoH resultante de la llamada a [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sohRequest* \[ En\]
</dt> <dd>

Puntero a un [**paquete SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*cacheSmioForLaterUse* \[ En\]
</dt> <dd>

Valor **BOOL que** es **TRUE si** NapAgent debe almacenar en caché [**soH**](/windows/win32/api/naptypes/ns-naptypes-soh) y **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>           | Operación realizada correctamente.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | El límite de recursos del sistema no pudo realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 






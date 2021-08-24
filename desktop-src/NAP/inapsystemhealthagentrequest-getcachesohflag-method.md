---
title: Método INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent.h)
description: NapAgent solo lo usa.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Método NAP de GetCacheSoHFlag
- Método NAP de GetCacheSoHFlag, interfaz INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP , GetCacheSoHFlag method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9268e620f38ef314c0699612436518315e44cf7f554bb393d2259ae4664519cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133680"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a>INapSystemHealthAgentRequest::GetCacheSoHFlag (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapSystemHealthAgentRequest::GetCacheSoHFlag** solo lo usa NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cacheSmioForLaterUse* 
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

 

 






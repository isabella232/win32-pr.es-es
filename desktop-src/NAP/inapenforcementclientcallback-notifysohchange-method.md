---
title: Método INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: NapAgent lo usa para informar al cliente de cumplimiento de los cambios de SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interfaz INapEnforcementClientCallback
- Interfaz INapEnforcementClientCallback NAP, método NotifySoHChange
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
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151203"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>INapEnforcementClientCallback:: NotifySoHChange (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El NapAgent usa el método de devolución de llamada **INapEnforcementClientCallback:: NotifySoHChange** para informar al cliente de cumplimiento de los cambios de SOH.

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
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Devuelve este valor si la operación se realizó correctamente.<br/>                                                                                                                                                              |
| <dl> <dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt> </dl> | Al devolver este valor, el aplicador se quita de la lista Bound-SHA y la entrada de caché de NapAgent correspondiente que se va a vaciar. Después, el SHA con error puede volver a inicializarse con el NapAgent.<br/> |



 

## <a name="remarks"></a>Observaciones

La finalización de la corrección del sistema es un evento de cambio de mantenimiento del sistema. Esto significa que debe llamar a **NotifySoHChange** cuando una notificación [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indica que el cliente es fijo. Cuando se corrige un cliente, el miembro **State** de la estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) devuelto por **GetFixupInfo** tiene un valor de **fixupStateSuccess**.

Después de ser llamado por el NapAgent a través de esta devolución de llamada, el agente de cumplimiento debe llamar a [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar la nueva solicitud. Esta llamada se puede realizar en el mismo subproceso que **INapEnforcementClientCallback:: NotifySoHChange**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 






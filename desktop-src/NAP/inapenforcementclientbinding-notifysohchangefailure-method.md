---
title: Método INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient.h)
description: El cliente de cumplimiento lo usa para informar a NapAgent de que no pudo procesar un INapEnforcementClientCallback notifySoHChange anterior.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Método NAP NotifySoHChangeFailure
- NotifySoHChangeFailure method NAP , INapEnforcementClientBinding interface
- INapEnforcementClientBinding interface NAP , NotifySoHChangeFailure method
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f91ae79656ec8909a8bff041e3ddc2714f1cbd17a65362e08731e9ca411d57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134223"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>INapEnforcementClientBinding::NotifySoHChangeFailure (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El cliente de cumplimiento usa el método **INapEnforcementClientBinding::NotifySoHChangeFailure** para informar a NapAgent de que no pudo procesar un [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                   | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | El ejecutor no se ha inicializado previamente.<br/>       |



 

## <a name="remarks"></a>Comentarios

Como resultado de este método, llame a los reintentos de NapAgent que aplican el cambio de SoH más adelante mediante una llamada a [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) de nuevo. Una vez que el cliente de cumplimiento ha llamado a [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), debe aplicar el cambio, es decir, napAgent no controla ningún error después de este punto.

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la [**interfaz INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 






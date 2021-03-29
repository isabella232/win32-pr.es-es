---
title: Método INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: Lo usa el cliente de cumplimiento para informar a NapAgent de que no pudo procesar una NotifySoHChange INapEnforcementClientCallback anterior.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Método NotifySoHChangeFailure NAP
- Método NotifySoHChangeFailure NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método NotifySoHChangeFailure
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
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493156"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>INapEnforcementClientBinding:: NotifySoHChangeFailure (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El cliente de cumplimiento usa el método **INapEnforcementClientBinding:: NotifySoHChangeFailure** para informar a NapAgent de que no pudo procesar una [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.

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
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                   | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ no \_ inicializado**</dt> </dl> | El exigidor no se ha inicializado previamente.<br/>       |



 

## <a name="remarks"></a>Observaciones

Como resultado de esta llamada al método, NapAgent reintenta aplicar el cambio de SoH más adelante llamando a [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) de nuevo. Una vez que el cliente de cumplimiento ha llamado a [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), debe aplicar el cambio, es decir, el NapAgent no controla ningún error después de este punto.

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
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

 

 






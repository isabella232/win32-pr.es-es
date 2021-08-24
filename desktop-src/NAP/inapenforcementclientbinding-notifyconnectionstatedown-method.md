---
title: Método INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient.h)
description: Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha desaparecido.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Método NAP NotifyConnectionStateDown
- Método NAP notifyConnectionStateDown , interfaz INapEnforcementClientBinding
- Método NAP de la interfaz INapEnforcementClientBinding , NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e40d3b46e8c970287f49d983d89733d4858e38671ac93fb75d482c0259a73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803055"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>INapEnforcementClientBinding::NotifyConnectionStateDown (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El **método INapEnforcementClientBinding::NotifyConnectionStateDown** se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha desaparecido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*downCxn* \[ En\]
</dt> <dd>

Puntero COM a la [**interfaz INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión fuera de servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                   | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | El ejecutor no se ha inicializado previamente.<br/>       |



 

## <a name="remarks"></a>Comentarios

Cuando alguna de las conexiones establecidas por un cliente de cumplimiento se desatas, el cliente de cumplimiento debe quitar la conexión de su lista activa e informar a NapAgent mediante este método. En cuanto se devuelve esta llamada, el objeto de conexión se puede liberar y liberar. NapAgent no contendrán referencias al objeto de conexión.

Como resultado de esta notificación, NapAgent actualiza su estado nap del sistema según corresponda.

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
</dt> </dl>

 

 






---
title: Método INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient.h)
description: Lo usa el cliente de cumplimiento para recuperar una solicitud SoH para una conexión determinada.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Nap del método GetSoHRequest
- Método Nap de GetSoHRequest , interfaz INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP , Método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134341"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>Método INapEnforcementClientBinding::GetSoHRequest

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El cliente de cumplimiento usa el método **INapEnforcementClientBinding::GetSoHRequest** para recuperar una solicitud SoH para una conexión determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexión* \[ En\]
</dt> <dd>

Puntero COM a una [**interfaz INapEnforcementClientConnection.**](inapenforcementclientconnection.md) NapAgent no contiene referencias al objeto asociado a esta interfaz una vez completado el método.

</dd> <dt>

*retriggerHint* \[ out\]
</dt> <dd>

Puntero a un **bool** que indica si se debe volver a desencadenar la conexión. Es TRUE **si** [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ha cambiado desde que se llamó por última vez a esta función o si [**ProbationTime**](nap-datatypes.md) ha expirado. De lo contrario, se devuelve **FALSE.**

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

NapAgent establece [**soHRequest en**](/windows/win32/api/naptypes/ns-naptypes-soh) el objeto de conexión.

Si un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estaba pendiente en esta conexión, se descarta y se notifica a los SHA de **SoHRequests huérfanos.**

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

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

 

 






---
title: Método INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Lo usa el cliente de cumplimiento para recuperar una solicitud de SoH para una conexión determinada.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método GetSoHRequest
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
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996183"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>INapEnforcementClientBinding:: GetSoHRequest (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El cliente de cumplimiento usa el método **INapEnforcementClientBinding:: GetSoHRequest** para recuperar una solicitud de SOH para una conexión determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexión* \[ de de\]
</dt> <dd>

Puntero COM a una interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) . El NapAgent no conserva las referencias al objeto asociado a esta interfaz una vez que se completa el método.

</dd> <dt>

*retriggerHint* \[ enuncia\]
</dt> <dd>

Un puntero a un **booleano** que indica si se debe volver a desencadenar la conexión. Es **true** si [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ha cambiado desde la última vez que se llamó a esta función o si [**ProbationTime**](nap-datatypes.md) ha expirado. De lo contrario, se devuelve **false** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                   | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |
| <dl> <dt>**NAP \_ E \_ no \_ inicializado**</dt> </dl> | El exigidor no se ha inicializado previamente.<br/>       |



 

## <a name="remarks"></a>Observaciones

NapAgent establece [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en el objeto de conexión.

Si un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estaba pendiente en esta conexión, se descartará y se notificará a los Sha de **SoHRequests** huérfanos.

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
</dt> </dl>

 

 






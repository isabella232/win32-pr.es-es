---
title: Método INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Método NotifyConnectionStateDown NAP
- Método NotifyConnectionStateDown NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método NotifyConnectionStateDown
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
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535608"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>INapEnforcementClientBinding:: NotifyConnectionStateDown (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El método **INapEnforcementClientBinding:: NotifyConnectionStateDown** se usa para informar a NapAgent de que una conexión a un cliente de cumplimiento ha dejado de funcionar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*downCxn* \[ de\]
</dt> <dd>

Puntero COM a la interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión hacia abajo.

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

Cuando cualquiera de las conexiones establecidas por un cliente de cumplimiento se desactive, el cliente de cumplimiento debe quitar la conexión de su lista activa e informar a NapAgent mediante este método. En cuanto se devuelve esta llamada, el objeto de conexión se puede liberar y liberar. NapAgent no conservará las referencias al objeto de conexión.

Como resultado de esta notificación, el NapAgent actualiza su estado NAP del sistema según corresponda.

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

 

 






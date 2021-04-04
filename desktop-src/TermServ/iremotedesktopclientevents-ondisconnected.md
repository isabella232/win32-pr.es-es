---
title: IRemoteDesktopClientEvents método OnDisconnect
description: Se llama cuando el control de cliente se ha desconectado de una sesión remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Método OnDisconnection Servicios de Escritorio remoto
- Método OnDisconnection Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnDisconnect
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802936"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a>IRemoteDesktopClientEvents:: OnDisconnection (método)

Se llama cuando el control de cliente se ha desconectado de una sesión remota.

## <a name="syntax"></a>Sintaxis


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*disconnectReason* \[ de\]
</dt> <dd>

Motivo del evento de desconexión.

</dd> <dt>

*ExtendedDisconnectReason* \[ de\]
</dt> <dd>

Información extendida para el evento de desconexión.

</dd> <dt>

*disconnectErrorMessage* \[ de\]
</dt> <dd>

Mensaje de error para el evento de desconexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 






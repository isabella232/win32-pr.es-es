---
title: Método IMsTscAxEvents OnServiceMessageReceived
description: Se llama cuando el cliente recibe un mensaje del sistema.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Método OnServiceMessageReceived Servicios de Escritorio remoto
- Método OnServiceMessageReceived Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca511710834f8aa9fdda02565c33c4732e4cba9300e74ad3b48276d74890bc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757253"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a>Método IMsTscAxEvents::OnServiceMessageReceived

Se llama cuando el cliente recibe un mensaje del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*serviceMessage* \[ En\]
</dt> <dd>

Especifica el mensaje del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre los mensajes del sistema, vea [Configurar la mensajería para un servidor Escritorio remoto gateway.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 


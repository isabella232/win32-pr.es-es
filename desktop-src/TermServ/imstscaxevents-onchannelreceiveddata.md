---
title: Método IMsTscAxEvents OnChannelReceivedData
description: Se llama cuando el cliente recibe datos en un canal virtual que puede incluirse en scripts.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Método OnChannelReceivedData Servicios de Escritorio remoto
- Método OnChannelReceivedData Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f411eae7e03f134f4adfd6fdc6108634e4e58c06bb8645e9f97f27e8489a3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125195"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Método IMsTscAxEvents::OnChannelReceivedData

Se llama cuando el cliente recibe datos en un canal virtual que puede incluirse en scripts.

## <a name="syntax"></a>Sintaxis


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*namename* \[ En\]
</dt> <dd>

Nombre del canal virtual en el que se recibieron los datos. Este nombre coincide con uno de los canales creados por la llamada a [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*datos* \[ En\]
</dt> <dd>

Los datos recibidos en el canal virtual que se puede incluir en el script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Consulte [Implementing Scriptable Virtual Channels using Conexión web a Escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) para obtener más información sobre este evento.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 






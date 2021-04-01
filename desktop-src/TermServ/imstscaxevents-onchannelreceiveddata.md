---
title: IMsTscAxEvents OnChannelReceivedData, método
description: Se llama cuando el cliente recibe datos en un canal virtual que admite scripts.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Método OnChannelReceivedData Servicios de Escritorio remoto
- Método OnChannelReceivedData Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnChannelReceivedData
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
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150215"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>IMsTscAxEvents:: OnChannelReceivedData (método)

Se llama cuando el cliente recibe datos en un canal virtual que admite scripts.

## <a name="syntax"></a>Sintaxis


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*chanName* \[ de\]
</dt> <dd>

Nombre del canal virtual en el que se recibieron los datos. Este nombre coincide con uno de los canales creados por la llamada a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*datos* \[ de de\]
</dt> <dd>

Los datos recibidos en el canal virtual con scripts.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Consulte [implementación de canales virtuales con scripts mediante conexión web a escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) para obtener más información sobre este evento.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 






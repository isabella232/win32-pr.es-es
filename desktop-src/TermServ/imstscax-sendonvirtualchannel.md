---
title: IMsTscAx SendOnVirtualChannel, método
description: Envía datos al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el método CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Método SendOnVirtualChannel Servicios de Escritorio remoto
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489503"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>IMsTscAx:: SendOnVirtualChannel (método)

Envía datos al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChanName* \[ de\]
</dt> <dd>

Nombre del canal virtual que se especificó en la llamada a [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*ChanData* \[ de\]
</dt> <dd>

Los datos que se van a enviar a través del canal virtual, en forma de **BSTR** . No hay ninguna restricción de que estos datos deban ser cadenas terminadas en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obtener información sobre las restricciones de nomenclatura de canal virtual.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 






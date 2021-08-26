---
title: Método IMsTscAx SendOnVirtualChannel
description: Envía datos al servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el método CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Método SendOnVirtualChannel Servicios de Escritorio remoto
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto método , SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto método , SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto método , SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , método SendOnVirtualChannel
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
ms.openlocfilehash: 03c5b84ff9cb272d5560f3b6588301a05a3e9a003db1b28f841a77b2e0618b37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125305"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>Método IMsTscAx::SendOnVirtualChannel

Envía datos al servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el [**método CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SonnombredeDesánda* \[ En\]
</dt> <dd>

Nombre del canal virtual que se especificó en la llamada a [**CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

</dd> <dt>

*ChanData* \[ En\]
</dt> <dd>

Datos que se envían a través del canal virtual, en **formato BSTR.** No hay ninguna restricción de que estos datos deben ser cadenas terminadas en NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Consulte Registro [de cliente de canal](virtual-channel-client-registration.md) virtual para obtener información sobre las restricciones de nomenclatura de canales virtuales.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 






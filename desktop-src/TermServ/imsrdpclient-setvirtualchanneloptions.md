---
title: Método IMsRdpClient SetVirtualChannelOptions
description: Establece las opciones de canal virtual para el control Escritorio remoto ActiveX virtual.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Método SetVirtualChannelOptions Servicios de Escritorio remoto
- Método SetVirtualChannelOptions Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto método , SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto método , SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890977"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>IMsRdpClient::SetVirtualChannelOptions (método)

Establece las opciones de canal virtual para el control Escritorio remoto ActiveX virtual.

Llame a este método después de llamar al [**método CreateVirtualChannels,**](imstscax-createvirtualchannels.md) pero antes de establecer una conexión con [**Conectar**](imstscax-connect.md) método. Este método establece opciones adicionales en los canales virtuales que se han creado **con CreateVirtualChannels**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SonnombredeDesánda* \[ En\]
</dt> <dd>

Nombre del canal virtual que se especificó en la llamada al [**método CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

</dd> <dt>

*options* \[ En\]
</dt> <dd>

Opciones que se establecerán para el canal virtual especificado por el *parámetroMosnombre.* Para obtener una descripción de las posibles opciones, vea [**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

Un ejemplo de uso de este método sería declarar el canal como control remoto persistente estableciendo la marca **CHANNEL OPTION REMOTE CONTROL \_ \_ \_ \_ PERSISTENT.** Esto significa que el canal no se cerraría cuando un control remoto se conecta a la sesión conectada al cliente o se desconecta de ella. Para obtener más información, [vea Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClient se define como \_ 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Consulte también

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 






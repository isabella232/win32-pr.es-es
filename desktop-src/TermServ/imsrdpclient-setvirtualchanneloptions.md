---
title: IMsRdpClient SetVirtualChannelOptions, método
description: Establece las opciones de canal virtual para el control ActiveX Escritorio remoto.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Método SetVirtualChannelOptions Servicios de Escritorio remoto
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método SetVirtualChannelOptions
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422085"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>IMsRdpClient:: SetVirtualChannelOptions (método)

Establece las opciones de canal virtual para el control ActiveX Escritorio remoto.

Llame a este método después de llamar al método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , pero antes de establecer una conexión con el método [**Connect**](imstscax-connect.md) . Este método establece opciones adicionales en los canales virtuales creados con **CreateVirtualChannels**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChanName* \[ de\]
</dt> <dd>

Nombre del canal virtual que se especificó en la llamada al método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*chanOptions* \[ de\]
</dt> <dd>

Opciones que se van a establecer para el canal virtual especificado por el parámetro *ChanName* . Para obtener una descripción de las opciones posibles, consulte [**Channel \_ Def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Un ejemplo del uso de este método sería declarar el canal como control remoto persistente mediante la configuración de **la \_ opción de canal \_ \_ \_ persistencia persistente de control remoto** . Esto significa que el canal no se cerrará cuando un control remoto se conecte o desconecte de la sesión conectada al cliente. Para obtener más información, consulte [Remote control remoto canales virtuales persistentes](remote-control-persistent-virtual-channels.md).

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**DEF. de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 






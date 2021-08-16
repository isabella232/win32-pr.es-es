---
description: Notifica a una aplicación que se ha completado una Conectar o desconexión programada previamente al dispositivo MTP/Bluetooth dispositivo.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: Método IConnectionRequestCallback::OnComplete (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843193"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback::OnComplete (método)

El **método OnComplete** notifica a una aplicación que se ha completado una solicitud de Conectar o desconexión programada previamente al dispositivo MTP/Bluetooth.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hrStatus* \[ En\]
</dt> <dd>

El estado de la solicitud para conectar o desconectar un dispositivo determinado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Una aplicación implementa la interfaz [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes.

Windows Dispositivos portátiles (WPD) llama a este método para notificar a una aplicación que se ha completado una solicitud programada previamente. La devolución de llamada proporcionada por la aplicación puede realizar un seguimiento de cada solicitud y cancelarla. Por lo tanto, si la aplicación necesita enviar varias solicitudes al mismo tiempo con el mismo objeto [**IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) a cada solicitud se le debe pasar un objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) único como parámetro de entrada a los métodos [**IPortableDeviceConnector::Conectar**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 





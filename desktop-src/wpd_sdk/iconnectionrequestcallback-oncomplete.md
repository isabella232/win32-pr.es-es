---
description: Notifica a una aplicación que se ha completado una solicitud de conexión o desconexión programada previamente al dispositivo MTP/Bluetooth.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Método IConnectionRequestCallback:: alcomplete (Devpkey. h)'
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
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911141"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>IConnectionRequestCallback:: alcomplete (método)

El método **alcomplete** notifica a una aplicación que se ha completado una solicitud de conexión o desconexión programada previamente al dispositivo MTP/Bluetooth.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hrStatus* \[ de\]
</dt> <dd>

El estado de la solicitud para conectar o desconectar un dispositivo determinado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Una aplicación implementa la interfaz [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes.

Dispositivos portátiles de Windows (WPD) llama a este método para notificar a una aplicación que se ha completado una solicitud programada previamente. La devolución de llamada proporcionada por la aplicación puede realizar un seguimiento de cada solicitud y cancelarla. Por lo tanto, si la aplicación necesita enviar varias solicitudes al mismo tiempo mediante el mismo objeto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , se debe pasar a cada solicitud un objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) único como parámetro de entrada a los métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) y [**IPortableDeviceConnector::D Ulta**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 





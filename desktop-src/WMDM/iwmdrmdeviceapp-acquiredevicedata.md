---
title: Método IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp.h)
description: El método AcquireDeviceData inicializa o restablece un reloj seguro del dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Método AcquireDeviceData de Windows Media Administrador de dispositivos
- Método AcquireDeviceData windows Media Administrador de dispositivos , interfaz IWMDRMDeviceApp
- IWMDRMDeviceApp interface windows Media Administrador de dispositivos , AcquireDeviceData method
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9280a358c7124a3f16e3d303026f36506610b6dc6fe0453fdf3e7b2432682719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055653"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>IWMDRMDeviceApp::AcquireDeviceData (método)

El **método AcquireDeviceData** inicializa o restablece un reloj seguro del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Puntero a una [**interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) para el dispositivo que va a notificar datos de medición.

</dd> <dt>

*pProgressCallback* \[ En\]
</dt> <dd>

Devolución de llamada de progreso a través de la cual la aplicación puede realizar un seguimiento del progreso del evento o cancelar el evento. El progreso se identifica mediante el *parámetro EventId* de [**los métodos IWMDMProgress3.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

UN **OR lógico** de una o ambas marcas siguientes, especificando la acción que se va a realizar. Este valor se recupera del parámetro *pdwStatus* de [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md). Puede usar la *marca pdwStatus* directamente.



| Marca                        | Descripción                                   |
|-----------------------------|-----------------------------------------------|
| \_NEEDCLOCK DEL DISPOSITIVO \_ WMDRM    | Adquirir un reloj de un servidor de reloj seguro.   |
| ACTUALIZACIÓN DE \_ DISPOSITIVO \_ WMDRMCLOCK | Actualice el reloj desde un servidor de reloj seguro. |



 

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Uno de los siguientes **valores DWORD** que especifica el estado devuelto por el dispositivo.



| Status | Descripción                                                     |
|--------|-----------------------------------------------------------------|
| 0      | No se admite la acción .                                    |
| 1      | No se pudo adquirir el reloj seguro del dispositivo del servicio. |
| 2      | No se pudo establecer el reloj seguro del dispositivo.                     |
| 3      | Se estableció el reloj seguro del dispositivo.                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                                             | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                    | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Uno o varios argumentos no son válidos.<br/>                                                                                     |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl>                        | El dispositivo especificado no es un dispositivo compatible Windows DRM multimedia.<br/>                                                       |
| <dl> <dt>**DRM DE \_ NS E \_ NO PUEDE OBTENER EL RELOJ \_ \_ \_ \_ \_ SEGURO**</dt> </dl>               | No se pudo recuperar el desafío de reloj seguro del dispositivo o no se pudo recuperar la dirección URL del reloj seguro del desafío.<br/> |
| <dl> <dt>**DRM DE \_ NS E \_ NO PUEDE OBTENER EL RELOJ SEGURO DEL \_ \_ \_ \_ \_ \_ \_ SERVIDOR**</dt> </dl> | No se pudo recuperar la respuesta del reloj seguro del servidor de reloj seguro.<br/>                                               |
| <dl> <dt>**DRM DE \_ NS E \_ NO SE PUEDE ESTABLECER EL RELOJ \_ \_ \_ \_ \_ SEGURO**</dt> </dl>               | No se pudo enviar el desafío de reloj seguro al dispositivo o el dispositivo no pudo establecer el reloj.<br/>                          |



 

## <a name="remarks"></a>Comentarios

Se trata de un método asincrónico; El dispositivo debe esperar la devolución de llamada [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) para esta operación antes de intentar reproducir cualquier contenido con licencia.

Una aplicación puede aprender si el dispositivo debe tener su reloj restablecido o actualizado llamando a [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).

La aplicación debe tener una conexión a Internet para poder adquirir o restablecer un reloj seguro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp i.c, creado a partir de \_ WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMDevice (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**IWMDMProgress3 (Interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp (interfaz)**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






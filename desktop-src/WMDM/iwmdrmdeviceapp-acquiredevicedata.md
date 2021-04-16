---
title: Método IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: El método AcquireDeviceData inicializa o restablece el reloj seguro de un dispositivo.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Método AcquireDeviceData de Windows Media Administrador de dispositivos
- Método AcquireDeviceData de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método AcquireDeviceData
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
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699682"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>IWMDRMDeviceApp:: AcquireDeviceData (método)

El método **AcquireDeviceData** inicializa o restablece el reloj seguro de un dispositivo.

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

*pDevice* \[ de\]
</dt> <dd>

Puntero a una interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) para el dispositivo que va a notificar los datos de medición.

</dd> <dt>

*pProgressCallback* \[ de\]
</dt> <dd>

Devolución de llamada de progreso a través de la cual la aplicación puede realizar el seguimiento del progreso del evento o cancelar el evento. El progreso se identifica mediante el parámetro *EventID* de los métodos [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un **or** lógico de uno o ambos de los siguientes marcadores, que especifican la acción que se va a realizar. Este valor se recupera del parámetro *pdwStatus* de [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md). Puede usar la marca *pdwStatus* directamente.



| Marca                        | Descripción                                   |
|-----------------------------|-----------------------------------------------|
| \_dispositivo \_ NEEDCLOCK de WMDRM    | Adquiera un reloj de un servidor de reloj seguro.   |
| \_dispositivo \_ REFRESHCLOCK de WMDRM | Actualice el reloj desde un servidor de reloj seguro. |



 

</dd> <dt>

*pdwStatus* \[ enuncia\]
</dt> <dd>

Uno de los siguientes valores **DWORD** que especifican el estado devuelto por el dispositivo.



| Status | Descripción                                                     |
|--------|-----------------------------------------------------------------|
| 0      | No se admite la acción.                                    |
| 1      | No se pudo adquirir el reloj seguro del dispositivo del servicio. |
| 2      | No se pudo establecer el reloj seguro del dispositivo.                     |
| 3      | Se estableció el reloj seguro del dispositivo.                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                                             | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                                    | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Uno o varios argumentos no son válidos.<br/>                                                                                     |
| <dl> <dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt> </dl>                        | El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.<br/>                                                       |
| <dl> <dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ reloj seguro**</dt> </dl>               | No se pudo recuperar el desafío del reloj seguro del dispositivo o no se pudo recuperar la dirección URL del reloj segura del desafío.<br/> |
| <dl> <dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ reloj seguro \_ del \_ servidor**</dt> </dl> | No se pudo recuperar la respuesta de reloj segura del servidor de reloj seguro.<br/>                                               |
| <dl> <dt>**\_DRM E \_ DRM \_ no \_ puede \_ establecer \_ el \_ reloj seguro**</dt> </dl>               | No se pudo enviar el desafío del reloj seguro al dispositivo o el dispositivo no pudo establecer el reloj.<br/>                          |



 

## <a name="remarks"></a>Observaciones

Se trata de un método asincrónico; el dispositivo debe esperar la devolución de llamada [**IWMDMProgress:: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) para esta operación antes de intentar reproducir cualquier contenido con licencia.

Una aplicación puede aprender si el dispositivo debe restablecer su reloj o actualizarse llamando a [**IWMDRMDeviceApp:: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) o [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).

La aplicación debe tener una conexión a Internet para que pueda adquirir o restablecer un reloj seguro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interfaz IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






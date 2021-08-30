---
title: Método IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp.h)
description: El método QueryDeviceStatus2 consulta un dispositivo para obtener un estado o una funcionalidad drm específicos.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Método QueryDeviceStatus2 windows Media Administrador de dispositivos
- Método QueryDeviceStatus2 windows Media Administrador de dispositivos interfaz , IWMDRMDeviceApp2
- IWMDRMDeviceApp2 interface windows Media Administrador de dispositivos , QueryDeviceStatus2 method
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2def2063498cc28de0f0e81efe4e34a382276e8d54466c5da321feea201e47a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031715"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>Método IWMDRMDeviceApp2::QueryDeviceStatus2

El **método QueryDeviceStatus2** consulta un dispositivo para obtener un estado o una funcionalidad drm específicos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Puntero a un [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Uno o varios de los siguientes valores **DWORD** que especifican las funcionalidades que se deben solicitar, combinados con un OR bit a **bit.**



| Marca                              | Descripción                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| \_INDIVSTATUS DEL CLIENTE DE CONSULTA \_ \_ WMDRM | Consulte si es necesario individualizar los componentes DRM del equipo.       |
| CLOCKSTATUS DEL DISPOSITIVO \_ DE \_ CONSULTA \_ WMDRM | Consulte si es necesario agregar o actualizar el reloj seguro del dispositivo.        |
| ISREVOKED DEL DISPOSITIVO DE CONSULTA \_ \_ \_ WMDRM   | Consulta si se revoca el dispositivo.                                         |
| \_ISWMDRM DEL DISPOSITIVO DE CONSULTA \_ \_ WMDRM     | Consulte si el dispositivo admite Windows DRM 10 multimedia para dispositivos portátiles. |



 

</dd> <dt>

*pdwStatus* \[ out\]
</dt> <dd>

Cero o más de los siguientes valores **DWORD** que especifican el estado del dispositivo solicitado, combinados con un OR bit a **bit.**



| Estado                      | Descripción                                              |
|-----------------------------|----------------------------------------------------------|
| \_ \_ ISWMDRM DEL DISPOSITIVO WMDRM      | El dispositivo admite drm Windows multimedia.                   |
| \_NEEDCLOCK DEL DISPOSITIVO \_ WMDRM    | El dispositivo no tiene un reloj seguro.                 |
| DISPOSITIVO WMDRM \_ \_ REVOCADO      | Se ha revocado el dispositivo.                             |
| NECESIDAD DE CLIENTE \_ \_ WMDRMINDIV    | Los componentes DRM del equipo deben individualizarse. |
| ACTUALIZACIÓN DE \_ DISPOSITIVO \_ WMDRMCLOCK | El reloj debe actualizarse.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | El método se ha llevado a cabo de forma correcta.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Uno o varios argumentos no son válidos.<br/>                           |
| <dl> <dt>**NS E DRM INVALID CERTIFICATE (CERTIFICADO NO VÁLIDO DE DRM DE NS \_ \_ \_ \_ E)**</dt> </dl>          | El certificado de dispositivo recuperado del dispositivo no es válido.<br/> |
| <dl> <dt>**DRM DE NS \_ E NO PUEDE OBTENER EL CERTIFICADO DE \_ \_ \_ \_ \_ \_ DISPOSITIVO**</dt> </dl> | No se pudo recuperar el certificado de dispositivo del dispositivo.<br/>     |



 

## <a name="remarks"></a>Comentarios

Se debe llamar a este método antes de realizar cualquier acción restringida en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición. Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (como la individualización para el escritorio o adquirir un reloj para el dispositivo), la aplicación debe llamar a [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor *pdwStatus* recuperado de esta función al parámetro *dwFlags* **de AcquireDeviceData.** Si se devuelve cero, el dispositivo no admite Windows DRM 10 multimedia para dispositivos portátiles y no es necesario realizar ninguna acción. Consulte [Control de contenido protegido en la aplicación para](handling-protected-content-in-the-application.md) obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp i.c, creado a partir de \_ WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**IWMDRMDeviceApp2 (interfaz)**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 






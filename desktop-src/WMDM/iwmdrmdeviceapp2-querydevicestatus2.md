---
title: Método IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: El método QueryDeviceStatus2 consulta un dispositivo para una funcionalidad o un estado DRM específico.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Método QueryDeviceStatus2 de Windows Media Administrador de dispositivos
- Método QueryDeviceStatus2 de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp2
- Interfaz IWMDRMDeviceApp2 de Windows Media Administrador de dispositivos, método QueryDeviceStatus2
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
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699802"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>IWMDRMDeviceApp2:: QueryDeviceStatus2 (método)

El método **QueryDeviceStatus2** consulta un dispositivo para una funcionalidad o un estado DRM específico.

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

*pDevice* \[ de\]
</dt> <dd>

Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Uno o varios de los siguientes valores **DWORD** que especifican las funciones que se van a solicitar, combinadas con **una operación OR** bit a bit.



| Marca                              | Descripción                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| \_INDIVSTATUS de \_ cliente de consulta WMDRM \_ | Consulte si los componentes DRM del equipo deben ser individualizados.       |
| \_dispositivo de consulta WMDRM \_ \_ CLOCKSTATUS | Consulte si es necesario agregar o actualizar el reloj seguro del dispositivo.        |
| \_dispositivo de consulta WMDRM \_ \_ ISREVOKED   | Consulta si el dispositivo se ha revocado.                                         |
| \_dispositivo de consulta WMDRM \_ \_ ISWMDRM     | Consulta si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles. |



 

</dd> <dt>

*pdwStatus* \[ enuncia\]
</dt> <dd>

Cero o más de los siguientes valores **DWORD** que especifican el estado de dispositivo solicitado, combinado con una operación **OR bit a** bit.



| Status                      | Descripción                                              |
|-----------------------------|----------------------------------------------------------|
| \_dispositivo \_ ISWMDRM de WMDRM      | El dispositivo es compatible con DRM de Windows Media.                   |
| \_dispositivo \_ NEEDCLOCK de WMDRM    | El dispositivo no tiene un reloj seguro.                 |
| \_dispositivo WMDRM \_ revocado      | El dispositivo se ha revocado.                             |
| \_NEEDINDIV de cliente WMDRM \_    | Los componentes de DRM del equipo deben ser individualizados. |
| \_dispositivo \_ REFRESHCLOCK de WMDRM | El reloj debe actualizarse.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                              | Descripción                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                     | El método se ha llevado a cabo de forma correcta.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Uno o varios argumentos no son válidos.<br/>                           |
| <dl> <dt>**\_ \_ \_ certificado no válido de DRM E DRM \_**</dt> </dl>          | El certificado de dispositivo recuperado del dispositivo no es válido.<br/> |
| <dl> <dt>**\_DRM E \_ DRM \_ no \_ puede \_ obtener \_ el \_ certificado del dispositivo**</dt> </dl> | No se pudo recuperar el certificado de dispositivo del dispositivo.<br/>     |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método antes de realizar cualquier acción restringida en el contenido DRM, como transferir contenido DRM al dispositivo o adquirir información de medición. Si los valores recuperados por *pdwStatus* indican que es necesario realizar alguna acción (por ejemplo, la individualización del escritorio o la adquisición de un reloj para el dispositivo), la aplicación debe llamar a [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) y pasar el valor de *pdwStatus* recuperado de esta función al parámetro *dwFlags* en **AcquireDeviceData**. Si se devuelve cero, el dispositivo no admite Windows Media DRM 10 para dispositivos portátiles y no es necesario realizar ninguna acción. Consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 






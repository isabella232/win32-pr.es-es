---
title: Método IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: El método SynchronizeLicenses actualiza las licencias en un dispositivo cuando están a la expiración.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Método SynchronizeLicenses de Windows Media Administrador de dispositivos
- Método SynchronizeLicenses de Windows Media Administrador de dispositivos, interfaz IWMDRMDeviceApp
- Interfaz IWMDRMDeviceApp de Windows Media Administrador de dispositivos, método SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699803"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>IWMDRMDeviceApp:: SynchronizeLicenses (método)

El método **SynchronizeLicenses** actualiza las licencias en un dispositivo cuando están a la expiración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Puntero a un objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pProgressCallback* \[ de\]
</dt> <dd>

Devolución de llamada de progreso que recibirá el progreso de los pasos que pueda necesitar llevar a cabo. El paso se identifica mediante el parámetro *EventID* del método [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) denominado.

</dd> <dt>

*cMinCountThreshold* \[ de\]
</dt> <dd>

Número mínimo opcional de recuento de reproducción restante en una licencia de dispositivo.

</dd> <dt>

*cMinHoursThreshold* \[ de\]
</dt> <dd>

Número mínimo opcional de horas restantes en una licencia de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                         | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Uno o varios argumentos no son válidos.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | XML tiene un formato incorrecto.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Esta funcionalidad no está implementada actualmente. (SyncLicenses w/ *pDevice* = null)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | El XML de la licencia tenía un formato incorrecto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | El XML de la licencia tenía un formato incorrecto.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OUTOFMEMORY**</dt> </dl>                  | Memoria insuficiente<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | No se pudo encontrar una etiqueta XML necesaria en la licencia.<br/>                                                                                                |
| <dl> <dt>**dispositivo \_ E \_ dispositivo \_ no \_ WMDRM \_**</dt> </dl>    | El dispositivo especificado no es un dispositivo compatible con DRM de Windows Media.<br/>                                                                               |
| <dl> <dt>**el \_ DRM de NS E \_ requiere la \_ \_ individualización**</dt> </dl> | DRM requiere un cuadro negro individual para realizar esta función. En otras palabras, el SDK de Windows Media Format requiere una actualización de seguridad.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta llamada solo se puede realizar en un dispositivo que admita Windows Media DRM 10 para dispositivos portátiles. Debe especificar al menos un parámetro de umbral.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp. h (también requiere Wmdrmdeviceapp \_ i, generado a partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaz IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interfaz IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






---
title: Método IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp.h)
description: El método SynchronizeLicenses actualiza las licencias de un dispositivo cuando están a punto de expirar.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Método SynchronizeLicenses windows Media Administrador de dispositivos
- Método SynchronizeLicenses de windows Media Administrador de dispositivos , interfaz IWMDRMDeviceApp
- IWMDRMDeviceApp interfaz windows Media Administrador de dispositivos , SynchronizeLicenses (método)
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
ms.openlocfilehash: 91ec48743bf52d990c64ce1aecf30897a7ee2f51664e88695a181f9d4f758140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031745"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>IWMDRMDeviceApp::SynchronizeLicenses (método)

El **método SynchronizeLicenses** actualiza las licencias de un dispositivo cuando están a punto de expirar.

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

*pDevice* \[ En\]
</dt> <dd>

Puntero a un [**objeto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

</dd> <dt>

*pProgressCallback* \[ En\]
</dt> <dd>

Devolución de llamada de progreso que recibirá el progreso de los pasos que tenga que llevar a cabo. El paso se identifica mediante el *parámetro EventId* del [**método IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) llamado.

</dd> <dt>

*cMinCountThreshold* \[ En\]
</dt> <dd>

Recuento mínimo de reproducción restante opcional en una licencia de dispositivo.

</dd> <dt>

*cMinHoursThreshold* \[ En\]
</dt> <dd>

Horas restantes mínimas opcionales en una licencia de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                                         | Descripción                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                | El método se ha llevado a cabo de forma correcta.<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Uno o varios argumentos no son válidos.<br/>                                                                                                             |
| <dl> <dt>**DRM \_ E \_ INVALIDXMLTAG**</dt> </dl>                | XML tiene un formato incorrecto.<br/>                                                                                                                        |
| <dl> <dt>**DRM \_ E \_ NOTIMPL**</dt> </dl>                      | Esta funcionalidad no está implementada actualmente. (SyncLicenses w/ *pDevice* =NULL)<br/>                                                               |
| <dl> <dt>**DRM \_ E \_ NOXMLCLOSETAG**</dt> </dl>                | El XML de licencia no se ha formado correctamente.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ NOXMLOPENTAG**</dt> </dl>                 | El XML de licencia no se ha formado correctamente.<br/>                                                                                                           |
| <dl> <dt>**DRM \_ E \_ OUTOFMEMORY**</dt> </dl>                  | Memoria insuficiente<br/>                                                                                                                                   |
| <dl> <dt>**DRM \_ E \_ XMLNOTFOUND**</dt> </dl>                  | No se pudo encontrar una etiqueta XML necesaria en la licencia.<br/>                                                                                                |
| <dl> <dt>**NS \_ E \_ DEVICE \_ NOT \_ WMDRM \_ DEVICE**</dt> </dl>    | El dispositivo especificado no es un Windows compatible con DRM multimedia.<br/>                                                                               |
| <dl> <dt>**DRM DE NS \_ E \_ NECESITA \_ \_ INDIVIDUALIZACIÓN**</dt> </dl> | Drm requiere una caja negra individualizada para realizar esta función. En otras palabras, el SDK Windows media format requiere una actualización de seguridad.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta llamada solo se puede realizar en un dispositivo que admita Windows DRM 10 multimedia para dispositivos portátiles. Debe especificar al menos un parámetro de umbral.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDRMDeviceApp.h (también requiere Wmdrmdeviceapp i.c, creado a partir de \_ WMDRMDeviceApp.idl)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDMProgress3 (Interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**IWMDRMDeviceApp (interfaz)**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






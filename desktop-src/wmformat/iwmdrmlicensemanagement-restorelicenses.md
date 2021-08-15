---
title: Método IWMDRMLicenseManagement RestoreLicenses (Wmdrmsdk.h)
description: El método RestoreLicenses restaura licencias a partir de una copia de seguridad de licencia que se creó mediante una llamada al método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Método RestoreLicenses windows Media Format
- Método RestoreLicenses windows Media Format , IWMDRMLicenseManagement (interfaz)
- IWMDRMLicenseManagement interface windows Media Format , RestoreLicenses method
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846943"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>IWMDRMLicenseManagement::RestoreLicenses (Método)

El **método RestoreLicenses** restaura licencias a partir de una copia de seguridad de licencia que se creó mediante una llamada [**al método BackupLicenses.**](iwmdrmlicensemanagement-backuplicenses.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrBackupDirectory* \[ En\]
</dt> <dd>

Ruta de acceso UNC de la ubicación desde la que se restaurarán las licencias.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de restauración que se usarán. La única marca admitida actualmente es WMDRM RESTORE INDIVIDUALIZE, que configura el método para realizar la individualización como parte de la \_ \_ restauración, si es necesario.

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método se ejecuta de forma asincrónica. Devuelve inmediatamente después de llamarse y, a continuación, genera una serie de eventos **MEWMDRMLicenseRestoreProgress** seguidos de un evento **MEWMDRMLicenseRestoreCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMLicenseRestoreProgress obtenidos** mediante una llamada a **IMFMediaEvent::GetValue** es un **puntero IUnknown.** Puede llamar al **método QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la [**interfaz IWMDRMLicenseBackupRestoreStatus.**](iwmdrmlicensebackuprestorestatus.md)

Para obtener más información sobre el uso de los métodos asincrónicos de Windows MEDIA DRM Client Extended API, vea [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

La copia de seguridad puede realizarse desde el equipo local o desde otro equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






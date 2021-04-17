---
title: Método IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: El método RestoreLicenses restaura las licencias de una copia de seguridad de licencias que se creó mediante una llamada al método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Método RestoreLicenses formato de Windows Media
- Método RestoreLicenses formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método RestoreLicenses
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
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718751"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>IWMDRMLicenseManagement:: RestoreLicenses (método)

El método **RestoreLicenses** restaura las licencias de una copia de seguridad de licencias que se creó mediante una llamada al método [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .

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

*bstrBackupDirectory* \[ de\]
</dt> <dd>

Ruta de acceso UNC de la ubicación desde la que se restaurarán las licencias.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones de restauración que se van a utilizar. La única marca admitida actualmente es la restauración de WMDRM \_ \_ individual, que configura el método para realizar una individualización como parte de la restauración, si es necesario.

</dd> <dt>

*ppunkCancelationCookie* \[ enuncia\]
</dt> <dd>

Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica. Vuelve inmediatamente después de llamarlo y, a continuación, genera una serie de eventos **MEWMDRMLicenseRestoreProgress** seguidos de un evento **MEWMDRMLicenseRestoreCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMLicenseRestoreProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** . Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).

La copia de seguridad puede estar en el equipo local o desde un equipo diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






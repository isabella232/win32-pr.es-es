---
title: Método IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: El método BackupLicenses crea una copia de seguridad de las licencias en el almacén de licencias local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Método BackupLicenses formato de Windows Media
- Método BackupLicenses formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718749"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>IWMDRMLicenseManagement:: BackupLicenses (método)

El método **BackupLicenses** crea una copia de seguridad de las licencias en el almacén de licencias local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrBackupDirectory* \[ de\]
</dt> <dd>

Ruta de acceso UNC de la ubicación en la que se realizará la copia de seguridad de las licencias.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones de copia de seguridad que se van a utilizar. La única marca admitida actualmente es \_ \_ sobrescribir la copia de seguridad de WMDRM, que configura el método para sobrescribir los archivos de copia de seguridad existentes en el directorio.

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

Este método se ejecuta de forma asincrónica. Vuelve inmediatamente después de llamarlo y, a continuación, genera una serie de eventos **MEWMDRMLicenseBackupProgress** seguidos de un evento **MEWMDRMLicenseBackupCompleted** cuando se completa el procesamiento. El valor de cada uno de los eventos **MEWMDRMLicenseBackupProgress** obtenidos mediante la llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** . Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).

No se permite realizar copias de seguridad de todas las licencias. Este método solo realiza una copia de seguridad de las licencias que lo permiten.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






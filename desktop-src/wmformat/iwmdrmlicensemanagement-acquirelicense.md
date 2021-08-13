---
title: Método IWMDRMLicenseManagement AcquireLicense (Wmdrmsdk.h)
description: El método AcquireLicense adquiere de forma asincrónica una licencia de una dirección URL especificada.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Formato multimedia de Windows del método AcquireLicense
- Formato multimedia de Windows del método AcquireLicense , interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interfaz windows Media Format , Método AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad8251650c8a7e16c6eb2fc957df5e70459239c0cd6cf1184b5209ae51b6aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701131"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>IWMDRMLicenseManagement::AcquireLicense (Método)

El **método AcquireLicense** adquiere de forma asincrónica una licencia de una dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* \[ En\]
</dt> <dd>

Dirección URL del servidor de licencias desde el que se va a adquirir la licencia. Pase **NULL** para que el método analice la dirección URL del encabezado de contenido.

</dd> <dt>

*bstrHeaderData* \[ En\]
</dt> <dd>

Encabezado de contenido que se va a pasar al servidor de licencias. Si *bstrURL* es **NULL,** el método analizará la dirección URL de este encabezado. Si *dwFlags se* establece en WMDRM \_ ACQUIRE LICENSE \_ \_ LEGACY NONSILENT, establezca este valor en el identificador de clave en lugar del \_ encabezado de contenido completo.

</dd> <dt>

*bstrActions* \[ En\]
</dt> <dd>

Cadena que contiene cero o más acciones para las que se va a solicitar permiso en la licencia. La cadena debe tener el formato siguiente:

-   Cada acción debe definirse dentro de un elemento ACTION. Los datos del elemento son la cadena de acción.
-   Todos los elementos ACTION deben estar incluidos dentro de un elemento ACTIONLIST.

    Por ejemplo, la cadena para solicitar una licencia para reproducir contenido tiene el formato siguiente:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas de opción de adquisición de licencias. Establezca en una de las constantes de la tabla siguiente.



| Constante                                   | Descripción                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ADQUISICIÓN SILENCIOSA \_ DE \_ LICENCIAS DE \_ WMDRM            | La licencia se emitirá directamente a través de Internet sin confirmación de la aplicación cliente.              |
| WMDRM \_ ACQUIRE \_ LICENSE \_ NONSILENT         | El subsistema DRM creará una solicitud de licencia que se devolverá de forma asincrónica para su publicación en el servidor de licencias. |
| WMDRM \_ ACQUIRE \_ LICENSE \_ LEGACY \_ NONSILENT | Igual que WMDRM \_ ACQUIRE \_ LICENSE NONSILENT, salvo que se creará un desafío de licencia de DRM versión \_ 1.           |



 

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al [**método IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica. Devuelve inmediatamente después de llamarse y, a continuación, genera un evento **MEWMDRMLicenseAcquisitionCompleted** cuando se completa el procesamiento. En el caso de las operaciones de adquisición de licencias no silenciosas, el valor del evento obtenido mediante una llamada a **IMFMediaEvent::GetValue** es un **puntero IUnknown.** Puede llamar al **método QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la [**interfaz IWMDRMNonSilentLicenseAquisition.**](iwmdrmnonsilentlicenseaquisition.md)

Para obtener más información sobre el uso de los métodos asincrónicos de Windows MEDIA DRM Client Extended API, vea [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Adquisición silenciosa de licencias**](silent-license-acquisition.md)
</dt> </dl>

 

 






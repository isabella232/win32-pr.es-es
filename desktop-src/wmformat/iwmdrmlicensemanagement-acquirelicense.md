---
title: Método AcquireLicense de IWMDRMLicenseManagement (wmdrmsdk. h)
description: El método AcquireLicense adquiere de forma asincrónica una licencia de una dirección URL especificada.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Método AcquireLicense de Windows Media Format
- Método AcquireLicense formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método AcquireLicense
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
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708804"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>IWMDRMLicenseManagement:: AcquireLicense (método)

El método **AcquireLicense** adquiere de forma asincrónica una licencia de una dirección URL especificada.

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

*bstrURL* \[ de\]
</dt> <dd>

Dirección URL del servidor de licencias del que se va a adquirir la licencia. Pase **null** para que el método analice la dirección URL del encabezado de contenido.

</dd> <dt>

*bstrHeaderData* \[ de\]
</dt> <dd>

Encabezado de contenido que se va a pasar al servidor de licencias. Si *bstrURL* es **null**, el método analizará la dirección URL de este encabezado. Si *dwFlags* se establece en \_ la licencia de adquisición de WMDRM Legacy no \_ \_ \_ Silent, establezca este valor en el identificador de clave en lugar del encabezado de contenido completo.

</dd> <dt>

*bstrActions* \[ de\]
</dt> <dd>

Cadena que contiene cero o más acciones para las que se va a solicitar permiso en la licencia. La cadena debe tener el formato siguiente:

-   Cada acción debe definirse dentro de un elemento ACTION. Los datos del elemento son la cadena de acción.
-   Todos los elementos ACTION deben estar contenidos dentro de un elemento ACTIONLIST.

    Por ejemplo, la cadena para solicitar una licencia para reproducir contenido tiene el formato siguiente:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas de opciones de adquisición de licencias. Establezca en una de las constantes de la tabla siguiente.



| Constante                                   | Descripción                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| la licencia de adquisición de WMDRM es \_ \_ \_ silenciosa            | La licencia se emitirá directamente a través de Internet sin confirmación de la aplicación cliente.              |
| la licencia de adquisición de WMDRM no es \_ \_ \_ silenciosa         | El subsistema DRM creará una solicitud de licencia que se devolverá de forma asincrónica para publicarla en el servidor de licencias. |
| licencia de adquisición de WMDRM \_ \_ \_ HEREDAda no \_ silenciosa | Lo mismo que la licencia de adquisición de WMDRM no \_ \_ \_ es silenciosa, salvo que se creará un desafío de licencia de la versión 1 de DRM.           |



 

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

Este método se ejecuta de forma asincrónica. Vuelve inmediatamente después de llamarlo y, a continuación, genera un evento **MEWMDRMLicenseAcquisitionCompleted** cuando se completa el procesamiento. Para las operaciones de adquisición de licencias no silenciosas, el valor del evento obtenido mediante una llamada a **IMFMediaEvent:: GetValue** es un puntero **IUnknown** . Puede llamar al método **QueryInterface** de la interfaz **IUnknown** recuperada para obtener una instancia de la interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .

Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Adquisición de licencias silenciosa**](silent-license-acquisition.md)
</dt> </dl>

 

 






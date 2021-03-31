---
title: Adquisición de licencias no silenciosa
description: Adquisición de licencias no silenciosa
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- SDK de Windows Media Format, adquisición de licencias no silenciosas
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), adquisición de licencias no silenciosas
- DRM (administración de derechos digitales), adquisición de licencias no silenciosas
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias no silenciosas
- API extendidas de cliente, adquisición de licencias no silenciosas
- adquisición de licencias no silenciosa
- licencias, adquisición de licencias no silenciosas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532440"
---
# <a name="non-silent-license-acquisition"></a>Adquisición de licencias no silenciosa

La adquisición de licencias no silenciosa permite al proveedor de licencias interactuar con el usuario final a través de una página web, como un paso intermedio en el proceso de adquisición de licencias. La adquisición de licencias no silenciosas se inicia en respuesta a un usuario que intenta tener acceso a contenido protegido.

Para realizar una adquisición de licencias no silenciosa, siga estos pasos:

1.  Llame al método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Pase el encabezado DRM del archivo protegido como el parámetro *bstrHeaderData* . Especifique los derechos que desea conceder a la licencia en el parámetro *bstrActions* . Por último, establezca el parámetro *dwFlags* en la licencia de adquisición de WMDRM no es \_ \_ \_ silenciosa.
2.  Eventos de captura para la interfaz **IWMDRMLicenseManagement** . Cuando reciba el evento **MEWMDRMLicenseAcquisitionCompleted** , obtenga su valor asociado llamando a **IMFMediaEvent:: GetValue**. El valor debe ser de tipo VT \_ Unknown, un puntero a una interfaz **IUnknown** .
3.  Llame al método **QueryInterface** de la interfaz **IUnknown** recuperada en el paso 2 para obtener la interfaz [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .
4.  Llame a [**IWMDRMNonSilentLicenseAquisition:: GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) para recuperar el desafío de licencia. También debe llamar a [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) si ya no tiene la dirección URL del servidor de licencias.
5.  Envíe el desafío a la Página Web especificada por la dirección URL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Usar el modelo de eventos Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 





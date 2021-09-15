---
title: Adquisición de licencias no silenciosas
description: Adquisición de licencias no silenciosas
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows SDK de formato multimedia, adquisición de licencias no silenciosas
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), adquisición de licencias no silenciosas
- DRM (administración de derechos digitales), adquisición de licencias no silenciosas
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, adquisición de licencias no silenciosas
- API extendidas de cliente, adquisición de licencias no silenciosas
- adquisición de licencias no silenciosas
- licencias, adquisición de licencias no silenciosas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360208"
---
# <a name="non-silent-license-acquisition"></a>Adquisición de licencias no silenciosas

La adquisición de licencias no silenciosas permite al proveedor de licencias interactuar con el usuario final a través de una página web, como paso intermedio en el proceso de adquisición de licencias. La adquisición de licencias no silenciosas se inicia en respuesta a un usuario que intenta acceder al contenido protegido.

Para realizar la adquisición de licencias no silenciosas, siga estos pasos:

1.  Llame al [**método IWMDRMLicenseManagement::AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md) Pase el encabezado DRM del archivo protegido como *parámetro bstrHeaderData.* Especifique los derechos que desea que conceda la licencia en el *parámetro bstrActions.* Por último, establezca el *parámetro dwFlags* en WMDRM \_ ACQUIRE LICENSE \_ \_ NONSILENT.
2.  Captura de eventos para **la interfaz IWMDRMLicenseManagement.** Cuando reciba el **evento MEWMDRMLicenseAcquisitionCompleted,** obtenga su valor asociado llamando a **IMFMediaEvent::GetValue**. El valor debe ser de tipo VT \_ UNKNOWN, un puntero a una **interfaz IUnknown.**
3.  Llame al **método QueryInterface** de la **interfaz IUnknown** recuperada en el paso 2 para obtener la [**interfaz IWMDRMNonSilentLicenseAquisition.**](iwmdrmnonsilentlicenseaquisition.md)
4.  Llame [**a IWMDRMNonSilentLicenseAquisition::GetChallenge para**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) recuperar el desafío de licencia. Llame también [**a IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) si aún no tiene la dirección URL del servidor de licencias.
5.  Envíe el desafío a la página web especificada por la dirección URL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modelo Media Foundation eventos**](using-the-media-foundation-model.md)
</dt> </dl>

 

 





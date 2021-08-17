---
title: Adquisición silenciosa de licencias
description: Adquisición silenciosa de licencias
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows SDK de formato multimedia, adquisición silenciosa de licencias
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), adquisición silenciosa de licencias
- DRM (administración de derechos digitales), adquisición silenciosa de licencias
- administración de derechos digitales (DRM),licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, adquisición silenciosa de licencias
- API extendidas de cliente, adquisición silenciosa de licencias
- adquisición silenciosa de licencias
- licenses,silent license acquisition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eff454ce673230f0c7dbe6f64afbf46e9bbe8b5f948609f5fb67d647a4151ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197467"
---
# <a name="silent-license-acquisition"></a>Adquisición silenciosa de licencias

La adquisición silenciosa de licencias solo requiere una sola llamada de método que controle todas las comunicaciones de red con el servidor de licencias de forma asincrónica.

Este tipo de adquisición de licencias normalmente se usa como respuesta al usuario final que intenta acceder a contenido protegido, por ejemplo, intentando reproducir un archivo protegido en una aplicación del reproductor multimedia. Dado que la adquisición de licencias silenciosas obtiene la licencia con una sola llamada, no se puede usar si se requiere una entrada adicional del usuario, como el pago por el contenido.

Para realizar la adquisición silenciosa de licencias, siga estos pasos:

1.  Llame al [**método IWMDRMLicenseManagement::AcquireLicense.**](iwmdrmlicensemanagement-acquirelicense.md) Pase el encabezado DRM del archivo protegido como *parámetro bstrHeaderData.* Especifique los derechos que desea que conceda la licencia en el *parámetro bstrActions.* Por último, establezca el *parámetro dwFlags* en WMDRM \_ ACQUIRE LICENSE \_ \_ SILENT.
2.  Captura de eventos para [**la interfaz IWMDRMLicenseManagement.**](iwmdrmlicensemanagement.md) Cuando reciba el evento **MEWMDRMLicenseAcquisitionCompleted,** compruebe su código de retorno llamando al método **IMFMediaEvent::GetStatus,** que se documenta en la documentación Media Foundation datos. Si el valor **HRESULT** recuperado es un código correcto, la licencia se descargó correctamente y está en el almacén de licencias local listo para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Uso del Media Foundation de eventos**](using-the-media-foundation-model.md)
</dt> </dl>

 

 





---
title: Adquisición de licencias silenciosa
description: Adquisición de licencias silenciosa
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- SDK de Windows Media Format, adquisición de licencias silenciosa
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), adquisición de licencias silenciosa
- DRM (administración de derechos digitales), adquisición de licencias silenciosa
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias silenciosa
- API extendidas de cliente, adquisición de licencias silenciosa
- adquisición de licencias silenciosa
- licencias, adquisición de licencias silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076010"
---
# <a name="silent-license-acquisition"></a>Adquisición de licencias silenciosa

La adquisición de licencias silenciosa solo requiere una única llamada de método que controle todas las comunicaciones de red con el servidor de licencias de forma asincrónica.

Este tipo de adquisición de licencias se usa normalmente como respuesta al usuario final que intenta tener acceso al contenido protegido, por ejemplo, intentando reproducir un archivo protegido en una aplicación del reproductor de media. Dado que la adquisición de licencia silenciosa obtiene la licencia con una sola llamada, no se puede usar si se requiere una entrada adicional del usuario, como el pago del contenido.

Para realizar una adquisición de licencias silenciosa, siga estos pasos:

1.  Llame al método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Pase el encabezado DRM del archivo protegido como el parámetro *bstrHeaderData* . Especifique los derechos que desea conceder a la licencia en el parámetro *bstrActions* . Por último, establezca el parámetro *dwFlags* en la licencia de adquisición de WMDRM en \_ \_ \_ modo silencioso.
2.  Eventos de captura para la interfaz [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) . Cuando reciba el evento **MEWMDRMLicenseAcquisitionCompleted** , compruebe su código de retorno llamando al método **IMFMediaEvent:: getStatus** , que se documenta en la documentación de Media Foundation. Si el valor **HRESULT** recuperado es un código de éxito, la licencia se descargó correctamente y está en el almacén de licencias local listo para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Usar el modelo de eventos Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 





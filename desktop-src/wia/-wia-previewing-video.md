---
description: La interfaz IWiaVideo permite a una aplicación ver vídeo y capturar imágenes fijas de ella.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Vista previa de vídeo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca270adf4e6461beac409315c782101744e8afeb72c33f07aa7bbc999e24751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813725"
---
# <a name="previewing-video-wia"></a>Vista previa de vídeo (WIA)

La [**interfaz IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) permite a una aplicación ver vídeo y capturar imágenes fijas de ella. Realice los pasos siguientes para seleccionar el dispositivo de streaming de vídeo y mostrar una secuencia de vídeo en una ventana.

-   Llame [a CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar un puntero a la [**interfaz IWiaDevMgr.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)
-   Use el [**método IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) de la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) para obtener un puntero a la interfaz [**INFO de IEnumWIA \_ DEV. \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Para obtener instrucciones sobre cómo enumerar dispositivos, consulte Enumeración de dispositivos del sistema.
-   Use la interfaz INFO de [**IEnumWIA \_ DEV \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obtener un puntero de interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo Windows adquisición de imágenes (WIA) encontrado.
-   Use la [**interfaz IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obtener la propiedad DeviceID del dispositivo deseado. Un dispositivo de vídeo de streaming tiene la marcaDeviceTypeStreamingVideo del conjunto de propiedades WIA \_ DIP \_ DEV \_ TYPE.
-   Use la [**interfaz IWiaPropertyStorage para**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) obtener el valor de la propiedad DIRECTORY DE \_ WIA DPV \_ \_ IMAGES.
-   Llame [a CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar un puntero a la [**interfaz IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)
-   Establezca la [**propiedad IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de la [**interfaz IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) en el valor recibido del valor de la propiedad DIRECTORY DE WIA \_ DPV \_ \_ IMAGES.
-   Llame [**a IWiaVideo::CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) en la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) y pase el identificador de dispositivo del dispositivo de imagen de streaming y el identificador de la ventana en la que se va a mostrar el vídeo.

> [!Note]  
> WIA no admite dispositivos de vídeo en Windows Server 2003, Windows Vista ni versiones posteriores. Para esas versiones de la Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes a partir de vídeo.

 

 

 

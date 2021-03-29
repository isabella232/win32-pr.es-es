---
description: La interfaz IWiaVideo permite a una aplicación ver vídeo y capturar imágenes estáticas.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Obtener una vista previa del vídeo (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541931"
---
# <a name="previewing-video-wia"></a>Obtener una vista previa del vídeo (WIA)

La interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) permite a una aplicación ver vídeo y capturar imágenes estáticas. Realice los pasos siguientes para seleccionar el dispositivo de vídeo de streaming y mostrar un flujo de vídeo en una ventana.

-   Llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar un puntero a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) .
-   Use el método [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) de la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) para obtener un puntero a la interfaz [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Para obtener instrucciones sobre cómo enumerar dispositivos, consulte enumerar dispositivos del sistema.
-   Use la interfaz [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) para obtener un puntero de interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para cada dispositivo de adquisición de imágenes de Windows (WIA) encontrado.
-   Use la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obtener la propiedad DeviceID del dispositivo deseado. Un dispositivo de vídeo de transmisión por secuencias tiene la marca StiDeviceTypeStreamingVideo del \_ conjunto de propiedades de tipo de dev DIP para WIA \_ \_ .
-   Use la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para obtener el valor de la \_ propiedad de directorio WIA DPV \_ images \_ .
-   Llame a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar un puntero a la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .
-   Establezca la propiedad [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) en el valor recibido del valor de la propiedad de \_ directorio WIA DPV \_ images \_ .
-   Llame a [**IWiaVideo:: CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) en la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , pasando el identificador de dispositivo del dispositivo de imagen de streaming y el identificador de la ventana en la que se va a mostrar el vídeo.

> [!Note]  
> WIA no admite dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior. En el caso de las versiones de Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes del vídeo.

 

 

 

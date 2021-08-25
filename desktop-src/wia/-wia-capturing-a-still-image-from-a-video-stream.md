---
description: Después de comenzar la vista previa de una secuencia de vídeo, llame al método IWiaVideo::TakePicture de la interfaz IWiaVideo para capturar una imagen fija del vídeo de streaming.
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Captura de una imagen fija desde una secuencia de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814285"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Captura de una imagen fija desde una secuencia de vídeo

Después de comenzar la vista previa de una secuencia de vídeo, llame al método [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar una imagen fija del vídeo de streaming. Para obtener instrucciones sobre cómo obtener un **puntero IWiaVideo** y empezar a obtener una vista previa del vídeo de streaming, consulte [Vista previa de vídeo.](-wia-previewing-video.md)

Cuando el [**método IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) devuelve , el parámetro *pbstrNewImageFilename* contiene la ruta de acceso completa y el nombre de archivo del archivo de imagen resultante. El archivo está en formato JPEG. El directorio en el que se crea el archivo se especifica mediante el valor de la propiedad [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de la [**interfaz IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)

> [!Note]  
> Windows Adquisición de imágenes (WIA) no admite dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior. Para esas versiones de la Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes de vídeo.

 

 

 

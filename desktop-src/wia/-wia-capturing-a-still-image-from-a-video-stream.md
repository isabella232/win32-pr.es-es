---
description: 'Después de comenzar la vista previa de una secuencia de vídeo, llame al método IWiaVideo:: TakePicture de la interfaz IWiaVideo para capturar una imagen del vídeo de streaming.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Capturar una imagen de un flujo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276862"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Capturar una imagen de un flujo de vídeo

Después de comenzar la vista previa de una secuencia de vídeo, llame al método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar una imagen del vídeo de streaming. Para obtener instrucciones sobre cómo obtener un puntero **IWiaVideo** y comenzar a obtener una vista previa del vídeo de streaming, vea obtener una [vista previa del vídeo](-wia-previewing-video.md).

Cuando el método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) devuelve, el parámetro *pbstrNewImageFilename* contiene la ruta de acceso completa y el nombre de archivo del archivo de imagen resultante. El archivo está en formato JPEG. El directorio en el que se crea el archivo se especifica mediante el valor de la propiedad [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> La adquisición de imágenes de Windows (WIA) no es compatible con dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior. En el caso de las versiones de Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes del vídeo.

 

 

 

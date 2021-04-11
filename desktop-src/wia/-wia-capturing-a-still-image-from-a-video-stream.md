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
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="36ee3-103">Capturar una imagen de un flujo de vídeo</span><span class="sxs-lookup"><span data-stu-id="36ee3-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="36ee3-104">Después de comenzar la vista previa de una secuencia de vídeo, llame al método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) para capturar una imagen del vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="36ee3-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="36ee3-105">Para obtener instrucciones sobre cómo obtener un puntero **IWiaVideo** y comenzar a obtener una vista previa del vídeo de streaming, vea obtener una [vista previa del vídeo](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="36ee3-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="36ee3-106">Cuando el método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) devuelve, el parámetro *pbstrNewImageFilename* contiene la ruta de acceso completa y el nombre de archivo del archivo de imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="36ee3-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="36ee3-107">El archivo está en formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="36ee3-107">The file is in JPEG format.</span></span> <span data-ttu-id="36ee3-108">El directorio en el que se crea el archivo se especifica mediante el valor de la propiedad [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) de la interfaz [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .</span><span class="sxs-lookup"><span data-stu-id="36ee3-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="36ee3-109">La adquisición de imágenes de Windows (WIA) no es compatible con dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="36ee3-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="36ee3-110">En el caso de las versiones de Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes del vídeo.</span><span class="sxs-lookup"><span data-stu-id="36ee3-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 

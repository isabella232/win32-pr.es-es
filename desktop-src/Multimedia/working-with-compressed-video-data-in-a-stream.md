---
title: Trabajar con datos de vídeo comprimidos en un flujo
description: Trabajar con datos de vídeo comprimidos en un flujo
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077646"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="85d30-103">Trabajar con datos de vídeo comprimidos en un flujo</span><span class="sxs-lookup"><span data-stu-id="85d30-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="85d30-104">AVIFile proporciona varias maneras de tener acceso a las secuencias de vídeo comprimidas.</span><span class="sxs-lookup"><span data-stu-id="85d30-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="85d30-105">Si desea mostrar uno o varios fotogramas de un flujo de vídeo comprimido, puede recuperar los fotogramas mediante la función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) y reenviar los datos del marco comprimido a las funciones DrawDib para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="85d30-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="85d30-106">Las funciones DrawDib pueden mostrar imágenes de varias profundidades de imagen y tramas automáticas de imágenes para las pantallas que no pueden controlar determinados tipos de mapas de bits independientes del dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="85d30-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="85d30-107">Estas funciones funcionan con imágenes sin comprimir y comprimidas.</span><span class="sxs-lookup"><span data-stu-id="85d30-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="85d30-108">Para obtener más información sobre las funciones de DrawDib, consulte [funciones de DrawDib](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="85d30-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="85d30-109">AVIFile proporciona funciones para descomprimir un solo fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85d30-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="85d30-110">Para asignar recursos, use la función [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) .</span><span class="sxs-lookup"><span data-stu-id="85d30-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="85d30-111">Esta función crea un búfer para los datos descomprimidos.</span><span class="sxs-lookup"><span data-stu-id="85d30-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="85d30-112">Puede descomprimir un solo fotograma de vídeo mediante la función [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) .</span><span class="sxs-lookup"><span data-stu-id="85d30-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="85d30-113">Esta función descomprime el marco y recupera un marco completo de datos de imagen, y devuelve la dirección del DIB en la estructura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="85d30-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="85d30-114">La aplicación puede mostrar el DIB mediante funciones de dibujo estándar o mediante las funciones de DrawDib.</span><span class="sxs-lookup"><span data-stu-id="85d30-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="85d30-115">Si la aplicación realiza llamadas sucesivas a **AVIStreamGetFrame**, la función sobrescribe su búfer con cada fotograma recuperado.</span><span class="sxs-lookup"><span data-stu-id="85d30-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="85d30-116">Cuando termine de usar **AVIStreamGetFrame** y el DIB descomprimido está en su búfer, puede liberar los recursos asignados mediante la función [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .</span><span class="sxs-lookup"><span data-stu-id="85d30-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="85d30-117">Para obtener más información sobre la descompresión de imágenes, consulte [Administrador de compresión de vídeo](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="85d30-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 
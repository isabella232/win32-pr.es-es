---
description: Ejemplo de VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Ejemplo de VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908365"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="0063b-103">Ejemplo de VMRPlayer</span><span class="sxs-lookup"><span data-stu-id="0063b-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="0063b-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="0063b-104">Description</span></span>

<span data-ttu-id="0063b-105">Este ejemplo usa el filtro de mezclador de vídeo 9 (VMR-9) para mezclar uno o dos vídeos en ejecución y una imagen estática.</span><span class="sxs-lookup"><span data-stu-id="0063b-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="0063b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0063b-106">Usage</span></span>

<span data-ttu-id="0063b-107">Para abrir el primer vídeo, elija **abrir flujo principal** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="0063b-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="0063b-108">Para abrir un segundo vídeo, elija **abrir flujo secundario** en el menú **archivo** (primero debe abrir el flujo principal).</span><span class="sxs-lookup"><span data-stu-id="0063b-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="0063b-109">Para reproducir el vídeo, haga clic en el botón **reproducir** .</span><span class="sxs-lookup"><span data-stu-id="0063b-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="0063b-110">Puede establecer la posición, el tamaño y los valores alfa de los vídeos seleccionando **flujo principal** o **secuencia de Secondard** desde el menú de **propiedades de VMR** .</span><span class="sxs-lookup"><span data-stu-id="0063b-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="0063b-111">Para agregar un mapa de bits estático sobre el vídeo, elija **imagen de aplicación estática** en el menú de **propiedades de VMR** y haga clic en el cuadro **Mostrar imagen de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="0063b-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="0063b-112">Puede usar el mismo cuadro de diálogo para controlar la posición, el tamaño y el valor alfa del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="0063b-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="0063b-113">Para capturar la imagen de vídeo combinada, elija **capturar imagen de mapa de bits** en el menú de **propiedades de VMR** .</span><span class="sxs-lookup"><span data-stu-id="0063b-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="0063b-114">También puede especificar la secuencia de imagen principal desde la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="0063b-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="0063b-115">**VMRPlayer** **/p** *nombrearchivo*</span><span class="sxs-lookup"><span data-stu-id="0063b-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="0063b-116">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0063b-116">Downloading the Sample</span></span>

<span data-ttu-id="0063b-117">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0063b-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0063b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0063b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0063b-119">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0063b-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




---
description: Ejemplo de filtros de origen de la instalación
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Ejemplo de filtros de origen de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537150"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="877f3-103">Ejemplo de filtros de origen de la instalación</span><span class="sxs-lookup"><span data-stu-id="877f3-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="877f3-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="877f3-104">Description</span></span>

<span data-ttu-id="877f3-105">Este ejemplo consta de un conjunto de tres filtros de origen que proporcionan los siguientes datos de origen como una secuencia de vídeo:</span><span class="sxs-lookup"><span data-stu-id="877f3-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="877f3-106">CPushSourceBitmap: mapa de bits único (cargado desde el directorio actual)</span><span class="sxs-lookup"><span data-stu-id="877f3-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="877f3-107">CPushSourceBitmapSet: conjunto de mapas de bits (cargados desde el directorio actual)</span><span class="sxs-lookup"><span data-stu-id="877f3-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="877f3-108">CPushSourceDesktop: copia de la imagen de escritorio actual (solo GDI)</span><span class="sxs-lookup"><span data-stu-id="877f3-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="877f3-109">Uso</span><span class="sxs-lookup"><span data-stu-id="877f3-109">Usage</span></span>

<span data-ttu-id="877f3-110">Para usar un filtro, cárguelo en GraphEdit y represente su PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="877f3-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="877f3-111">Esto conectará un representador de vídeo (y posiblemente un filtro de convertidor de espacio de colores) y le permitirá mostrar la salida.</span><span class="sxs-lookup"><span data-stu-id="877f3-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="877f3-112">Si desea representar el resultado en un archivo AVI, cárguelo, cargue el filtro del escritor de archivos, proporcione un nombre de salida al escritor de archivos y represente el PIN de salida del filtro PushSource.</span><span class="sxs-lookup"><span data-stu-id="877f3-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="877f3-113">También puede cargar y conectar compresores de vídeo, efectos de vídeo, etc.</span><span class="sxs-lookup"><span data-stu-id="877f3-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="877f3-114">El filtro de captura del escritorio no es compatible con las superposiciones de hardware, por lo que no capturará el vídeo representado en una superficie de superposición o los cursores que se muestran a través de la superposición de hardware.</span><span class="sxs-lookup"><span data-stu-id="877f3-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="877f3-115">Usa GDI para convertir la imagen de escritorio actual en un mapa de bits, que se pasa al pin de salida como un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="877f3-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="877f3-116">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="877f3-116">Downloading the Sample</span></span>

<span data-ttu-id="877f3-117">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="877f3-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="877f3-118">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ PushSource.</span><span class="sxs-lookup"><span data-stu-id="877f3-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="877f3-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="877f3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877f3-120">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="877f3-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




---
description: Ejemplo de filtro de volcado de memoria
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Ejemplo de filtro de volcado de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537965"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="580a5-103">Ejemplo de filtro de volcado de memoria</span><span class="sxs-lookup"><span data-stu-id="580a5-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="580a5-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="580a5-104">Description</span></span>

<span data-ttu-id="580a5-105">El filtro de volcado es un filtro de representador que escribe los ejemplos de medios que recibe en un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="580a5-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="580a5-106">En este ejemplo se muestra cómo usar la clase de filtro base [**CBaseFilter**](cbasefilter.md) y la clase de PIN de entrada representada [**CRenderedInputPin**](crenderedinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="580a5-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="580a5-107">También se muestra cómo implementar la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) .</span><span class="sxs-lookup"><span data-stu-id="580a5-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="580a5-108">El filtro de volcado tiene un solo PIN de entrada, que escribe cada ejemplo que recibe directamente en un archivo.</span><span class="sxs-lookup"><span data-stu-id="580a5-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="580a5-109">Uso</span><span class="sxs-lookup"><span data-stu-id="580a5-109">Usage</span></span>

<span data-ttu-id="580a5-110">Este filtro es una herramienta de depuración útil.</span><span class="sxs-lookup"><span data-stu-id="580a5-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="580a5-111">Por ejemplo, puede comprobar, bit a bit, los resultados de un filtro de transformación.</span><span class="sxs-lookup"><span data-stu-id="580a5-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="580a5-112">Puede compilar un gráfico manualmente mediante GraphEdit y conectar el filtro de volcado a la salida de un filtro de transformación o cualquier otro PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="580a5-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="580a5-113">También puede conectar un filtro tee y colocar el filtro de volcado en un segmento del filtro tee y el resultado típico en otro segmento para supervisar los resultados en un escenario en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="580a5-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="580a5-114">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="580a5-114">Downloading the Sample</span></span>

<span data-ttu-id="580a5-115">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="580a5-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="580a5-116">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz del SDK* de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="580a5-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="580a5-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="580a5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="580a5-118">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="580a5-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




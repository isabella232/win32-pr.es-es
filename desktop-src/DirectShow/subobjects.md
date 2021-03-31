---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911701"
---
# <a name="subobjects"></a><span data-ttu-id="77285-103">Subobjetos</span><span class="sxs-lookup"><span data-stu-id="77285-103">Subobjects</span></span>

<span data-ttu-id="77285-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="77285-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="77285-105">Los orígenes, los efectos y las transiciones tienen punteros internos a otros objetos COM, denominados *subobjetos*.</span><span class="sxs-lookup"><span data-stu-id="77285-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="77285-106">El subobjeto realiza el trabajo real del objeto.</span><span class="sxs-lookup"><span data-stu-id="77285-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="77285-107">El subobjeto de un origen es el componente que crea los datos de vídeo o audio.</span><span class="sxs-lookup"><span data-stu-id="77285-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="77285-108">El subobjeto de un efecto o transición es el componente que transforma los datos. por ejemplo, en un efecto de vídeo, crea el efecto visual en el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="77285-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="77285-109">El tipo de subobjeto depende del tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="77285-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="77285-110">Origen: cualquier filtro de origen de DirectShow o filtro de analizador que admita búsquedas y genere un formato compatible con DES.</span><span class="sxs-lookup"><span data-stu-id="77285-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="77285-111">Puede ser un formato comprimido si existen filtros de DirectShow para descodificarlo.</span><span class="sxs-lookup"><span data-stu-id="77285-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="77285-112">Efecto: para el vídeo, cualquier objeto de transformación de® de Microsoft® DirectX de una entrada de una sola entrada.</span><span class="sxs-lookup"><span data-stu-id="77285-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="77285-113">En audio, cualquier filtro de efecto de audio de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="77285-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="77285-114">Transición: para vídeo, cualquier objeto de transformación de DirectX de dos entradas 2D.</span><span class="sxs-lookup"><span data-stu-id="77285-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="77285-115">Audio no admite transiciones.</span><span class="sxs-lookup"><span data-stu-id="77285-115">Audio does not support transitions.</span></span>

<span data-ttu-id="77285-116">Los grupos, las composiciones y las pistas no tienen subobjetos.</span><span class="sxs-lookup"><span data-stu-id="77285-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="77285-117">La aplicación no establece directamente el puntero de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="77285-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="77285-118">En el caso de los efectos y las transiciones, la aplicación llama al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar el GUID del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="77285-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="77285-119">En el caso de los objetos de origen, una aplicación normalmente llama a [**IAMTimelineSrc:: SetMediaName**](iamtimelinesrc-setmedianame.md) para especificar el nombre de un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="77285-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="77285-120">Sin embargo, el método **SetSubObjectGUID** también se puede usar para los objetos de origen, para especificar el identificador de clase (CLSID) de un filtro.</span><span class="sxs-lookup"><span data-stu-id="77285-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="77285-121">Para obtener más información, vea [trabajar con orígenes](working-with-sources.md) y [trabajar con efectos y transiciones](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="77285-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77285-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77285-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77285-123">Información general de los componentes de la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="77285-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 




---
description: Ejemplo de DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Ejemplo de DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274787"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="1a65f-103">Ejemplo de DMOEnum</span><span class="sxs-lookup"><span data-stu-id="1a65f-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="1a65f-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a65f-104">Description</span></span>

<span data-ttu-id="1a65f-105">En esta aplicación de ejemplo se enumeran todos los [objetos multimedia de DirectX](directx-media-objects.md) (DMOs) registrados en el sistema del usuario y se muestra información sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="1a65f-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="1a65f-106">En el ejemplo se usa la función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) y la interfaz [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar el DMOs.</span><span class="sxs-lookup"><span data-stu-id="1a65f-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="1a65f-107">Usa la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) y otras interfaces de DMO para recuperar información acerca de cada DMO.</span><span class="sxs-lookup"><span data-stu-id="1a65f-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="1a65f-108">Uso</span><span class="sxs-lookup"><span data-stu-id="1a65f-108">Usage</span></span>

<span data-ttu-id="1a65f-109">Cuando se inicia la aplicación, enumera todas las DMOs instaladas.</span><span class="sxs-lookup"><span data-stu-id="1a65f-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="1a65f-110">Si selecciona una categoría de DMO específica, la aplicación muestra solo los DMOs de esa categoría.</span><span class="sxs-lookup"><span data-stu-id="1a65f-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="1a65f-111">Para ver información acerca de un DMO, seleccione el DMO en la lista.</span><span class="sxs-lookup"><span data-stu-id="1a65f-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="1a65f-112">La aplicación muestra el número de flujos, los tipos de medios preferidos, el servidor DLL para ese DMO y otra información acerca de DMO.</span><span class="sxs-lookup"><span data-stu-id="1a65f-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="1a65f-113">Para incluir o excluir DMOs con clave, active la casilla **incluir DMOs con clave** .</span><span class="sxs-lookup"><span data-stu-id="1a65f-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="1a65f-114">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a65f-114">Downloading the Sample</span></span>

<span data-ttu-id="1a65f-115">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a65f-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="1a65f-116">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ multimedia \\ DirectShow \\ varios \\ DMOEnum.</span><span class="sxs-lookup"><span data-stu-id="1a65f-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a65f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a65f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a65f-118">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a65f-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 




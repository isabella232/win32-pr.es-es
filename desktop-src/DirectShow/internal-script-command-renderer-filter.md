---
description: Filtro de representador de comando de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de representador de comando de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537348"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="4d3c1-103">Filtro de representador de comando de script interno</span><span class="sxs-lookup"><span data-stu-id="4d3c1-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="4d3c1-104">Recibe comandos de script y los envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="4d3c1-105">Este filtro acepta comandos de script en uno de los dos formatos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4d3c1-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="4d3c1-106">\_Texto MEDIATYPE: cada ejemplo multimedia contiene una cadena de texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="4d3c1-107">MEDIATYPE \_ comando: cada ejemplo multimedia contiene dos cadenas Unicode terminadas en null, concatenadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="4d3c1-108">La primera cadena describe el tipo de comando y la segunda cadena es el comando de script.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="4d3c1-109">Cuando el filtro recibe un ejemplo, envía una notificación de evento de [**\_ \_ evento OLE de EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="4d3c1-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="4d3c1-110">El primer parámetro de evento es un **BSTR** con el tipo de comando o `Text` si el formato es \_ texto de MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="4d3c1-111">El segundo parámetro de evento es un **BSTR** con el comando de script.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="4d3c1-112">La aplicación puede recuperar el evento y responder al comando de script.</span><span class="sxs-lookup"><span data-stu-id="4d3c1-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="4d3c1-113">Para obtener un ejemplo de cómo usar este filtro, vea [Sami (CC) parser](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4d3c1-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d3c1-114">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="4d3c1-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="4d3c1-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d3c1-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3c1-116">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="4d3c1-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="4d3c1-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="4d3c1-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="4d3c1-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="4d3c1-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3c1-119">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="4d3c1-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="4d3c1-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="4d3c1-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3c1-121">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="4d3c1-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="4d3c1-122">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4d3c1-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3c1-123">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="4d3c1-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="4d3c1-124">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4d3c1-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3c1-125">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="4d3c1-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="4d3c1-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="4d3c1-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3c1-127">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4d3c1-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="4d3c1-128">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4d3c1-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3c1-129">Executable</span><span class="sxs-lookup"><span data-stu-id="4d3c1-129">Executable</span></span></td>
<td><span data-ttu-id="4d3c1-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4d3c1-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3c1-131"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="4d3c1-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="4d3c1-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="4d3c1-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3c1-133"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="4d3c1-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="4d3c1-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4d3c1-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4d3c1-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d3c1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3c1-136">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4d3c1-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




---
title: El modelo de presentación en cola está en desuso
description: El modelo de presentación en cola está en desuso
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "105705067"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="1cb65-103">El modelo de presentación en cola está en desuso</span><span class="sxs-lookup"><span data-stu-id="1cb65-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="1cb65-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="1cb65-104">Platforms</span></span>

<span data-ttu-id="1cb65-105">**Clientes** : después de Windows 8</span><span class="sxs-lookup"><span data-stu-id="1cb65-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="1cb65-106">**Servidores** : después de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cb65-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="1cb65-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb65-107">Description</span></span>

<span data-ttu-id="1cb65-108">En la versión de Windows después de Windows 8, estas API devolverán E \_ NOTIMPL:</span><span class="sxs-lookup"><span data-stu-id="1cb65-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="1cb65-109">DwmSetPresentParameters</span><span class="sxs-lookup"><span data-stu-id="1cb65-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="1cb65-110">DwmSetDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="1cb65-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="1cb65-111">DwmModifyPreviousDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="1cb65-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="1cb65-112">Además, esta API solo aceptará el valor NULL para el parámetro HWND:</span><span class="sxs-lookup"><span data-stu-id="1cb65-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="1cb65-113">DwmGetCompositionTimingInfo</span><span class="sxs-lookup"><span data-stu-id="1cb65-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="1cb65-114">Se dejará de admitir DwmGetCompositionTimingInfo con HWND! = NULL y se quitará la funcionalidad asociada.</span><span class="sxs-lookup"><span data-stu-id="1cb65-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="1cb65-115">Si se especifica un valor distinto de NULL para HWND, esta API devolverá E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1cb65-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="1cb65-116">También se desaconseja el uso de la API de DwmGetCompositionTimingInfo y se sugiere que los desarrolladores cambien a DXGI Flip Model y la API de DX present Statistics asociada.</span><span class="sxs-lookup"><span data-stu-id="1cb65-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="1cb65-117">Manifestación</span><span class="sxs-lookup"><span data-stu-id="1cb65-117">Manifestation</span></span>

<span data-ttu-id="1cb65-118">Las aplicaciones que usan el modelo de presentación en cola no funcionarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="1cb65-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="1cb65-119">La manifestación exacta depende de la aplicación determinada, pero puede variar de un tiempo de presentación incorrecto a la aplicación saliendo inesperadamente).</span><span class="sxs-lookup"><span data-stu-id="1cb65-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="1cb65-120">En la práctica, no esperamos ver muchas aplicaciones (si las hay).</span><span class="sxs-lookup"><span data-stu-id="1cb65-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="1cb65-121">El reproductor de media de vista usó este modelo, que no se usará en Windows 8 (y posiblemente el reproductor de Zune anterior).</span><span class="sxs-lookup"><span data-stu-id="1cb65-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="1cb65-122">En este momento, no tenemos información sobre otras aplicaciones que usan realmente este modelo.</span><span class="sxs-lookup"><span data-stu-id="1cb65-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="1cb65-123">Solución</span><span class="sxs-lookup"><span data-stu-id="1cb65-123">Solution</span></span>

<span data-ttu-id="1cb65-124">Los desarrolladores deben usar el modo de presentación de flip de DXGI en lugar de presentar la cola (disponible en el tiempo de ejecución de DX9 desde Windows 7 y en los tiempos de ejecución de contenido DX10 y DX11 en Windows 8).</span><span class="sxs-lookup"><span data-stu-id="1cb65-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="1cb65-125">Pruebas</span><span class="sxs-lookup"><span data-stu-id="1cb65-125">Tests</span></span>

<span data-ttu-id="1cb65-126">Ejecute pruebas generales para asegurarse de que los componentes de Windows de la bandeja de entrada y los productos principales continúan funcionando en la siguiente versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="1cb65-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 





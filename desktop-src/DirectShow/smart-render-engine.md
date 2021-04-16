---
description: Smart Render Engine
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Smart Render Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686366"
---
# <a name="smart-render-engine"></a><span data-ttu-id="02ada-103">Smart Render Engine</span><span class="sxs-lookup"><span data-stu-id="02ada-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="02ada-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="02ada-104">\[Deprecated.</span></span> <span data-ttu-id="02ada-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02ada-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02ada-106">El objeto Smart Render Engine representa la salida comprimida de una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="02ada-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="02ada-107">Para crear este objeto, llame a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="02ada-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="02ada-108">En el caso de la salida sin comprimir, use el motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="02ada-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="02ada-109">El identificador de clase es CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="02ada-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="02ada-110">El motor de representación inteligente expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="02ada-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="02ada-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="02ada-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="02ada-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="02ada-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="02ada-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="02ada-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="02ada-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="02ada-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="02ada-115">**ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="02ada-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="02ada-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02ada-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ada-117">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="02ada-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="02ada-118">Motor de representación básico</span><span class="sxs-lookup"><span data-stu-id="02ada-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 




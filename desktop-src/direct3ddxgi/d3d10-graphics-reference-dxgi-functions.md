---
description: Esta sección contiene información sobre las funciones proporcionadas por DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funciones de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536808"
---
# <a name="dxgi-functions"></a><span data-ttu-id="ca273-103">Funciones de DXGI</span><span class="sxs-lookup"><span data-stu-id="ca273-103">DXGI Functions</span></span>

<span data-ttu-id="ca273-104">Esta sección contiene información sobre las funciones proporcionadas por DXGI.</span><span class="sxs-lookup"><span data-stu-id="ca273-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca273-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ca273-105">In this section</span></span>



| <span data-ttu-id="ca273-106">Tema</span><span class="sxs-lookup"><span data-stu-id="ca273-106">Topic</span></span>                                                                                   | <span data-ttu-id="ca273-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca273-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca273-108">**CreateDXGIFactory**</span><span class="sxs-lookup"><span data-stu-id="ca273-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="ca273-109">Crea un generador de DXGI 1,0 que puede usar para generar otros objetos de DXGI.</span><span class="sxs-lookup"><span data-stu-id="ca273-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="ca273-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="ca273-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="ca273-111">Crea un generador de DXGI 1,1 que puede usar para generar otros objetos de DXGI.</span><span class="sxs-lookup"><span data-stu-id="ca273-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="ca273-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="ca273-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="ca273-113">Crea un generador de DXGI 1,3 que puede usar para generar otros objetos de DXGI.</span><span class="sxs-lookup"><span data-stu-id="ca273-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="ca273-114">En Windows 8, cualquier fábrica de DXGI creada mientras DXGIDebug.dll estaba presente en el sistema la cargaría y la usaría.</span><span class="sxs-lookup"><span data-stu-id="ca273-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="ca273-115">A partir de Windows 8.1, las aplicaciones solicitan explícitamente que se carguen DXGIDebug.dll en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ca273-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="ca273-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) y especifique el \_ marcador de \_ depuración de DXGI CREATE Factory \_ para solicitar DXGIDebug.dll; la dll se cargará si está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ca273-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="ca273-117">**DXGIDeclareAdapterRemovalSupport**</span><span class="sxs-lookup"><span data-stu-id="ca273-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="ca273-118">Permite que un proceso indique que es resistente a cualquiera de sus dispositivos de gráficos que se quitan.</span><span class="sxs-lookup"><span data-stu-id="ca273-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="ca273-119">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="ca273-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="ca273-120">Recupera una interfaz de depuración.</span><span class="sxs-lookup"><span data-stu-id="ca273-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ca273-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="ca273-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="ca273-122">Recupera una interfaz que las aplicaciones de la tienda Windows usan para depurar la infraestructura de gráficos de Microsoft DirectX (DXGI).</span><span class="sxs-lookup"><span data-stu-id="ca273-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ca273-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca273-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca273-124">Referencia de DXGI</span><span class="sxs-lookup"><span data-stu-id="ca273-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 





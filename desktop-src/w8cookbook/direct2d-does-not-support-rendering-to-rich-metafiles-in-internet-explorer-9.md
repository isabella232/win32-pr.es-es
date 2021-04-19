---
title: Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9
description: Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314828"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="21a2c-103">Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="21a2c-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="21a2c-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="21a2c-104">Platforms</span></span>

<span data-ttu-id="21a2c-105">**Clientes** : Windows Vista, Windows 7, Windows 8</span><span class="sxs-lookup"><span data-stu-id="21a2c-105">**Clients** – Windows Vista, Windows 7, Windows 8</span></span>  
<span data-ttu-id="21a2c-106">**Servidores** : windows Server 2008, windows Server 2008 R2 y windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21a2c-106">**Servers** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="21a2c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="21a2c-107">Description</span></span>

<span data-ttu-id="21a2c-108">Debido a los cambios de representación internos en Internet Explorer 9, las API [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) y [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) crearán ahora un metarchivo que contiene un mapa de bits único que representa el contenido web en lugar de un metarchivo enriquecido que contiene texto e información de vector.</span><span class="sxs-lookup"><span data-stu-id="21a2c-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="21a2c-109">Este cambio se debía al procesamiento de la representación de GDI en Direct2D (D2D) con aceleración de hardware.</span><span class="sxs-lookup"><span data-stu-id="21a2c-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="21a2c-110">Este cambio afecta a las aplicaciones que usan estas API y se basan en la información de texto o vector del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="21a2c-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="21a2c-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="21a2c-111">Manifestation</span></span>

<span data-ttu-id="21a2c-112">En función de la aplicación que se vea afectada por este cambio, los usuarios podrían ver un comportamiento erróneo o incorrecto en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="21a2c-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="21a2c-113">Mitigación</span><span class="sxs-lookup"><span data-stu-id="21a2c-113">Mitigation</span></span>

<span data-ttu-id="21a2c-114">Las aplicaciones que solo necesitan extraer información de texto de un documento Web (sin información de posicionamiento) pueden usar la propiedad [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extraer texto.</span><span class="sxs-lookup"><span data-stu-id="21a2c-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="21a2c-115">Las aplicaciones que usan IViewObject::D RAW pueden usar la [característica \_ IVIEWOBJECTDRAW \_ DMLT9 \_ con \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la clave de control de características de GDI para revertir a la representación de GDI si el modo de documento:</span><span class="sxs-lookup"><span data-stu-id="21a2c-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="21a2c-116">Es menor o igual que 8</span><span class="sxs-lookup"><span data-stu-id="21a2c-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="21a2c-117">FCK autoriza a ese host a usar GDI</span><span class="sxs-lookup"><span data-stu-id="21a2c-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="21a2c-118">Y se pasa un DC de metarchivo a la API</span><span class="sxs-lookup"><span data-stu-id="21a2c-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="21a2c-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="21a2c-119">Resources</span></span>

-   <span data-ttu-id="21a2c-120">[IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21a2c-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="21a2c-121">IViewObject::D RAW</span><span class="sxs-lookup"><span data-stu-id="21a2c-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="21a2c-122">[IHTMLElement:: innerText (propiedad)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21a2c-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="21a2c-123">[Controles de características de Internet (I.. CG](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21a2c-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 
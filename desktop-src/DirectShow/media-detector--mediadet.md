---
description: Detector de medios (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de medios (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157020"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="c485d-103">Detector de medios (MediaDet)</span><span class="sxs-lookup"><span data-stu-id="c485d-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="c485d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c485d-104">\[Deprecated.</span></span> <span data-ttu-id="c485d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c485d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c485d-106">El objeto de detección de medios (MediaDet) recupera la información de formato y las tramas fijas de los orígenes de archivo.</span><span class="sxs-lookup"><span data-stu-id="c485d-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="c485d-107">El detector de medios no requiere que funcione el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="c485d-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="c485d-108">Para crear este objeto, llame a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="c485d-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="c485d-109">El identificador de clase es CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="c485d-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="c485d-110">Para leer archivos de™ de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave.</span><span class="sxs-lookup"><span data-stu-id="c485d-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="c485d-111">Registre la aplicación como un proveedor de claves a través de la interfaz **IObjectWithSite** del detector de medios.</span><span class="sxs-lookup"><span data-stu-id="c485d-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="c485d-112">Para obtener más información, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="c485d-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="c485d-113">El objeto MediaDet expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="c485d-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="c485d-114">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="c485d-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="c485d-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="c485d-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c485d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c485d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c485d-117">Trabajar con orígenes</span><span class="sxs-lookup"><span data-stu-id="c485d-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 




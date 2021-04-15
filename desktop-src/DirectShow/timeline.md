---
description: Escala de tiempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688732"
---
# <a name="timeline"></a><span data-ttu-id="9a037-103">Escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="9a037-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="9a037-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9a037-104">\[Deprecated.</span></span> <span data-ttu-id="9a037-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a037-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9a037-106">El objeto Timeline administra todos los objetos de un proyecto de edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a037-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="9a037-107">Para crear este objeto, llame a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="9a037-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="9a037-108">El identificador de clase es CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="9a037-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="9a037-109">Para leer archivos de™ de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave.</span><span class="sxs-lookup"><span data-stu-id="9a037-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="9a037-110">Registre la aplicación como proveedor de claves a través de la interfaz **IObjectWithSite** de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="9a037-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="9a037-111">Para obtener más información, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="9a037-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="9a037-112">El objeto Timeline expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="9a037-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="9a037-113">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="9a037-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="9a037-114">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="9a037-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="9a037-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="9a037-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="9a037-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="9a037-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a037-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a037-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a037-118">Modelo de escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="9a037-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="9a037-119">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="9a037-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




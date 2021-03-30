---
title: Versiones de DRM
description: Versiones de DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- SDK de Windows Media Format, versiones de DRM
- Administración de derechos digitales (DRM), versiones
- DRM (administración de derechos digitales), versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994085"
---
# <a name="drm-versions"></a><span data-ttu-id="cee15-106">Versiones de DRM</span><span class="sxs-lookup"><span data-stu-id="cee15-106">DRM Versions</span></span>

<span data-ttu-id="cee15-107">Hay varias versiones de administración de derechos digitales (DRM) de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cee15-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="cee15-108">La versión 1 de DRM suele estar separada de las otras versiones de esta documentación, ya que se implementa mediante técnicas que son diferentes de las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cee15-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="cee15-109">La segunda generación de DRM de Windows Media se denomina DRM versión 7 porque se presentó como parte del SDK de Windows Media Format 7.</span><span class="sxs-lookup"><span data-stu-id="cee15-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="cee15-110">A veces se denomina DRM versión 2.</span><span class="sxs-lookup"><span data-stu-id="cee15-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="cee15-111">Las versiones posteriores de DRM de Windows Media, DRM versión 9 y el nuevo Windows Media DRM 10, son extensiones de la versión 7 de DRM y usan los mismos procedimientos para la implementación.</span><span class="sxs-lookup"><span data-stu-id="cee15-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="cee15-112">Todas las versiones de Windows Media DRM usan las mismas rutinas de cifrado. las diferencias entre las versiones tienen que hacer con las características de licencia.</span><span class="sxs-lookup"><span data-stu-id="cee15-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="cee15-113">Al crear archivos protegidos con los objetos del SDK de Windows Media Format, debe admitir la versión 1 y la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="cee15-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="cee15-114">Los archivos protegidos por la versión 1 de DRM se diferencian de los archivos protegidos por versiones posteriores solo en el contenido del encabezado.</span><span class="sxs-lookup"><span data-stu-id="cee15-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="cee15-115">Los archivos más recientes que contienen la información de encabezado adicional se pueden seguir usando en clientes que solo representan contenido de la versión 1.</span><span class="sxs-lookup"><span data-stu-id="cee15-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="cee15-116">Aunque las versiones posteriores de DRM ofrecen un mayor nivel de seguridad y características adicionales, hay todavía muchos reproductores que solo usan la versión 1.</span><span class="sxs-lookup"><span data-stu-id="cee15-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="cee15-117">Para obtener más información sobre las versiones de DRM, consulte la documentación del SDK de Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="cee15-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="cee15-118">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="cee15-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cee15-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cee15-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee15-120">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="cee15-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="cee15-121">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="cee15-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 





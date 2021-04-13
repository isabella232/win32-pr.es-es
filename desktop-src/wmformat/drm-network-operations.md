---
title: Operaciones de red DRM
description: Operaciones de red DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- SDK de Windows Media Format, operaciones de red DRM
- Advanced Systems Format (ASF), operaciones de red DRM
- ASF (formato de sistemas avanzados), operaciones de red DRM
- Administración de derechos digitales (DRM), operaciones de red
- DRM (administración de derechos digitales), operaciones de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356776"
---
# <a name="drm-network-operations"></a><span data-ttu-id="c3a9b-108">Operaciones de red DRM</span><span class="sxs-lookup"><span data-stu-id="c3a9b-108">DRM Network Operations</span></span>

<span data-ttu-id="c3a9b-109">Varias operaciones relacionadas con DRM requieren que la aplicación se conecte a un servicio que se ejecuta en una red.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="c3a9b-110">Estas operaciones incluyen la individualización, adquisición de licencias, revocación de licencias y copia de seguridad y restauración de licencias.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="c3a9b-111">Como con cualquier transacción de red, la aplicación debe tener en cuenta una serie de dificultades al incluir características que requieren operaciones de red.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="c3a9b-112">La aplicación debe realizar un seguimiento del estado de la operación en cualquier medida que sea posible para la característica específica, normalmente mediante el control de los mensajes de estado.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="c3a9b-113">Debe proporcionar comentarios al usuario sobre el estado.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="c3a9b-114">Si se produce un error en una operación en el primer intento, debe proporcionar al usuario la oportunidad de volver a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="c3a9b-115">En muchos casos, el primer intento tiene problemas, pero un intento posterior se completa sin errores.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="c3a9b-116">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="c3a9b-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c3a9b-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3a9b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3a9b-118">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="c3a9b-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




